#  **Mechanism-grounded RNA velocity: from kinetic models to deep learning and foundation models**

### **Overview**
Single-cell RNA sequencing (scRNA-seq) provides unprecedented resolution of cellular states but captures only a static snapshot, limiting its ability to reveal dynamic biological processes. RNA velocity overcomes part of this limitation by inferring short-term transcriptional dynamics from unspliced and spliced mRNA abundances, thereby estimating each cell’s future state.

Despite substantial methodological progress, existing RNA velocity models remain limited by simplified assumptions, such as simplified kinetic assumptions, overlook of gene regulatory networks, and insufficient incorporation of developmental trajectory constraints. These constraints can compromise both accuracy and interpretability, particularly in complex or heterogeneous developmental systems.

<p align="center">  <img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%201.png" height="800px" />  </p>  <br />

### **Benchmark on real datasets**
To systematically evaluate current models, we benchmarked them on two well-characterized datasets, mouse gastrulation erythroid lineage and mouse dentate gyrus, both of which are widely used due to their rich biological annotation and challenging dynamic structures. The dentate gyrus neurogenesis single cell data can be extracted using scVelo command scvelo.datasets.dentategyrus(). The mouse gastrulation erythroid lineage data can be extracted via scVelo command scvelo.datasets.gastrulation_erythroid().

### **Benchmark on simulated dataset: tumor microenvironment**
To further assess model performance under spatially heterogeneous kinetics, we simulated 4,000 CD8⁺ T cells (2,000 from immune-sensitive and 2,000 from immune-resistant regions) focusing on _PTPN11_, _KRAS_, and _MAPK1_. Among the three genes, only _PTPN11_ in the immune-sensitive area exhibits gradually changing transcription, whereas _KRAS_ and _MAPK1_ in the immune-sensitive area, and all three genes in the immune-resistant area display abrupt shifts in their transcription rates (_α_) at specific time points such as T-cell activation or PD-1/PD-L1 binding (Figure 2). These sharp kinetic transitions are particularly challenging for conventional RNA velocity models, which typically assume smooth or even time-invariant transcription rates, to capture.

<p align="center">  <img src="https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%203.png" height="800px" />  </p>  <br />
