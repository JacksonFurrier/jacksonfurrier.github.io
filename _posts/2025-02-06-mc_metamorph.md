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
  - name: Adam Istvan Szucs
    url: "jacksonfurrier.github.io"
    affiliations:
      name: ELTE, Budapest

bibliography: 1_project_mc.bib

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

## Task

Develop the [technique](https://github.com/JacksonFurrier/ieee_bibm_2024_code) further, based on <d-cite key="szHucs2024projection"></d-cite>, <d-cite key="szHucs2019automated"></d-cite> to get better results on MPH apertures with motion phenomena.

## Background materials

To understand the different parts of this complex approach one needs to master the following materials

0. Get a good understanding of python with numpy, the brief introduction is written at [numpy for matlab programmers](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html). Numpy and pytorch are quite similar, for a hands on tutorial consult [pytorch intro](https://pytorch.org/tutorials/beginner/basics/intro.html)
1. Get a good understanding of LDDMM based on the book <d-cite key="younes2010shapes"></d-cite> and further read the Hamiltonian formalism <d-cite key="miller2015hamiltonian"></d-cite>
2. Understand the difference between the *Lagrangian* vs *Hamiltonian*, try to approach it from a *Calculus of Variations* point of view

## Contact

szaqaei@inf.elte.hu