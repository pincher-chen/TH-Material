首先我想先说一说我对整个CUDA部分的要做什么的理解，如果有错误请指出。

实际上整个CUDA部分实现的是 Conjugate Residual Method ，这是一个求线性方程组解的方法。CUDA 用这个方法的目的是为了求矩阵 $M_{\sigma}^{\dagger}(x) M_{\sigma}(x)$ 的逆，也就是解方程：

$$M_{\sigma}^{\dagger}(x) M_{\sigma}(x) \cdot x=I$$

根据文档内的定义 $M_{\sigma}^{\dagger}(x) M_{\sigma}(x)$ 的维度为 $N_{\tau} * N_{\tau}$ 。那矩阵 $x$ 和矩阵 $I$ 的维度应该都为 $N_{\tau} * N_{\tau}$。

### 关于输入

但是我在CUDA程序的输入输出中没有看到矩阵 $M_{\sigma}^{\dagger}(x) M_{\sigma}(x)$ 和维度 $N_{\tau} * N_{\tau}$ 。取而代之的是如下的输入（具体的数值以某一次调用`ftdqmc_conjgate_cg_`为例）

```
int ndim = 256;
int ltrot = 160;
int nfam = 4;
int lfam = 128;
cuDoubleComplex coshrtdtau = make_cuDoubleComplex(1.00125, 0); 
cuDoubleComplex sinhrtdtau = make_cuDoubleComplex(0.05, 0); 
cuDoubleComplex csqrt2 = make_cuDoubleComplex(1.4142, 0); 
int l_bonds[] = {1, 17, 3, 19, 5, 21, 7, 23, 9, ...};

int size1 = 40960; //ndim*ltrot;
int size2 = 81920; //lfam*nfam*ltrot;
// 四个 cuDoubleComplex 类型的数组
cuDoubleComplex * zep, * zem; //大小为size1
cuDoubleComplex *x, *b; //大小为size2
```

* 请问这些参数分别代表什么意义？
* 我怎么才能得到矩阵 $M_{\sigma}^{\dagger}(x) M_{\sigma}(x)$ 和维度 $N_{\tau} * N_{\tau}$ ？

### 关于 Conjugate Residual Method 的步骤

在函数`ftdqmc_conjgate_cg_`的迭代中有如下语句。

```
// update ar_k+1 = a*r_k
cudaStreamSynchronize(stream1);
cudaMemcpyAsync( phi2, r, sizeof(cuDoubleComplex)*size1, cudaMemcpyDeviceToDevice, stream2);
bmat2<<<dimGrid2, dimBlock, 0, stream2>>>(zep_d, zem_d, phi2);
cudaMemcpyAsync( phi1, r, sizeof(cuDoubleComplex)*size1, cudaMemcpyDeviceToDevice, stream1);
bmat1<<<dimGrid2, dimBlock, 0, stream1>>>(zep_d, zem_d, phi1);
cudaMemcpyAsync( phi3, phi1, sizeof(cuDoubleComplex)*size1, cudaMemcpyDeviceToDevice, stream1);
bmat1<<<dimGrid2, dimBlock, 0, stream1>>>(zep_d, zem_d, phi3);

// obtain ar_k+1
cudaStreamSynchronize(stream2);
vector_add3_new<<<dimGrid, dimBlock, 0, stream1>>>(phi1, phi2, phi3, r, ar);

// rar2
cublasSetStream(d, stream1);
cublasZdotc(d, size1, r, 1, ar, 1, rar2_d);
```

我能大概推测出其目的是为了计算文档式（59）中的$r_{k+1}^{\dagger} A r_{k+1}$， 但由于我不知道矩阵`A`是怎么表示的，所以我也不能理解每一个核函数具体的操作是什么。

* 请问能将上文代码中的每一步表达成数学公式吗？这样能方便我理解每一个核函数在做什么操作。

上次收到回复说`bmat1`和`bmat2`是在计算$B(\tau)*vec(\tau)$和$B(\tau)*vec(\tau+1)$。

* 请问$B(\tau)$是输入中的哪一个变量？
* $vec(\tau)$是输入中的哪一个变量？
* 计算$B(\tau)*vec(\tau)$和$B(\tau)*vec(\tau+1)$是 Conjugate Residual Method 迭代步骤的式（54）-（62）的哪一步（因为没有看到这样的步骤）？计算他们的目的是为了计算$r_{k+1}^{\dagger} A r_{k+1}$吗？
