---
layout: distill
title: Optimization methods in left ventricle segmentation
description: Classical optimization methods in left ventricle segmentation
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

bibliography: 1_project_seg_optim.bib

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

Image segmentation is a day-to-day task of clinical practitioners to carry out volume/area/surface specific quantities of a region of interest (ROI). In most cases this task can be challenging and too long to solve (multiple hours/half an hour), therefore some level of automation is needed.

There are many segmentation methodologies based on different theories, but in most of the cases these are not applied in the practice due to the unacceptable running times. Besides deep-learning the graph-based algorithms are actively being researched and developed. <d-cite key="grady2006isoperimetric"></d-cite> The data being volumetric (3D scalar field) it can be represented as a large graph with nodes being voxels and edges being the connection between neighboring (e.g. 6 neighboring cubes) voxels. With this abstraction, a segmentation task can be thought as a graph partitioning/slicing method to find the desired ROI (e.g. a liver in a CT dataset, thyroids in a SPECT dataset).

The graph-based algorithms are often developed in hand with variational image segmentation methods to define an energy which can be minimized on the graph. Sometimes this approach can lead to long running times and complicated optimization tactics. A different approach was introduced in <d-cite key="grady2006fast"></d-cite> to overcome the drawbacks of the latter. The method is fast and accurate in the segmentation task with a simple isoperimetric cost function. Even though it is fast and accurate solving the isoperimetric problem for instance in most cases this wont suffice (e.g.: full body bone segmentation)

Problem with graph-based methods is metrication bias, which renders as low resolution or high computation times. To overcome the aforementioned problem, a continuous optimization <d-cite key="yuan2010study"></d-cite>, <d-cite key="sun2020efficient"></d-cite> can be applied to handle the discrete resolution of graph-based methods. The continuous max-flow (CMF) method is very accurate in classification problems.

## Task

Investigate and develop a technique based-on CMF method with shape priors to handle the “few-shot” learning with classical methods. Compare the current method to the competing ones (given by the topic supervisor). Investigate shape descriptors in a statistical setting and compare it to self-supervised methods.

## Background materials

To understand the different parts of this complex approach one needs to master the following materials

0. Get a good understanding of python with numpy, the brief introduction is written at [numpy for matlab programmers](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html). Numpy and pytorch are quite similar, for a hands on tutorial consult [pytorch intro](https://pytorch.org/tutorials/beginner/basics/intro.html)
1. Convex optimization by Boyd <d-cite key="boyd2004convex"></d-cite> is must have for the optimization part of the algorithm
2. Calculus of variations basics <d-cite key="gelfand2000calculus"></d-cite>

## Contact

szaqaei@inf.elte.hu