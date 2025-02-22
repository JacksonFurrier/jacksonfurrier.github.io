---
layout: distill
title: Self-supervised few-shot learning in left ventricle segmentation
description: Problems with low labeled left ventricle segmentation in MPI SPECT
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

bibliography: 1_project_ssl.bib

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

A self-supervised learning (SSL) approach was developed in <d-cite key="szHucs2023self"></d-cite> with convolutional neural networks (CNN). The technique was based on jigsaw puzzle as a pretext task and supervision on 5 patients as fine-tuning. The method reached good performance on various metrics, however on hypoperfused myocardia it wasn’t able to get acceptable results. A way to enhance the technique is to apply methods from Vision transformers (ViT) <d-cite key="dosovitskiy2020image"></d-cite> on some parts of the architecture and training as well <d-cite key="zhu2023new"></d-cite>, <d-cite key="hatamizadeh2022unetr"></d-cite>. Furthermore the incorporation of shape information about left ventricles can raise the performance of such methods.

## Task

Develop a ViT-based SSL few-shot learning method and investigate the incorporation of shape information in the optimization process.

## Backgound materials

To understand and contribute to the project, the following materials help a lot

1. Pytorch, the book [Deep Learning With Pytorch](https://www.manning.com/books/deep-learning-with-pytorch) is one of the best on the topic of pytorch and deep learning
2. To get a good understanding on protein folding, structure and the role of amino acids check out the book [Deep Learning for life sciences](https://www.oreilly.com/library/view/deep-learning-for/9781492039822/). Chapters 1, (2), 6, 9, (11) are interesting.
3. If one needs further knowledge on deep learning there is great introductory book Simone Scardapane, [Alice's adventures in differentiable wonderland](https://www.sscardapane.it/assets/alice/Alice_book_volume_1.pdf). This is a great approach, I strongly suggest to read it


## Contact

szaqaei@inf.elte.hu