---
layout: distill
title: Motion correction of Multi-pinhole (MPH) projection frames with metamorphosis
description: Non-linear and projective geometry based motion detection and correction
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

Various functional imaging cameras are specialized to acquire the biochemical processes in a time and space-dependent way of different organs in-vivo. The main properties of functional imaging are relatively low resolution and high sensitivity to be manifested in multiple collimation and detection strategies. As a result, the projection geometry in each multi-vendor camera has large variability, making the inherent and acquired imaging artifacts hard to handle by algorithms. 

We seek a method, which overcomes one of the biggest effects of acquired imperfection, the patient’s motion which interferes with the heart’s motion. It is well known that, the different motion influences may alter the crucial quantitative measures. These are rendered as the main important issues of functional imaging. Solutions exist by multiple commercial approaches already, but only for specific collimation geometries. This motivation inspired the development of an automatic optimization method to overcome the above-mentioned motion artifact with general collimation geometry on the complete detector field-of-view (FOV). 

The theory (geo mc) is based on a metamorphic control problem with Optimal Transport (OT) augmentation to overcome the problems introduced by the acquired artifacts and intrinsic imaging system. The algorithm is designed on multi-pinhole (MPH) and low energy high resolution (LEHR) collimation with promising a great improvement over Optial Flow (OF) methods. The aim is to further lower the error in total perfusion deficit (TPD) scores for practical ability to apply on the patient Single-Photon Emission Computed Tomography (SPECT) studies as well.

---

## Task

Develop the [technique](https://github.com/JacksonFurrier/ieee_bibm_2024_code) further, based on [1], [2] to get better results on MPH apertures with motion phenomena.

---

## References

[1] [Projection geometry invariant nonrigid motion correction](http://dx.doi.org/10.1109/BIBM62325.2024.10822170), Adam et. al.

[2] [Automated non-linear motion detection and estimation for MPI SPECT](http://dx.doi.org/10.1109/GPMC48183.2019.9106957), Adam et. al.

---

## Contact

szaqaei@inf.elte.hu