# chemical editor or chemical view tools

1. 3DMol
https://github.com/3dmol/3Dmol.js
2. ChemdoodleWeb
https://web.chemdoodle.com/
3. Marvin
https://www.chemaxon.com/products/marvin/marvin-js/
4. Jmol
http://www.jmol.org/
5. Chemozart
https://github.com/mohebifar/chemozart
6. WebMo
https://www.webmo.net/demoserver/cgi-bin/webmo/login.cgi </br>
http://172.16.11.179:8005/cgi-bin/webmo/login.cgi
7. WebMol
https://github.com/cvdlab-projects/webmol
8. molcalc
http://172.16.11.179:8008/molcalc </br>
https://github.com/jensengroup/molcalc
9. molview
http://molview.org 
10. GLmol
http://webglmol.osdn.jp/index-en.html
11. rescale
https://platform.rescale.com
12. for vasp
https://github.com/hzhangxyz/Visual-CONTCAR
13. ..
https://github.com/mohebifar/molcanvas.js
14. Kekule.js
http://partridgejiang.github.io/Kekule.js/
15. pv
https://github.com/biasmv/pv
16. ngl
http://nglviewer.org/ngl/

17. CH5M3D  https://sourceforge.net/projects/ch5m3d/

18. Molmil  https://github.com/gjbekker/molmil/

19.  iCn3D  https://www.ncbi.nlm.nih.gov/Structure/icn3d/docs/icn3d_about.html

20.  Web3DMol https://www.researchgate.net/publication/316843332_Web3DMol_Interactive_protein_structure_visualization_based_on_WebGL

21.  HTMoLAR  https://github.com/es605/HTMoLAR

22. mmView  https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3094370/

23. open-mx  http://www.openmx-square.org/viewer/index.html

view atomic electronic-stucture on web

# 开发计划
1.从前端读入文件方式：
* 打开本地文本（支持cif/mol/sdf格式）；
* 直接贴入字符串。

An example for  Crystallographic Information Files （cif） file format from MS:
```
#------------------------------------------------------------------------------
#$Date: 2016-02-18 13:08:31 +0200 (Thu, 18 Feb 2016) $
#$Revision: 176725 $
#$URL: svn://www.crystallography.net/cod/cif/9/00/83/9008393.cif $
#------------------------------------------------------------------------------
#
# This file is available in the Crystallography Open Database (COD),
# http://www.crystallography.net/. The original data for this entry
# were provided the American Mineralogist Crystal Structure Database,
# http://rruff.geo.arizona.edu/AMS/amcsd.php
#
# The file may be used within the scientific community so long as
# proper attribution is given to the journal article from which the
# data were obtained.
#
data_9008393
loop_
_publ_author_name
'Nowack, E.'
'Schwarzenbach, D.'
'Gonschorek, W.'
'Hahn, T.'
_publ_section_title
;
 Deformationsdichten in CoS2 und NiS2 mit pyritstruktur
 Note: T = 295 K
 Note: pyrite structure
;
_journal_name_full               'Zeitschrift fur Kristallographie'
_journal_page_first              213
_journal_page_last               215
_journal_volume                  186
_journal_year                    1989
_chemical_formula_sum            'Co S2'
_chemical_name_mineral           Cattierite
_space_group_IT_number           205
_symmetry_space_group_name_Hall  '-P 2ac 2ab 3'
_symmetry_space_group_name_H-M   'P a -3'
_cell_angle_alpha                90
_cell_angle_beta                 90
_cell_angle_gamma                90
_cell_length_a                   5.5385
_cell_length_b                   5.5385
_cell_length_c                   5.5385
_cell_volume                     169.893
_diffrn_ambient_temperature      295
_exptl_crystal_density_diffrn    4.811
_cod_original_sg_symbol_H-M      'P a 3'
_cod_database_code               9008393
loop_
_symmetry_equiv_pos_as_xyz
x,y,z
1/2+z,x,1/2-y
z,1/2-x,1/2+y
1/2-z,1/2+x,y
-z,-x,-y
1/2+y,1/2-z,-x
1/2-y,-z,1/2+x
-y,1/2+z,1/2-x
y,z,x
x,1/2-y,1/2+z
1/2-x,1/2+y,z
1/2+x,y,1/2-z
-x,-y,-z
1/2-z,-x,1/2+y
-z,1/2+x,1/2-y
1/2+z,1/2-x,-y
z,x,y
1/2-y,1/2+z,x
1/2+y,z,1/2-x
y,1/2-z,1/2+x
-y,-z,-x
-x,1/2+y,1/2-z
1/2+x,1/2-y,-z
1/2-x,-y,1/2+z
loop_
_atom_site_aniso_label
_atom_site_aniso_U_11
_atom_site_aniso_U_22
_atom_site_aniso_U_33
_atom_site_aniso_U_12
_atom_site_aniso_U_13
_atom_site_aniso_U_23
Co 0.00436 0.00436 0.00436 0.00002 0.00002 0.00002
S 0.00446 0.00446 0.00446 -0.00010 -0.00010 -0.00010
loop_
_atom_site_label
_atom_site_fract_x
_atom_site_fract_y
_atom_site_fract_z
Co 0.00000 0.00000 0.00000
S 0.38987 0.38987 0.38987

```

An example for CIF from ICSD:

```

#(C) 2018 by FIZ Karlsruhe - Leibniz Institute for Information Infrastructure.  All rights reserved.
data_86351-ICSD
_database_code_ICSD 86351
_audit_creation_date 1999-11-30
_audit_update_record 2003-04-01
_chemical_name_systematic 'Cobalt disulfide'
_chemical_formula_structural 'Co S2'
_chemical_formula_sum 'Co1 S2'
_chemical_name_structure_type Pyrite-FeS2(cP12)
_chemical_name_mineral Galtierite
_exptl_crystal_density_diffrn 4.81
_cell_measurement_temperature 295.
_publ_section_title 'Charge densities in Co S2 and Ni S2 (pyrite structure)'
loop_
_citation_id
_citation_journal_full
_citation_year
_citation_journal_volume
_citation_page_first
_citation_page_last
_citation_journal_id_ASTM
primary 'Acta Crystallographica, Section B: Structural Science' 1991 47 650 659
ASBSDK
loop_
_publ_author_name
'Nowack, E.'
'Schwarzenbach, D.'
'Hahn, T.'
_cell_length_a 5.5385(2)
_cell_length_b 5.5385(2)
_cell_length_c 5.5385(2)
_cell_angle_alpha 90.
_cell_angle_beta 90.
_cell_angle_gamma 90.
_cell_volume 169.89
_cell_formula_units_Z 4
_symmetry_space_group_name_H-M 'P a -3'
_symmetry_Int_Tables_number 205
_refine_ls_R_factor_all 0.015
loop_
_symmetry_equiv_pos_site_id
_symmetry_equiv_pos_as_xyz
1 '-z+1/2, x+1/2, y'
2 'z+1/2, x, -y+1/2'
3 'z, -x+1/2, y+1/2'
4 '-z, -x, -y'
5 'y, -z+1/2, x+1/2'
6 '-y+1/2, z+1/2, x'
7 'y+1/2, z, -x+1/2'
8 '-y, -z, -x'
9 'x+1/2, y, -z+1/2'
10 'x, -y+1/2, z+1/2'
11 '-x+1/2, y+1/2, z'
12 '-x, -y, -z'
13 'z+1/2, -x+1/2, -y'
14 '-z+1/2, -x, y+1/2'
15 '-z, x+1/2, -y+1/2'
16 'z, x, y'
17 '-y, z+1/2, -x+1/2'
18 'y+1/2, -z+1/2, -x'
19 '-y+1/2, -z, x+1/2'
20 'y, z, x'
21 '-x+1/2, -y, z+1/2'
22 '-x, y+1/2, -z+1/2'
23 'x+1/2, -y+1/2, -z'
24 'x, y, z'
loop_
_atom_type_symbol
_atom_type_oxidation_number
Co2+ 2
S1- -1
loop_
_atom_site_label
_atom_site_type_symbol
_atom_site_symmetry_multiplicity
_atom_site_Wyckoff_symbol
_atom_site_fract_x
_atom_site_fract_y
_atom_site_fract_z
_atom_site_B_iso_or_equiv
_atom_site_occupancy
_atom_site_attached_hydrogens
Co1 Co2+ 4 a 0 0 0 . 1. 0
S1 S1- 8 c 0.38988(1) 0.38988(1) 0.38988(1) . 1. 0
loop_
_atom_site_aniso_label
_atom_site_aniso_type_symbol
_atom_site_aniso_U_11
_atom_site_aniso_U_22
_atom_site_aniso_U_33
_atom_site_aniso_U_12
_atom_site_aniso_U_13
_atom_site_aniso_U_23
Co1 Co2+ 0.00426(2) 0.00426(2) 0.00426(2) 0.00001(1) 0.00001(1) 0.00001(1)
S1 S1- 0.00453(2) 0.00453(2) 0.00453(2) -0.00016(2) -0.00016(2) -0.00016(2)
#End of TTdata_86351-ICSD
```
An example for CIF file from CCDC:
```

#######################################################################
#
#                 Cambridge Crystallographic Data Centre
#                                CCDC 
#
#######################################################################
#
# If this CIF has been generated from an entry in the Cambridge 
# Structural Database, then it will include bibliographic, chemical, 
# crystal, experimental, refinement or atomic coordinate data resulting 
# from the CCDC's data processing and validation procedures.
#
#######################################################################

data_ABAFOA
_symmetry_cell_setting           triclinic
_symmetry_space_group_name_H-M   'P -1'
_symmetry_Int_Tables_number      2
_space_group_name_Hall           '-P 1'
loop_
_symmetry_equiv_pos_site_id
_symmetry_equiv_pos_as_xyz
1 x,y,z
2 -x,-y,-z
_cell_length_a                   8.6031(3)
_cell_length_b                   8.8247(3)
_cell_length_c                   10.4609(4)
_cell_angle_alpha                80.514(2)
_cell_angle_beta                 87.499(2)
_cell_angle_gamma                72.114(2)
_cell_volume                     745.45
loop_
_atom_site_label
_atom_site_type_symbol
_atom_site_fract_x
_atom_site_fract_y
_atom_site_fract_z
C1 C 1.15482(15) 0.39757(15) 0.76616(11)
C2 C 1.28283(17) 0.27239(16) 0.72999(13)
H1 H 1.2641 0.1969 0.6851
C3 C 1.43894(17) 0.26447(17) 0.76330(13)
H2 H 1.5267 0.1814 0.7408
C4 C 1.46875(17) 0.37727(17) 0.82957(13)
H3 H 1.5755 0.3684 0.8503
C5 C 1.34207(15) 0.50179(16) 0.86478(12)
H4 H 1.3622 0.5774 0.9087
C6 C 1.18294(15) 0.51223(14) 0.83321(11)
C7 C 1.02493(14) 0.62392(14) 0.85320(11)
C8 C 0.97472(15) 0.75589(15) 0.91712(12)
H5 H 1.0505 0.7899 0.9561
C9 C 0.80848(16) 0.83680(15) 0.92188(12)
C10 C 0.69339(16) 0.78683(16) 0.86297(13)
H6 H 0.5829 0.8431 0.8670
C11 C 0.74155(16) 0.65580(16) 0.79929(13)
H7 H 0.6653 0.6228 0.7599
C12 C 0.90815(15) 0.57363(15) 0.79534(11)
C13 C 0.91238(15) 0.35356(16) 0.67085(12)
C14 C 0.81166(17) 0.43835(18) 0.56626(12)
H8 H 0.7938 0.5487 0.5431
C15 C 0.73821(18) 0.3594(2) 0.49679(13)
H9 H 0.6688 0.4181 0.4282
C16 C 0.76514(18) 0.1943(2) 0.52662(14)
C17 C 0.86723(18) 0.11099(18) 0.63019(15)
H10 H 0.8883 -0.0001 0.6512
C18 C 0.93897(17) 0.18914(16) 0.70359(13)
H11 H 1.0047 0.1313 0.7745
C19 C 0.6847(3) 0.1091(3) 0.4495(2)
H12 H 0.5682 0.1520 0.4557
H13 H 0.7182 -0.0041 0.4832
H14 H 0.7163 0.1249 0.3603
C20 C 0.75645(17) 0.97199(16) 0.99028(14)
N1 N 0.98705(12) 0.43589(13) 0.74328(10)
N2 N 0.72084(16) 1.07784(16) 1.04614(14)

#END

```

Another no-cubic box CIF file example from CCDC:
```

#######################################################################
#
#                 Cambridge Crystallographic Data Centre
#                                CCDC 
#
#######################################################################
#
# If this CIF has been generated from an entry in the Cambridge 
# Structural Database, then it will include bibliographic, chemical, 
# crystal, experimental, refinement or atomic coordinate data resulting 
# from the CCDC's data processing and validation procedures.
#
#######################################################################

data_ZZZZCB03
_symmetry_cell_setting           triclinic
_symmetry_space_group_name_H-M   'P -1'
_symmetry_Int_Tables_number      2
_space_group_name_Hall           '-P 1'
loop_
_symmetry_equiv_pos_site_id
_symmetry_equiv_pos_as_xyz
1 x,y,z
2 -x,-y,-z
_cell_length_a                   13.442(4)
_cell_length_b                   4.869(2)
_cell_length_c                   12.192(2)
_cell_angle_alpha                88.58(2)
_cell_angle_beta                 116.76(2)
_cell_angle_gamma                88.91(2)
_cell_volume                     711.869
loop_
_atom_site_label
_atom_site_type_symbol
_atom_site_fract_x
_atom_site_fract_y
_atom_site_fract_z
O1 O 0.09200 0.24010 0.02210
O2 O -0.05660 0.14830 -0.15270
O3 O 0.15950 1.03250 -0.35780
C1 C 0.06400 0.48780 -0.15910
C2 C 0.00490 0.51950 -0.28690
C3 C 0.03820 0.70610 -0.35000
C4 C 0.13160 0.85840 -0.28720
C5 C 0.19040 0.83250 -0.15970
C6 C 0.15530 0.64660 -0.09770
C7 C 0.03370 0.28130 -0.09030
C8 C 0.25940 1.18500 -0.29900
C9 C 0.27600 1.34200 -0.39690
C10 C 0.29400 1.16310 -0.48630
C11 C 0.32630 1.32460 -0.57330
C12 C 0.34720 1.14910 -0.66160
C13 C 0.38520 1.31090 -0.74340
C14 C 0.40390 1.13690 -0.83440
C15 C 0.44790 1.30400 -0.91050
H1 H -0.06800 0.41300 -0.33500
H2 H -0.00200 0.72900 -0.43700
H3 H 0.26100 0.95500 -0.11000
H4 H 0.19300 0.62900 -0.00900
H5 H 0.32300 1.06100 -0.25400
H6 H 0.25300 1.30800 -0.23900
H7 H 0.34000 1.47300 -0.35300
H8 H 0.21200 1.47500 -0.44100
H9 H 0.35000 1.03600 -0.44300
H10 H 0.22900 1.06500 -0.53500
H11 H 0.39600 1.44800 -0.52400
H12 H 0.27200 1.47200 -0.61500
H13 H 0.40200 1.00400 -0.61500
H14 H 0.28200 1.03400 -0.71300
H15 H 0.46000 1.41700 -0.68800
H16 H 0.32700 1.48500 -0.78700
H17 H 0.46100 0.98500 -0.78900
H18 H 0.32300 1.04900 -0.88900
H19 H 0.40100 1.48400 -0.96000
H20 H 0.46700 1.15100 -0.97300
H21 H 0.53000 1.38600 -0.86600
H22 H -0.07100 -0.00600 -0.08900

#END

```


参考文献：https://nvlpubs.nist.gov/nistpubs/jres/101/3/j3brow.pdf  

参考代码：https://github.com/IkarosKappler/CIFFileReader.js

格式转换：http://home.ustc.edu.cn/~lipai/scripts/vasp_scripts/bash_cif2pos.html

文件格式描述：http://kuaibao.qq.com/s/20190103A07BWG00?refer=spider


2.支持晶体结构相关操作
* 切面；
* 建立超晶包；
* 建立真空层。

参考文献：https://www.sciencedirect.com/science/article/pii/S003960281300160X  
文章附件信息有matlab代码。
```
Pymatgen:
https://github.com/materialsproject/pymatgen
$ vi core/surface.py
...
687 class SlabGenerator:
..

Aflow:
http://materials.duke.edu/AFLOW/
$ vi aflow_surface.cpp
```
3.选定指定原子或原子团进行移动
* 点击原子（可持续点击）后，被选定；
* 移动方向（上/下/左/右），并且可以设定指定移动距离。

4.显示指定原子的距离/角度/二面角
* 点击length后，选择两个原子可以显示原子距离（距离用虚线表示）；
* 点击angle后，选择三个原子可以显示原子的角度；
* 点击dihedral,选择四个原子可以显示原子的二面角。

5.显示晶格参数
* 晶格边长
* 晶格角度


# upload files
1. 
https://github.com/hogenwang/beego-ueditor

2.
https://github.com/sthielen/BigUpload

3.
https://github.com/phpinside/ajaxUploadFile

# header && footer format
1.
https://github.com/ShaorxCN/photoShare

# angular.js vs react.js
https://hackernoon.com/reactjs-vs-angular-comparison-which-is-better-805c0b8091b1

# data viualization
https://github.com/wcharczuk/go-chart

# go package-example
https://github.com/radovskyb/go-packages

MDTraj: A Modern Open Library for the Analysis of Molecular Dynamics Trajectorier
https://www.cell.com/biophysj/references/S0006-3495(15)00826-7
