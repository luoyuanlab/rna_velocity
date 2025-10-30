#  **Mechanism-grounded RNA velocity: from kinetic models to deep learning and foundation models**

### **Overview**
Single-cell RNA sequencing (scRNA-seq) provides unprecedented resolution of cellular states but captures only a static snapshot, limiting its ability to reveal dynamic biological processes. RNA velocity overcomes part of this limitation by inferring short-term transcriptional dynamics from unspliced and spliced mRNA abundances, thereby estimating each cell’s future state.

Despite substantial methodological progress, existing RNA velocity models remain limited by simplified assumptions, such as simplified kinetic assumptions, overlook of gene regulatory networks, and insufficient incorporation of developmental trajectory constraints. These constraints can compromise both accuracy and interpretability, particularly in complex or heterogeneous developmental systems.

<img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%201.png" height="800px" />  <br />
<p align="center">  <img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%201.png" height="800px" />  </p>  <br />

### **Benchmark on real datasets**
To systematically evaluate current models, we benchmarked them on two well-characterized datasets, mouse gastrulation erythroid lineage and mouse dentate gyrus, both of which are widely used due to their rich biological annotation and challenging dynamic structures.

### **Benchmark on simulated dataset: tumor microenvironment**
To further assess model performance under spatially heterogeneous kinetics, we simulated 4,000 CD8⁺ T cells (2,000 from immune-sensitive and 2,000 from immune-resistant regions) focusing on PTPN11, KRAS, and MAPK1. Among the three genes, only PTPN11 in the immune-sensitive area exhibits gradually changing transcription, whereas KRAS and MAPK1 in the immune-sensitive area, and all three genes in the immune-resistant area display abrupt shifts in their transcription rates (α) at specific time points such as T-cell activation or PD-1/PD-L1 binding (Figure). These sharp kinetic transitions are particularly challenging for conventional RNA velocity models, which typically assume smooth or even time-invariant transcription rates, to capture.

<img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%203.png" height="800px" />  <br />
