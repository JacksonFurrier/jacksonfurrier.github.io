---
layout: distill
title: MPI SPECT left ventricle modelling with flow-matching
description: Shape manifold representation learning
tags: distill formatting
giscus_comments: true
date: 2025-02-06
featured: true
mermaid:
  enabled: true
  zoomable: true
code_diff: true
map: true
chart:
  chartjs: true
  echarts: true
  vega_lite: true
tikzjax: true
typograms: true

authors:
  - name: Adam Istvan szucs
    url: "jacksonfurrier.github.io"
    affiliations:
      name: ELTE, Budapest

bibliography: 2018-12-22-distill.bib

# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }
---

## Topic

Single-Photon Emission Computed Tomography (SPECT) left ventricular assessment protocols are important for detecting ischemia in high-risk patients. To quantitatively measure myocardial function, clinicians depend on commercially available solutions to segment and reorient the left ventricle (LV) for evaluation. Based on large normal datasets, the segmentation performance and the high price of these solutions can hinder the availability of reliable and precise localization of the LV delineation. To overcome the aforementioned shortcomings this project aims to give a recipe for diagnostic centers as well as for clinics to automatically segment the myocardium based on small and low-quality labels on reconstructed SPECT, complete field-of-view (FOV) volumes.

The way this approach works as compared to the [self-supervised learning approach](https://jacksonfurrier.github.io/blog/2025/seg_ssl_fs_vit/) is that we first try to understand the shape of the left ventricle during the myocardial perfusin imaging (MPI) SPECT protocol. As in [1] we built a feature space, based on the kernel embedding in [reproducing kernel Hilbert space (RKHS)](https://en.wikipedia.org/wiki/Reproducing_kernel_Hilbert_space). Constructing the space we assumed a simplistic model, which was a square root function rotated around the x-axis giving us the 3 dimensional surface of the left ventricle. The base model was as simple as it could be, having only hyperparameters controlling the septal, endo and epicardial surfaces of the mycoardial volume. After constructing the distribution of our left ventricular shapes we embedded them with the Wasserstein-2 kernel [4](Sinkhorn-divergence based one) in the higher dimensional RKHS. During the running of the segmentation we connected the original and the latent space with a [Mahalanobis-type distance](https://en.wikipedia.org/wiki/Mahalanobis_distance) to sample the feature space during segmentation, ultimately convering the problem into a [density estimation problem](https://en.wikipedia.org/wiki/Density_estimation). The basic building blocks were following the footsteps of [2], [3], [5], [6]. Now as per the results, the shape prior was able to describe a well diversified 80 patient dataset, however we would like to push this further and see if we can understand the manifold of distribution of the left ventricular shapes.

To overcome the limit in expressability of RKHS-es we plan to investigate [flow matching](https://mlg.eng.cam.ac.uk/blog/2024/01/20/flow-matching.html) to get a better insight into the left ventricular shape distribution. 

---

## Task

Develop a flow matching based solution to describe the shapes of the left ventricles more accurately. Compare the method to the RKHS based solution and prove enhancement. 

---

## References

[1] Myocardial perfusion imaging SPECT left ventricle segmentation with graphs, Adam et. al.

[2] [Shape statistics in kernel space for variational image segmentation](https://www.sciencedirect.com/science/article/pii/S0031320303000566?casa_token=_OYwvXehkoIAAAAA:90b5a76xe47mkEWeIDckKGlsB6y5NwFX7SHFfinKNxNdXf7C1YvlyfkKJzhB_5gr0ZGKgWPWnKE), Daniel et. al.

[3] [Kernel pca Pattern Reconstruction via Approximate Pre-Images](https://link.springer.com/chapter/10.1007/978-1-4471-1599-1_18), Bernhard et. al.

[4] [Wasserstein exponential kernels](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9207630&casa_token=qLFvaMf3MTUAAAAA:NTFR70AIIl5NA3BhQTkIJcA5mQ_Y4x1LTaK-9s1d_qI4VHjQK6jNWAyPcaTcjga-LguyH2BoQ-K_Gw), Henri et. al.

[5] [Diffusion Snakes: Introducing Statistical Shape Knowledge into the Mumford-Shah Functional](https://link.springer.com/content/pdf/10.1023/A:1020826424915.pdf), Daniel et. al.

[6] [Nonlinear Shape Statistics in Mumford–Shah Based Segmentation](https://ipa.iwr.uni-heidelberg.de/ipabib/Papers/Cremers_Kohlberger_Schnoerr:Nonlinear_Shape_Statistics_in_Mumford-Shah_Based_Segmentation.pdf), Daniel et. al.

[7] [Flow Matching for Generative Modeling](https://arxiv.org/abs/2210.02747), Yaron et. al.

---

## Contact

szaqaei@inf.elte.hu