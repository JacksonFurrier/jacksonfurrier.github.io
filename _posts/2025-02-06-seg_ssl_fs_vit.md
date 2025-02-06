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

A self-supervised learning (SSL) approach was developed in [1] with convolutional neural networks (CNN). The technique was based on jigsaw puzzle as a pretext task and supervision on 5 patients as fine-tuning. The method reached good performance on various metrics, however on hypoperfused myocardia it wasn’t able to get acceptable results. A way to enhance the technique is to apply methods from Vision transformers (ViT) on some parts of the architecture and training as well [2], [3]. Furthermore the incorporation of shape information about left ventricles can raise the performance of such methods.

---

## Task

Develop a ViT-based SSL few-shot learning method and investigate the incorporation of shape information in the optimization process.

---

## References

[1] [Self-supervised segmentation of myocardial perfusion imaging SPECT left ventricles](https://dl.acm.org/doi/pdf/10.1145/3632047.3632078), Adam et al.

[2] [A new method incorporating deep learning with shape priors for left ventricular segmentation in myocardial perfusion SPECT images](https://www.sciencedirect.com/science/article/pii/S0010482523004195?casa_token=T2dI_3cEndIAAAAA:kPV9wHN_07raKCy6hzW_5CJfFA0AjxmV9yXDoZg6o8l2Z7dKvwGKFE27_pJRpPov6sG2tjsAE-c), Fubau et al.

[3] [UNETR: Transformers for 3D Medical Image Segmentation](https://openaccess.thecvf.com/content/WACV2022/papers/Hatamizadeh_UNETR_Transformers_for_3D_Medical_Image_Segmentation_WACV_2022_paper.pdf)



---

## Contact

szaqaei@inf.elte.hu