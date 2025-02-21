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
  - name: Adam Istvan Szucs
    url: "jacksonfurrier.github.io"
    affiliations:
      name: ELTE, Budapest

bibliography: 2_project.bib

---

## Introduction

The immune response triggered by infection can lead to significantly different types of tissue damage. A high level of collaboration is necessary to successfully develop methodologies for the post-treatment of serious health-related tissue problems.

To treat and heal damage to vital organs, it is essential to explore the appropriate combination of diagnostic protocols (multi-modality) for the most accurate evaluation. Among vital tissues, the myocardial area of the heart stands out, which is responsible for pumping blood throughout the body with proper contraction. The testing of cardiac scar tissue or prefunded areas will be completed by running myocardial perfusion imaging (MPI) SPECT/CT scans to detect and then later check the affected areas in the left/right ventricle.

After localizing the area where improvements are required at the tissue level, the most important aspect is to deliver the appropriate regenerative method—cell family or meta-tissue—to the target area. It is necessary to investigate the applicability of modern procedures such as cell ionization and robotic catheters. Continuous monitoring of target area vitality must be conducted alongside already developed imaging procedures, hence the aim to develop artificial intelligence-based methods capable of efficiently recognizing imaging information characterized by different attributes—varying noise and geometry. A series of preclinical studies are planned during the course of the research development project to establish the initial database and network architecture necessary for solving the problem. After establishing validated and operational preclinical methods, the next step will involve finding the appropriate localization procedure and optimizing it with artificial intelligence.


## Cardiological alterations in acute post-infection patients

The infectous disease can lead to hyper-inflammatory states in more severe phases, which can cause inflammation and subsequent damage to secondary organs—such as the heart, liver, and brain. The types of damage can primarily be classified into two categories. More significant cardiovascular strain often arises from acute pneumonia, or it can stem from myocarditis, which develops due to secondary inflammatory disease. A large proportion of lasting damage is caused by the latter inflammatory reaction, which can be implicitly measured when examining numerous quantitative values. The most severe consequences are arrhythmia, coronary artery syndrome, and increased destruction of lymphocytes and T-cells. Damage can also extend beyond the left ventricular myocardial area, potentially causing pulmonary embolism, leading to right ventricular failure.


## Methods for tissue regeneration

Tissue regeneration methods are diverse and possess different regeneration and treatment characteristics.  

One approach is tissue engineering, which manages the physical, chemical, and biological environment surrounding a cell population. The area includes the use of embryonic stem cells, bone marrow-derived mesenchymal stem cells, and cord-derived mesenchymal stem cells for the derivation of cell populations. The challenge lies in creating a type of scaffold that is personalized and enhances the growth factor of the implanted cells while not triggering drastic immunogenicity in the body. These techniques involve laser sintering, supercritical carbon dioxide processing, incorporation and zoning of growth factors, plasma modification of scaffold surfaces, and the combination of new, reusable, thermos-sensitive injectable materials <d-cite key="borsy2009identifying"></d-cite>. Due to the complexities of the material's physical properties, the construction of flexible and elastic tissue scaffolds is a complicated process that complicates their application.

Another approach utilizes the regenerative capabilities of the human body, where the self-renewing and differentiating properties of resident stem cells are activated to achieve regeneration. To restore damaged tissues and regenerate functional organs, scientific research in regenerative medicine is actively exploring the molecular mechanisms through which stem cells’ regenerative potentials can unfold as clinical applications <d-cite key="akhmerov2020covid"></d-cite>. The objective is to identify and apply natural molecules to human tissues that can be revealed as evolutionary patterns in the tissues of various regenerating organisms. This potential has manifested from physical energies, such as electromagnetic fields and mechanical vibrations of adult human stem cells. Scientific investigations related to stem cell modulation confirm the viability of chemical manipulation of stem cell fate in vitro, paving the way for the use of natural molecules, as well as electromagnetic fields and mechanical vibrations. Human stem cells can be targeted internally, enhancing the body's natural self-healing ability. The current limitation in using stem cells is that they can derive and diversify into any type of cell—including cancerous cells—and may produce arrhythmias and other circulatory symptoms during cardiovascular applications.

Certain negative effects and properties of stem cell methods can potentially be influenced by the modified mRNA technology used in infection vaccine research <d-cite key="shahrbaf2021right"></d-cite>. The common basis of these methods is single-stranded ribonucleic acid (mRNA), which can relay genetic information from DNA—the molecule that stores cell information—to ribosomes for protein synthesis. In eukaryotic cells, mRNA undergoes significant modifications before entering the cytoplasm. After entry, proteins are synthesized based on the ACGU sequence, enabling the immune system to target a specific type of cell to the appropriate area. This type of cell programming technique could fundamentally advance regenerative medicine. 

This approach enables the control of cellular processes and the ability to directly manage cells. Recent developments in in vitro transcribed (IVT) mRNA technology along chemical modifications have led to methods that regulate spatial and temporal gene expression. The development of a safe, integration-free approach to gene therapy is aimed at translational goals. In RNA-based methods, the challenge fundamentally lies not in modelling the information but in delivering it into the intracellular envelope. This is due to RNA's instability—generally beginning to degrade immediately after production—as well as the body's capability to degrade RNA strands using appropriate enzymes. However, this allows for increased effectiveness in tissue engineering scaffolds, such as when using hydrogel scaffolds.

The application of this method carries simulation and optimization potential that has already been examined in analyzing the transformative potential of new mRNA preparations. Research has explored the initiation of controlled genetic manipulation embedded in hydrogels for in vitro and in vivo regeneration of tissues and organs. Notably, the role of mRNA delivery has been highlighted in vascularization, cytoprotection, and Cas9-mediated xenotransplantation. The coordination of interactions between mRNA delivery carriers and polymer scaffolds can be used to present genetic signals that lead to the reprogramming, differentiation of stem cells, and precise control of secretome activity, which is critical from a tissue engineering perspective.

In these processes, the most significant aspect is the delivery of mRNA with sufficient stability to the appropriate cells. Beyond numerous biophysical features, one of the most determinative factors is the geometry of the material enveloping the mRNA and the properly encoded information within the mRNA. Computational simulations conducted on high-efficiency machines allow for rapid testing and development iterations to find a suitable delivery mechanism.

The statements are substantiated by the application of human VEGF-A encoded in mRNA, where successful improvements in the condition of the heart muscle were achieved via targeted injections into the myocardium. Various small animal models showed a general improvement in ejection fraction (EF) of around 5-6%, which can be significant in critical cases. Additionally, one study succeeded in restoring microcirculation in a dead area <d-cite key="balla2008different"></d-cite>.

Measuring the effectiveness of therapy in the heart is an important question. Most research measured improvements using MRI or CT modality devices and the quantitative metrics derivable from them. These modalities individually excel in either specificity or sensitivity. Accurate examination of the processes that occur as a result of treatment requires hybrid imaging techniques. Nuclear medicine methods that can be well combined with anatomical modalities (CT) are also necessary for detailed examination of tissue information.

To achieve the necessary effectiveness, the barriers to the application of modified RNA methods must be overcome <d-cite key="kaur2020modified"></d-cite>. Cited publications have shown that modified RNA therapy improves outcomes following myocardial infarction. However, ill-defined delivery systems have hindered the translation of the research into clinical practice. Currently, intracardiac injection is the most effective method for delivering genes into the heart. Direct penetration of genes into the myocardium causes stress and localized damage in the tissue. Therefore, there is a real need to develop efficient mRNA delivery systems that ensure targeted, non-invasive gene transfer to the heart. Interest in cell-penetrating peptides (CPPs) is increasing, which can be used alongside modified RNA to ensure its specific delivery. Recent studies have supported the application of CPPs for the delivery of small interfering RNAs to inhibit the expression of target genes in cancer cells. mRNA transfection can be effectively mediated by RNA aptamers that bind to specific cell markers and can be modified to target tissues. Consistent dosing optimization is necessary among patients receiving therapy in the myocardium and modified RNA therapy. Both controlled release of modified RNA into the cytoplasm post-endocytosis and the relationship between modified RNA dosage/protein effects must be taken into consideration before modified RNA can be practically realized in heart therapy.


## Tasks

The main goal is to design and develop a protein representation learning technique so we can better understand how mRNA VEGF-based solutions would work in post infection cause scar tissue regeneration and/or avoiding scar tissue formation in these scenarios. The method shall be developed on the ideas of <d-cite key="quan2024clustering"></d-cite> and further enhanced to get better predictions and facilitate large database learning on, e.g.: [Cx43, GJA1](https://en.wikipedia.org/wiki/GJA1) proteins to understand inflammation signalling pathways.

## Backgound materials

To understand and contribute to the project, the following materials help a lot

0. Get a good understanding of python with numpy, the brief introduction is written at [numpy for matlab programmers](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html). Numpy and pytorch are quite similar, for a hands on tutorial consult [pytorch intro](https://pytorch.org/tutorials/beginner/basics/intro.html)
1. Pytorch, the book [Deep Learning With Pytorch](https://www.manning.com/books/deep-learning-with-pytorch) is one of the best on the topic of pytorch and deep learning
2. To get a good understanding on protein folding, structure and the role of amino acids check out the book [Deep Learning for life sciences](https://www.oreilly.com/library/view/deep-learning-for/9781492039822/). Chapters 1, (2), 6, 9, (11) are interesting.
3. If one needs further knowledge on deep learning there is great introductory book Simone Scardapane, [Alice's adventures in differentiable wonderland](https://www.sscardapane.it/assets/alice/Alice_book_volume_1.pdf). This is a great approach, I strongly suggest to read it

## Contact
szaqaei@inf.elte.hu