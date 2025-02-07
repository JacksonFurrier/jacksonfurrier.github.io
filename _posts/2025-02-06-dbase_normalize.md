---
layout: distill
title: Mathematical generation of normal data for evaluating myocardial perfusion studies
description: Generating normal databases from non-healthy patients
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
  - name: Bela Kari
    url: "https://semmelweis.hu/telefonkonyv/?emp_id=7846"
    affiliations:
      name: SOTE, Budapest

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
Single-Photon Emission Computed Tomography (SPECT) protocols for left ventricular assessment play a crucial role in detecting ischemia in high-risk patients. To quantitatively evaluate myocardial function, clinicians rely on commercially available solutions for segmenting and reorienting the left ventricle (LV). These solutions are developed using extensive normal datasets, however this approach is having many drawbacks

* Whenever a new aperture is being developed a new normal database has to be created to get good quantitative evaluations
* Normal database establishment carries a high cost and time consuming slowing down the development iteration time of collimators
* Clinics often screen patients with suspectible cardiac deficiency and rarely healthy individuals, making the creation of normal databases extra work
* The size of these datasets are fixed and normalized, which might leave out important samples from the distribution

One idea of Kari and Partos to create normal datasets based on badly conditioned cardiac data using only the "normal" subsets of these samples. A mathematical method was developed that synthesizes normal data sets for quantification of regional myocardium perfusion. In clinical practice, regional myocardial perfusion is often measured with a gamma camera and quantified via circumferential profile analysis. Normal reference profile data is used to increase the accuracy of the clinical interpretations. The goal here is to create reference data from an existing set of archived studies. An iterative mathematical method, based on two statistical hypotheses, was used to generate the study set instead of collecting normal examinations from a healthy population.

---

## Task

Develop a method based on [1], [2] which can generate normal data from a reference dataset of ill-conditioned patients.

---

## References

[1] [Mathematical generation of normal data for evaluating myocardial perfusion studies](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=1175084&casa_token=YDjkMXjuuUgAAAAA:V-1R4nhJLftTOlbcZwyMXq9BCxbanE9vAN7ub3sZUx4yyxrVxyS0tT0SjUxWSkn75PHHSMHNabhVqw), Marianna et. al.

[2] Osszehasonlito adatok eloallitasa bull's-eye kepek ertekelesehez, Mate et. a.

---

## Contact

szaqaei@inf.elte.hu, kari.bela@semmelweis.hu