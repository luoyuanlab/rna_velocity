#  **Mechanism-grounded RNA velocity: from kinetic models to deep learning and foundation models**

## **Description**
### **Overview**
Single-cell RNA sequencing (scRNA-seq) provides unprecedented resolution of cellular states but captures only a static snapshot, limiting its ability to reveal dynamic biological processes. RNA velocity overcomes part of this limitation by inferring short-term transcriptional dynamics from unspliced and spliced mRNA abundances, thereby estimating each cell’s future state.

Despite substantial methodological progress, existing RNA velocity models remain limited by simplified assumptions, such as simplified kinetic assumptions, overlook of gene regulatory networks, and insufficient incorporation of developmental trajectory constraints. These constraints can compromise both accuracy and interpretability, particularly in complex or heterogeneous developmental systems.

### **Benchmark on Real Datasets**
To systematically evaluate current models, we benchmarked them on two well-characterized datasets, mouse gastrulation erythroid lineage and mouse dentate gyrus, both of which are widely used due to their rich biological annotation and challenging dynamic structures.

### **Benchmark on Simulated Dataset: Tumor Microenvironment**
To further assess model performance under spatially heterogeneous kinetics, we simulated 4,000 CD8⁺ T cells (2,000 from immune-sensitive and 2,000 from immune-resistant regions) focusing on PTPN11, KRAS, and MAPK1. Among these genes, only PTPN11 in the immune-sensitive area exhibits gradual transcriptional changes, whereas KRAS and MAPK1 in the sensitive region — and all three genes in the resistant region — display sharp, stepwise shifts in transcription rates. These discontinuous dynamics pose a major challenge for conventional RNA velocity models, which typically assume smooth or time-invariant transcriptional kinetics.

Single-cell RNA sequencing offers unprecedented resolution of cellular states but captures only a static snapshot, limiting its ability to capture dynamic biological processes. RNA velocity addresses this gap by inferring short-term transcriptional kinetics from unspliced and spliced mRNA counts, enabling the inference of future cell states. Despite significant methodological progress, current approaches remain constrained by simplified assumptions, such as independent gene-wise kinetics and a heavy reliance on nearest-neighbor smoothing. These limitations reduce both accuracy and interpretability, particularly in complex developmental systems.
To illustrate the limitations, we benchmarked models on two well-characterized datasets: mouse gastrulation erythroid lineage and mouse dentate gyrus. These datasets are widely adopted as benchmarks because they are both biologically well-characterized and challenging for accurate velocity inference. To further explore the challenges and benchmark RNA velocity model performance on complex tumor microenvironment, we simulated 4,000 CD8⁺ T cells, with 2,000 from the immune‑sensitive area and 2,000 from the immune‑resistant area, focusing on PTPN11, KRAS, and MAPK1. Among the three genes across both areas, only PTPN11 in the immune-sensitive area shows non-stepwise transcription; KRAS and MAPK1 in the sensitive area, and all three genes in the resistant area, display clear stepwise changes in transcription rates, which are difficult for conventional RNA velocity models to capture.

![Image text](https://github.com/luoyuanlab/rna_velocity/blob/main/img_folder/Figure%201.png)
