---
layout: distill
title: Monte Carlo based reconstruction for Multi-pinhole apertures and dynamic acquisitions
description: Aiming for absolute perfusion in myocardial dynamic studies with 3-headed MPH cameras
img: assets/img/proj_mc_rec.jpg
importance: 1
category: work
giscus_comments: true
tags: distill formatting
giscus_comments: false
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

## Introduction

The main theory behind reconstruction methods are the [inverse problems](https://en.wikipedia.org/wiki/Inverse_problem), which can be described as how one can calculate the casual factors from a set of observed samples. This methodology of going backwards or in inverse path from the measured quantities to the original distribution of some phenomena called reconstruction. 

The main focus here is on Single-photon emission computed tomography (SPECT), where the data and the reconstruction methods, so do the optimization techniques are aimed to exploit the Poisson nature of the gamma photon detection in these systems. For a mathematically more elaborate discussion, please take a look at [spect data modelling](https://jacksonfurrier.github.io/models_nuclear_cardiology/topics/e_spect_data_math.html).

---

## Task

TODO

---

## References

[1] [Monte Carlo Particle Transport Methods](https://www.taylorfrancis.com/books/mono/10.1201/9781351074834/monte-carlo-particle-transport-methods-lux), Ivan L. et. al.


---

## Contact

szaqaei@inf.elte.hu

