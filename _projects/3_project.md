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

The main theory behind reconstruction methods are the [inverse problems](https://en.wikipedia.org/wiki/Inverse_problem), which can be described as how one can calculate the casual factors from a set of observed samples. This methodology of going backwards or in inverse path from the measured quantities to the original distribution of some phenomena, called reconstruction. 

The main focus here is on Single-photon emission computed tomography (SPECT), where the data and the reconstruction methods, so do the optimization techniques are aimed to exploit the Poisson nature of the gamma photon detection in these systems. For a mathematically more elaborate discussion, please take a look at [spect data modelling](https://jacksonfurrier.github.io/models_nuclear_cardiology/topics/e_spect_data_math.html).

The main problem during SPECT reconstruction is that there are many new methodologies developed since the [filtered back projection](https://en.wikipedia.org/wiki/Tomographic_reconstruction) in terms of acquisition and multi modality based enhancements. One of the well known addition is the [attenuation correction](https://www.digirad.com/understanding-attenuation-correction/), which is computed based on the $\mu$ map of the low-dose CT during the acuqisition to help correct the attenuated gamma-photons to be "recalculated". To have a flexible optimization method in incorporating the attenuation correction and forward and back projection formulas, iterative reconstruction methods have been developed [1]. 

The main problem however, with this MLEM approach is the forward and back projection methods, which have to be developed in a physically accurate manner. The best way is to utilize [monte carlo simulation](https://en.wikipedia.org/wiki/Monte_Carlo_method) to simulate the gamma photon traversal inside the body and the collimator as well [2] [3] .

---

## Task

Develop a `CUDA` based monte carlo projector for the MPH-73 collimator with the utilization of pytorch. 

---

## References

[1] [Maximum likelihood reconstruction for emission tomography](https://ieeexplore.ieee.org/iel5/42/4307552/04307558.pdf?casa_token=BdryRstdcCMAAAAA:GXsmArkUiNEOtPP_jc7MF8WP2256UCSjz8mF10wCJFKQ9Q40IJA6MZonwn5P8Hv8G7DsAbg1aisQ), Schepp et. al.

[2] [Monte Carlo Particle Transport Methods](https://www.taylorfrancis.com/books/mono/10.1201/9781351074834/monte-carlo-particle-transport-methods-lux), Ivan L. et. al.

[3] [Oftankonyv](http://oftankonyv.reak.bme.hu/), Kari et. al.

---

## Contact

szaqaei@inf.elte.hu, kari.bela@semmelweis.hu

