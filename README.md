#  **Mechanism-grounded RNA velocity: from kinetic models to deep learning and foundation models**

### **Overview**
Single-cell RNA sequencing (scRNA-seq) provides unprecedented resolution of cellular states but captures only a static snapshot, limiting its ability to reveal dynamic biological processes. RNA velocity overcomes part of this limitation by inferring short-term transcriptional dynamics from unspliced and spliced mRNA abundances, thereby estimating each cell’s future state.

Despite substantial methodological progress, existing RNA velocity models remain limited by simplified kinetic assumptions, limited consideration of gene regulatory networks, and insufficient incorporation of developmental trajectory constraints. These constraints can compromise both accuracy and interpretability, particularly in complex or heterogeneous developmental systems.

<p align="center">  <img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%201.png" height="800px" />  </p>  <br />

### **Benchmark on real datasets**
To systematically evaluate current models, we benchmarked them on two well-characterized datasets, mouse gastrulation erythroid lineage and mouse dentate gyrus, both of which are widely used due to their rich biological annotation and challenging dynamic structures. The dentate gyrus neurogenesis single cell data can be extracted using [scVelo](https://scvelo.readthedocs.io/en/stable/index.html) command [scvelo.datasets.dentategyrus()](https://scvelo.readthedocs.io/en/stable/scvelo.datasets.dentategyrus.html). The mouse gastrulation erythroid lineage data can be extracted via [scVelo](https://scvelo.readthedocs.io/en/stable/index.html) command [scvelo.datasets.gastrulation_erythroid()](https://scvelo.readthedocs.io/en/stable/scvelo.datasets.gastrulation_erythroid.html).

### **Benchmark on simulated dataset: tumor microenvironment**
To further assess model performance under spatially heterogeneous kinetics, we simulated 4,000 CD8⁺ T cells (2,000 from immune-sensitive and 2,000 from immune-resistant regions) focusing on _PTPN11_, _KRAS_, and _MAPK1_. Among the three genes, only _PTPN11_ in the immune-sensitive area exhibits gradually changing transcription, whereas _KRAS_ and _MAPK1_ in the immune-sensitive area, and all three genes in the immune-resistant area display abrupt shifts in their transcription rates (_α_) at specific time points such as T-cell activation or PD-1/PD-L1 binding (Figure 2). These sharp kinetic transitions are particularly challenging for conventional RNA velocity models, which typically assume smooth or even time-invariant transcription rates, to capture. The simulated dataset in stored in the `Data/` directory, while the scripts in `simulation/` can be used to regenerate them.

<p align="center">  <img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%203.png" height="800px" />  </p>  <br />

## **System requirements**
### **OS Requirements**
The codes have been tested on the following systems:
* Linux: CentOS Linux 7

### **Tools**
Tools that are compared include:

* [scVelo](https://github.com/theislab/scvelo)
* [VeloVAE](https://github.com/welch-lab/VeloVAE)
* [LatentVelo](https://github.com/Spencerfar/LatentVelo)
* [RegVelo](https://github.com/theislab/regvelo)
* [UniTVelo](https://github.com/StatBiomed/UniTVelo)
* [VeloVI](https://github.com/YosefLab/velovi)
* [pyro-velocity](https://github.com/pinellolab/pyrovelocity)
* [DeepVelo](https://github.com/bowang-lab/DeepVelo)
* [DeepKINET](https://github.com/3254c/DeepKINET)
* [cell2fate](https://github.com/BayraktarLab/cell2fate)
* [cellDancer](https://github.com/GuangyuWangLab2021/cellDancer)

### **Python Dependencies**
<pre>
numpy
scipy
torch
pandas
scanpy
anndata
pickle
seaborn
umap
matplotlib
</pre>

### **Usage**
The codes for proceeding RNA velocity are stored in the `benchmark/` directory
