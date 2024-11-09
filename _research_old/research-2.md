---
title: "BayICE: A hierarchical Bayesian deconvolution model with stochastic search variable selection"
excerpt: <img src='https://an-shun-tai.github.io/anshun.tai/images/research_work2-1.png'>
collection: research
---

Abstract:
-----
Gene expression deconvolution is a powerful tool for exploring the microenvironment of complex tissues comprised of multiple cell groups using transcriptomic data. Characterizing cell activities for a particular condition has been regarded as a primary mission against diseases. For example, cancer immunology aims to clarify the role of the immune system in the progression and development of cancer through analyzing the immune cell components of tumors. To that end, many deconvolution methods have been proposed for inferring cell subpopulations within tissues. Nevertheless, two problems limit the practicality of current approaches. First, all approaches use external purified data to preselect cell type-specific genes that contribute to deconvolution. However, some types of cells cannot be found in purified profiles and the genes specifically over- or under-expressed in them cannot be identified. This is particularly a problem in cancer studies. Hence, a preselection strategy that is independent from deconvolution is inappropriate. The second problem is that existing approaches do not recover the expression profiles of unknown cells present in bulk tissues, which results in biased estimation of unknown cell proportions. Furthermore, it causes the shift-invariant property of deconvolution to fail, which then affects the estimation performance. To address these two problems, we propose a novel deconvolution approach, BayICE, which employs hierarchical Bayesian modeling with stochastic search variable selection. We develop a comprehensive Markov chain Monte Carlo procedure through Gibbs sampling to estimate cell proportions, gene expression profiles, and signature genes. Simulation and validation studies illustrate that BayICE outperforms existing deconvolution approaches in estimating cell proportions. Subsequently, we demonstrate an application of BayICE in the RNA sequencing ofpatients with non-small cell lung cancer. The model is implemented in the R package “BayICE” and the algorithm is available for download.

<div style="display: flex; justify-content: space-between;">
    <img src="https://an-shun-tai.github.io/anshun.tai/images/research_work2-1.png" style="width: 48%; margin-right: 1%;">
    <img src="https://an-shun-tai.github.io/anshun.tai/images/research_work2-2.png" style="width: 48%;">
</div>

Availability and Implementation: The BayICE R package is available at [https://github.com/AshTai/BayICE](https://github.com/AshTai/BayICE).
