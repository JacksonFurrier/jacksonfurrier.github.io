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
  - name: Adam Istvan Szucs
    url: "jacksonfurrier.github.io"
    affiliations:
      name: ELTE, Budapest

bibliography: 1_project_seg_shape.bib

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

The way this approach works as compared to the [self-supervised learning approach](https://jacksonfurrier.github.io/blog/2025/seg_ssl_fs_vit/) is that we first try to understand the shape of the left ventricle during the myocardial perfusin imaging (MPI) SPECT protocol. As in <d-cite key="szucs2025graph"></d-cite> we built a feature space, based on the kernel embedding in [reproducing kernel Hilbert space (RKHS)](https://en.wikipedia.org/wiki/Reproducing_kernel_Hilbert_space). Constructing the space we assumed a simplistic model, which was a square root function rotated around the x-axis giving us the 3 dimensional surface of the left ventricle. The base model was as simple as it could be, having only hyperparameters controlling the septal, endo and epicardial surfaces of the mycoardial volume. After constructing the distribution of our left ventricular shapes we embedded them with the Wasserstein-2 kernel (Sinkhorn-divergence based one) <d-cite key="de2020wasserstein"></d-cite> in the higher dimensional RKHS. During the running of the segmentation we connected the original and the latent space with a [Mahalanobis-type distance](https://en.wikipedia.org/wiki/Mahalanobis_distance) to sample the feature space during segmentation, ultimately convering the problem into a [density estimation problem](https://en.wikipedia.org/wiki/Density_estimation). The basic building blocks were following the footsteps of <d-cite key="cremers2003shape"></d-cite>, <d-cite key="scholkopf1998kernel"></d-cite>, <d-cite key="cremers2002diffusion"></d-cite>, <d-cite key="cremers2002nonlinear"></d-cite>. Now as per the results, the shape prior was able to describe a well diversified 80 patient dataset, however we would like to push this further and see if we can understand the manifold of distribution of the left ventricular shapes.

To overcome the limit in expressability of RKHS-es we plan to investigate [flow matching](https://mlg.eng.cam.ac.uk/blog/2024/01/20/flow-matching.html) to get a better insight into the left ventricular shape distribution. 

## Task

Develop a flow matching <d-cite key="lipman2022flow"></d-cite> based solution to describe the shapes of the left ventricles more accurately. Compare the method to the RKHS based solution and prove enhancement.

## Backgound materials

To understand and contribute to the project, the following materials help a lot

1. Pytorch, the book [Deep Learning With Pytorch](https://www.manning.com/books/deep-learning-with-pytorch) is one of the best on the topic of pytorch and deep learning
2. If one needs further knowledge on deep learning there is great introductory book Simone Scardapane, [Alice's adventures in differentiable wonderland](https://www.sscardapane.it/assets/alice/Alice_book_volume_1.pdf). This is a great approach, I strongly suggest to read it
3. Flow matching [tutorial](https://mlg.eng.cam.ac.uk/blog/2024/01/20/flow-matching.html) and a really good explanation by facebook research [documentation](https://facebookresearch.github.io/flow_matching/)

## Contact

szaqaei@inf.elte.hu