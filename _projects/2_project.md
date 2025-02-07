---
layout: distill
title: Protein representation learning for regenerative medicine
description: A deep learning approach to help the development of regenerative medicine for heart disease
img: assets/img/proj_protein.jpg
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

The immune response triggered by infection can cause significantly different tissue damage. To successfully develop effective post-treatment methodologies for serious health-related tissue issues, a high level of cooperation is necessary.

To treat and heal vital organ damage, it is essential to identify the optimal combination of diagnostic protocols (multi-modality) for the most accurate evaluation. Among the vital tissues, the myocardial area of the heart is crucial, as it ensures proper blood circulation through contraction. To locate areas affected by low perfusion, we are developing AI-based methods for modern multi-modality SPECT/CT procedures. The goal is to create a methodology capable of precisely identifying problematic areas in anatomical CT imaging to facilitate optimal cell regeneration procedures.

After identifying the tissue area to be improved, the next step is to deliver the appropriate regenerative method—whether a specific cell family or meta-tissue—to the target area. It is necessary to investigate the applicability of modern methods such as cell ionization and robotic catheters. Continuous monitoring of the target area's vitality is crucial using advanced imaging techniques, which require the development of AI-based methods capable of recognizing diverse image characteristics with high efficiency. To establish the necessary initial database and network architecture for solving this problem, several preclinical studies are planned during the research development project. Following the establishment of validated and functional preclinical methods, we will proceed with optimizing localization procedures and AI-based optimization.

## Cardiological alterations in acute post-infection patients
As a result of infection, severe cases may lead to a hyper-inflammatory state, causing secondary organ inflammation (heart, liver, brain) and subsequent damage.

Tissue damage can generally be classified into two categories: significant cardiac strain due to acute pneumonia and secondary inflammatory diseases such as myocarditis. The latter often leads to chronic damage, measurable through various quantitative indicators. The most severe consequences include arrhythmia, coronary artery syndromes, and increased lymphocyte and T-cell destruction. Damage beyond the left ventricular myocardial region can also cause pulmonary embolism, potentially leading to right ventricular failure.

## Methods for tissue regeneration
One approach is tissue engineering, where the physical, chemical, and biological environment surrounding a cell population is managed. This field utilizes embryonic stem cells, bone marrow-derived mesenchymal stem cells, and umbilical cord-derived mesenchymal stem cells for deriving cell populations. The challenge lies in creating a scaffold system that is personalized and enhances the growth factor of implanted cells while avoiding drastic immunogenicity in the body. These techniques involve laser sintering, supercritical carbon dioxide processing, growth factor incorporation and zoning, plasma modification of scaffold surfaces, and the combination of new, reusable, temperature-sensitive injectable materials. Due to quality control difficulties caused by complex material physical properties, constructing flexible and elastic tissue scaffolds is a complex process, making their application more challenging.

Another approach is based on harnessing the regenerative capabilities of the human body by activating the self-renewing and differentiating properties of resident stem cells. To restore damaged tissues and regenerate functional organs, scientific research in regenerative medicine aims to uncover the molecular mechanisms through which stem cell regenerative potential can be translated into clinical applications. The goal is to identify and apply natural molecules in human tissues that have been revealed as evolutionary patterns in regenerating organisms. This potential has been demonstrated through physical energies such as electromagnetic fields and the mechanical vibrations of human adult stem cells. Scientific studies on stem cell modulation confirm the possibility of chemically manipulating stem cell fate in vitro, opening the way for the use of natural molecules, electromagnetic fields, and mechanical vibrations. Human stem cells can be targeted internally, enhancing the body's natural self-healing abilities. The current limitation of stem cell applications is that they can differentiate into any type of cell—including cancerous ones—and in cardiological applications, they have caused arrhythmia and other circulatory symptoms in several cases.

Certain negative effects and properties of stem cell methods may be influenced by the modified mRNA technology used in COVID-19 vaccine research. The common foundation of these methods is single-stranded ribonucleic acid (RNA), which can transmit hereditary genetic information from the DNA molecules storing cellular information to the ribosomes for protein synthesis. In eukaryotic cells, mRNA undergoes significant modifications before reaching the cytoplasm. Upon entry, proteins are synthesized based on the ACGU sequence, enabling the immune system to direct a specific type of cell to the appropriate area. This type of cell programming technique could fundamentally advance regenerative medicine.

This approach enables the control of cellular processes at the cellular level and the ability to directly manage cells. The latest developments in in vitro transcribed (IVT) mRNA technology, through chemical modifications, have led to methods that regulate spatial and temporal gene expression. The development of a safe, integration-free approach to gene therapy is aimed at translational applications. In RNA-based methods, the primary challenge is not modeling the information but delivering it into the cellular compartment. This is due to RNA's instability—it typically begins degrading immediately after synthesis—and the body's ability to break down RNA chains with specific enzymes. However, this allows for increased efficiency in tissue engineering scaffolds, such as when using hydrogel scaffolds.

The application of this method carries simulation and optimization potential, already explored in analyzing the transformative potential of new mRNA formulations. Research has examined the initiation of controlled genetic manipulation embedded in hydrogels for in vitro and in vivo tissue and organ regeneration. Notably, the role of mRNA delivery in vascularization, cytoprotection, and Cas9-mediated xenotransplantation was highlighted. Coordinating interactions between mRNA delivery carriers and polymer scaffolds can be used to introduce genetic signals that lead to stem cell reprogramming, differentiation, and precise regulation of secretome activity, which is a critical target in tissue engineering.

In these processes, the most critical factor was delivering mRNA with sufficient stability into the appropriate cell. Beyond numerous biophysical characteristics, one of the most decisive factors is the geometry of the material encapsulating the mRNA and the properly encoded information within the mRNA itself. High-efficiency computational analyses enable rapid testing and development iterations to find an optimal delivery mechanism.

The claims are supported by the application of human VEGF-A encoded in mRNA, where successful improvement in myocardial condition was achieved through targeted injection into the heart muscle. Studies in various small animal models generally demonstrated an improvement in ejection fraction (EF) of around 5-6%, which can be significant in critical cases. Additionally, one study successfully restored microcirculation in a necrotic area.

Measuring the effectiveness of therapy in the heart is a crucial question. In most studies, the effectiveness of improvement was measured using MRI and CT imaging modalities and their derived quantitative parameters. These modalities are typically outstanding in either specificity or sensitivity. Hybrid imaging techniques are necessary to properly examine the processes occurring as a result of or during treatment. Detailed tissue information requires nuclear medicine methods that can be effectively combined with anatomical modalities such as CT.

To achieve adequate effectiveness, the barriers to applying modRNA methods must be overcome. Published studies have shown that modRNA therapy improves outcomes after myocardial infarction. However, poorly defined delivery systems have hindered the transition of research to the clinic. Currently, intracardiac injection is the most effective method for delivering genes to the heart. Direct gene penetration into the myocardium, however, causes stress and local tissue damage. Therefore, there is a real need to develop efficient mRNA delivery systems that ensure targeted, non-invasive gene transfer into the heart. Interest is growing in cell-penetrating peptides (CPPs), which can be used alongside modRNA to ensure its targeted delivery. Recent studies have supported the application of CPPs for delivering small interfering RNA (siRNA) to inhibit target gene expression in cancer cells. mRNA transfection can also be efficiently mediated by RNA aptamers, which bind to specific cell markers and can be modified for tissue targeting. Optimizing consistent dosing is essential for both myocardial tissue and patients receiving modRNA therapy. Both the controlled modRNA release into the cytoplasm following endocytosis and the dose-protein effect relationship must be considered before modRNA can be implemented in heart therapy.

## Tasks

The main goal is to design and develop a protein representation learning technique so we can better understand how mRNA VEGF-based solutions would work in post infection cause scar tissue regeneration and/or avoiding scar tissue formation in these scenarios. The method shall be developed on the ideas of [18] and further enhanced to get better predictions and facilitate large database learning on, e.g.: [Cx43, GJA1](https://en.wikipedia.org/wiki/GJA1) proteins to understand inflammation signalling pathways. 


## References

[1] Adrienn Borsy  et al., Identifying novel genes involved in both deer physiological and human pathological osteoporosis, Mol Genet Genomics (2009), vol 281, pages 301-313, DOI: 10.1007/s00438-008-0413-7

[2] A.Akhmerov  et al., COVID-19 and the Heart, Circulation Research (2020) p. 1443-1455, DOI: 10.1161/CIRCRESAHA.120.317055

[3] Abdallah Fayssoil et al., The Right Ventricle in COVID-19 Patients, Am J Cardiol (2020), vol. 130, pages 166-167, DOI: 10.1016/j.amjcard.2020.06.007

[4] Bernadett Balla et al., Different Gene Expression Patterns in the Bone Tissue of Aging Postmenopausal Osteoporotic and Non-osteoporotic Women, Calcif Tissue Int (2008), vol. 82, pages 12-26, DOI: 10.1007/s00223-007-9092-3

[5] Viktor Stéger et al., Antler development and coupled osteoporosis in the skeleton of red deer Cervus elaphus: expression dynamics for regulatory and effector genes, Mol Genet Genomics (2010), vol. 284, pages 273-287, DOI: 10.1007/s00438-010-0565-0

[6] D. Howard et al., Tissue engineering: strategies, stem cells and scaffolds,  Journal of Anatomy (2008) vol. 213, iss. 1, p. 66-72, DOI: 10.1111/j.1469-7580.2008.00878.x

[7] F. Facchin et al., Tissue Regeneration without Stem Cell Transplantation: Self-Healing Potential from Ancestral Chemistry and Physical Energies, Stem cell international (2018), DOI: 10.1155/2018/7412035

[8] Siddhart Patel et al., Messenger RNA Delivery for Tissue Engineering and Regenerative Medicine Applications, Tissue Engineering - Part A (2019), vol. 25, iss. 1-2, p. 91-112, DOI: 10.1089/ten.tea.2017.0444

[9] István Gyurján Jr. et al., Gene expression dynamics in deer antler: mesenchymal differentiation toward chondrogenesis, Mol Genet Genomics (2007), vol. 277, pages 221-235, DOI:10.1007/s00438-006-0190-0

[10] Lior Zangi et al., Modified mRNA directs the fate of heart progenitor cells and induces vascular regeneration after myocardial infarction, Nature Biotechnology (2013), vol. 31, iss. 10, p. 898-907, DOI: 10.1038/nbt.2682

[11] L. Carlsson et al., Biocompatible, Purified VEGF-A mRNA Improves Cardiac Function after Intracardiac Injection 1 Week Post-myocardial Infarction in Swine,  Molecular Therapy - Methods and Clinical Development (2018), vol. 9, iss. June, p. 330-346, DOI: 10.1016/j.omtm.2018.04.003

[12] K. Kaur et al., Modified mRNA as a Therapeutic Tool for the Heart,  Cardiovascular Drugs and Therapy, Cardiovascular Drugs and Therapy (2020), vol. 34, iss. 6, p. 871-880, DOI: 10.1007/s10557-020-07051-4

[13] Kathrin L.et al., Combinatorial optimization of mRNA structure, stability, and translation for
RNA-based therapeutics, preprint, bioRxiv(2021) 

[14] Siu Kwan Lam et. al, Numba: a LLVM-based Python JIT compiler, LLVM '15: Proceedings of the Second Workshop on the LLVM Compiler Infrastructure in HPC(2015), Article No. 7, Pages 1-6, https://doi.org/10.1145/2833157.2833162 

[15] He Zhang et al., LinearDesign: Efficient Algorithms for Optimized mRNA Sequence Design, preprint, arXiv(2020)

[16] Gang Liu et. al, Module-based multiscale simulation of angiogenesis in skeletal muscle, Theoretical and Medical Modelling(2011), vol. 8 iss 6, DOI: 10.1186/1742-4682-8-6

[17] Mark James Abraham et. al, GROMACS: High performance molecular simulations through multi-level
parallelism from laptops to supercomputers, Software X(2015), pages 19-25, http://dx.doi.org/10.1016/j.softx.2015.06.001

[18] [Clustering for Protein Representation Learning](https://openaccess.thecvf.com/content/CVPR2024/papers/Quan_Clustering_for_Protein_Representation_Learning_CVPR_2024_paper.pdf), Quan et. al.


## Contact
szaqaei@inf.elte.hu