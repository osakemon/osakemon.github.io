---
layout: project
title: Thor & Mjolnir
description: Cell-level analysis of spatial transcriptomics and histology, with a browser-based interface for exploring gigapixel tissue images.
img: /assets/img/projects/thor_mjolnir_gene_expression_poster.jpg
importance: 2
category: work
venue: Nature Communications, 2025
role: Co-first author
github: https://github.com/GuangyuWangLab2021/Thor
links:
  - label: Paper
    url: https://www.nature.com/articles/s41467-025-62593-1
  - label: Code
    url: https://github.com/GuangyuWangLab2021/Thor
  - label: Documentation & tutorials
    url: https://wanglab.tech/thor
  - label: Mjolnir video tutorials
    url: https://wanglab.tech/thor/Mjolnir_video_tutorials.html
---

<p class="research-lead">Thor infers single-cell spatial transcriptomes from spot-level data by combining gene expression with cell morphology. Mjolnir, its web interface, lets you explore the result on the full-resolution slide without writing code.</p>

{% include figure.html path="assets/img/projects/thor_workflow.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Thor workflow: histology and genomics build a cell graph, heterogeneous spots are corrected with homogeneous spots, and a transition matrix drives the anti-shrinking Markov diffusion model" caption="Thor builds a cell graph from histology and genomics, then runs an anti-shrinking Markov diffusion that corrects heterogeneous spots with their homogeneous neighbours to produce in silico single-cell profiles." %}

## What Thor does

- Infers a single-cell spatial transcriptome from spot-based data such as Visium, without a separate single-cell reference.
- Ships 10 modular analysis tools, including pathway enrichment, transcription-factor activity, tissue immune microenvironment, copy-number variation, differential expression and spatially expressed module detection. Outputs plug into standard single-cell software.
- Validated on simulated data and on ISH, MERFISH, Xenium and Stereo-seq platforms, and extended to Visium HD, where it sharpens spatial gene patterns to match histology.
- Applied to regenerative signatures in heart failure, hallmark screening and CNV-based tumour mapping in ductal carcinoma in situ, fine layers of the mouse olfactory bulb, and annotation of fibrotic heart tissue.

## Mjolnir in action

Mjolnir is Thor's web interface: a viewer for whole-slide images with Thor's outputs overlaid, built for pathologists and biologists who want to inspect results interactively.

{% include video.html path="thor_mjolnir_gene_expression.mp4" poster="projects/thor_mjolnir_gene_expression_poster.jpg" label="Mjolnir: visualization of gene expression at spot and cell level" caption="<strong>Gene expression at spot and cell level.</strong> Upload an H&E slide with spot- or cell-level data, pick a gene, set the colour range, then draw a region to get its expression histogram and summary statistics. Breast cancer sample with 76,320 cells. 2 min 55 s. Video created by Alex Tran." %}

{% include video.html path="thor_mjolnir_cell_annotation.mp4" poster="projects/thor_mjolnir_cell_annotation_poster.jpg" label="Mjolnir: semi-supervised annotation of cells" caption="<strong>Semi-supervised annotation of cells.</strong> Check Thor's cell detection on the slide, select a few cells of interest, and let Mjolnir locate similar cells across the whole tissue. 45 s. Video created by Alex Tran." %}

## My contributions

Co-first author. I led the downstream application design and analysis: CNV-based tumor mapping in ductal carcinoma in situ and the identification of vascular PLA2G2A enrichment in post-LVAD heart tissue. I performed the data analyses with co-authors and co-wrote the manuscript.
