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
