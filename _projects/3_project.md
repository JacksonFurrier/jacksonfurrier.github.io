---
layout: distill
title: Monte Carlo based reconstruction for dynamic acquisitions in SPECT
description: Aiming for absolute perfusion in myocardial dynamic studies
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
  - name: Adam Istvan Szucs
    url: "jacksonfurrier.github.io"
    affiliations:
      name: ELTE, Budapest
  - name: Bela Kari
    url: "https://semmelweis.hu/telefonkonyv/?emp_id=7846"
    affiliations:
      name: SOTE, Budapest
bibliography: 3_project.bib

---

## Introduction

The main theory behind reconstruction methods are the [inverse problems](https://en.wikipedia.org/wiki/Inverse_problem), which can be described as how one can calculate the casual factors from a set of observed samples. This methodology of going backwards or in inverse path from the measured quantities to the original distribution of some phenomena, called reconstruction. 

The main focus here is on Single-photon emission computed tomography (SPECT), where the data and the reconstruction methods, so do the optimization techniques are aimed to exploit the Poisson nature of the gamma photon detection in these systems. For a mathematically more elaborate discussion, please take a look at [spect data modelling](https://jacksonfurrier.github.io/models_nuclear_cardiology/topics/e_spect_data_math.html).

The main problem during SPECT reconstruction is that there are many new methodologies developed since the [filtered back projection](https://en.wikipedia.org/wiki/Tomographic_reconstruction) in terms of acquisition and multi modality based enhancements. One of the well known addition is the [attenuation correction](https://www.digirad.com/understanding-attenuation-correction/), which is computed based on the $\mu$ map of the low-dose CT during the acuqisition to help correct the attenuated gamma-photons to be "recalculated". To have a flexible optimization method in incorporating the attenuation correction and forward and back projection formulas, iterative reconstruction methods have been developed <d-cite key="shepp2007maximum"></d-cite> named as MLEM, further enhancement have been done by <d-cite key="hudson1994accelerated"></d-cite> named OSEM.

The main problem however, with this MLEM-based approach is the forward and back projection methods, which have to be developed in a physically accurate manner. The best way is to utilize [monte carlo simulation](https://en.wikipedia.org/wiki/Monte_Carlo_method) to simulate the gamma photon traversal inside the body and the collimator as well <d-cite key="lux2018monte"></d-cite> and the [oftankonyv](http://oftankonyv.reak.bme.hu/).

---

## Task

Develop a `CUDA` based monte carlo projector with the utilization of pytorch. 

---


## Background materials

To understand the different parts of this complex approach one needs to master the following materials

1. The book on photon transport <d-cite key="lux2018monte"></d-cite> with a focus on variance reduction techniques, these are mostly for the transport simulation
2. Convex optimization by Boyd <d-cite key="boyd2004convex"></d-cite> is must have for the optimization part of the algorithm
3. [CUDA programming](https://docs.nvidia.com/cuda/cuda-c-programming-guide/) by nvidia, a good reference will give you an idea about the hardware and the language constructs to program GPUs (in this time only by using CUDA)

---

## Contact

szaqaei@inf.elte.hu, kari.bela@semmelweis.hu

