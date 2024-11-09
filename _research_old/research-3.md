---
title: "Decomposing the subclonal structure of tumors with two-way mixture models on copy number aberrations"
excerpt: <img src='https://an-shun-tai.github.io/anshun.tai/images/research_work3.png'>
collection: research
---

## Abstract:
### Motivation: 
Multistage tumorigenesis is a dynamic process characterized by the accumulation of mutations. Thus, a tumor mass is composed of genetically divergent cell subclones. With the advancement of next-generation sequencing (NGS), mathematical models have been recently developed to de-mix tumor subclonal architecture among single-nucleotide variants (SNVs) from DNA sequencing data. However, somatic copy number aberrations (CNAs) also play critical roles in carcinogenesis. Therefore, further modeling subclonal CNAs composition would hold the promise to improve the analysis of tumor heterogeneity and cancer evolution.

### Results: 
We developed a **two-way mixture Poisson model**, named CloneDeMix, for the deconvolution of read-depth information and inferred the subclonal copy number of each target region, mutational cellular prevalence (MCP), subclone composition, and the order in which mutations occurred in the evolutionary hierarchy. The performance of CloneDeMix was systematically assessed in simulations. Furthermore, we also demonstrated its applicability using head and neck cancer samples from TCGA. Our results inform about the extent of subclonal CNA diversity, and a group of candidate genes that probably initiate lymph node metastasis during tumor evolution was also discovered. Most importantly, these driver genes located at 11q13.3 which is highly susceptible to copy number change in head and neck cancer genomes. Briefly, this framework has implications for improved modeling of tumor evolution and the importance of inclusion of subclonal CNAs.

### Availability and Implementation:
The CloneDeMix R package is available at [https://github.com/AshTai/CloneDeMix](https://github.com/AshTai/CloneDeMix).

![Research Work](https://an-shun-tai.github.io/anshun.tai/images/research_work3.png)

