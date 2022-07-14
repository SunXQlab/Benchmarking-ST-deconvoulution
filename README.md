Benchmarking and integration of methods for deconvoluting spatial transcriptomic data
===========================
![image](https://github.com/SunXQlab/ST-deconvoulution/blob/main/figure1-framework_v2.jpg)

Implementation descripttion
--------------------------
We collected three synthetic ST datasets with known single-cell compositions and a human heart ST dataset with known regional cell type information
to benchmark 14 different deconvlution methods. Furthermore, we investigate the robustness of different methods to sequencing depth, spot size, and 
the choice of normalization. Moreover, we propose a new ensemble learning-based deconvolution method (EnDecon) by integrating multiple individual 
methods for more accurate deconvolution.
The main steps of benchamrking pipeline include: 
1) we employed two staregies to generate synthetic ST datasets with known cell type compositions as ground truth. For single-cell resolution ST data, we adopted 'grid' method to simulated ST data. For scRNA-seq data, we firstly first mapped it to the spatial locations of ST data to synthesize single-cell resolution ST data, and then simulated spatial mixtures with known cell type proportions using the ‘grid’ method;<br> 
2) we investigated the robustness of different methods to sequencing depth, spot size, and the choice of normalization;<br> 
3) we used RMSE, PCC, JSD to evaluate the performance of the 14 computational methods in disentangling cell type contribution from a single capture spot based on the above synthetic ST datasets;<br>
4) we developed an ensemble learning-based deconvolution method (EnDecon) for ST data by drawing on strengths from existing methods;<br> 

Datasets
--------------------------
All datasets can be downloaded from their respective sources:<br>
* mouse embryo was downloaded from the National Center for Biotechnology Information (NCBI) under GSE166692<br>
* MPOA was downloaded from https://datadryad.org/stash/dataset/doi:10.5061/dryad.8t8s248/<br>
* mouse brain ST data was download from https://www.dropbox.com/s/azjysbt7lbpmbew/brain_st_cortex.rds?dl=0 <br>
* mouse brain scRNA-seq data was downloaded from https://www.dropbox.com/s/ruseq3necn176c7/brain_sc.rds?dl=0<br>
* human developing heart ST data was downloaded from https://data.mendeley.com/datasets/mbvhhf8m62/2<br>

Dependencies and requirements for disentangle discrete cell types from spatial mixtures
---------------------------------
**R**<br>
RCTD(by spacexr of version 2.0.0)<br>
Giotto/PAGE/RANK/Hypergeometric(Version 1.1.0)<br>
spatialDWLS(by Giotto of Version 1.0.4)<br>
SPOTlight(Version 0.1.7)<br>
Seurat(Version 4.0.5)<br>
STdeconvolve(Version 0.1.0)<br>
EnDecon<br>
**Python**<br>
cell2location(Version 0.7a0)<br>
DestVI(scvi-tools Version 0.11.0)<br>
stereoscope(Version 0.3.1)<br>
STRIDE(Version 0.0.1b0)<br>
Tangram(Version 1.0.0)<br>





