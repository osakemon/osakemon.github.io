---
layout: project
title: OmiCLIP & Loki
description: A visual–omics foundation model that links H&E histology with spatial transcriptomics, and the Loki toolkit built on it.
img: /assets/img/projects/loki_overview.jpg
importance: 1
category: work
venue: Nature Methods, 2025
role: First author
github: https://github.com/GuangyuWangLab2021/Loki
links:
  - label: Paper
    url: https://www.nature.com/articles/s41592-025-02707-1
  - label: Code
    url: https://github.com/GuangyuWangLab2021/Loki
  - label: Documentation & tutorials
    url: https://guangyuwanglab2021.github.io/Loki/
  - label: Model weights
    url: https://huggingface.co/WangGuangyuLab/Loki
---

<p class="research-lead">OmiCLIP learns one embedding space for H&amp;E tissue images and transcriptomic profiles. Loki turns that space into everyday tools for spatial biology, from tissue alignment to predicting gene expression from a plain histology slide.</p>

{% include figure.html path="assets/img/projects/loki_overview.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Overview of the ST-bank dataset, the OmiCLIP model, and the Loki Align, Annotate, Decompose and Retrieve functions" caption="ST-bank pairs 2.2 million H&E tissue patches with Visium transcriptomics across 32 organs. OmiCLIP encodes each patch and its top-expressed genes, written out as a “sentence”, with contrastive learning. Loki builds five analysis functions on the shared embedding." %}

## Why

Computational pathology models see morphology. Omics models see molecules. Research and clinical workflows need both, but existing tools analysed one modality at a time. OmiCLIP places a tissue image and its gene-expression profile at the same point in one embedding space, so either modality can be used to query, annotate or predict the other.

## What Loki does

- **Loki Align** registers spatial transcriptomics sections to each other or to an H&amp;E image.
- **Loki Annotate** labels tissue regions from bulk RNA-seq or marker-gene lists, with no spatially resolved training data.
- **Loki Decompose** estimates cell-type composition per spot from a single-cell reference.
- **Loki Retrieve** searches histology by transcriptomics and transcriptomics by histology.
- **Loki PredEx** predicts spatial gene expression directly from an H&amp;E image.

## Under the hood

- A vision transformer encodes 224 × 224 H&amp;E patches cropped to the Visium spot size.
- A causal transformer encodes each spot's transcriptome as text: the top 50 expressed gene symbols, written as one sentence of up to 76 tokens.
- The two encoders are trained contrastively with the CoCa recipe; the text encoder starts from LAION-5B weights.
- Pretraining on 2.2 million pairs took 20 epochs on a single NVIDIA A100 80 GB GPU.

## Scale and evaluation

<ul class="research-evidence" aria-label="OmiCLIP and Loki study scale">
  <li><strong>2.2M</strong> paired image–omics profiles</li>
  <li><strong>1,007</strong> tissue samples</li>
  <li><strong>32</strong> organs</li>
  <li><strong>22</strong> comparison methods</li>
  <li><strong>28</strong> benchmark datasets (5 simulated, 19 public, 4 in-house)</li>
</ul>

## My contributions

First author. I led OmiCLIP from model design and data curation through training and evaluation, and built and released Loki, the open-source platform that turns the model into five capabilities for biological research. With co-authors I analysed the data and co-wrote the manuscript. Across the visual–omics projects I have worked with TB-scale pathology datasets of more than 100,000 images. I presented the work at ICIBM 2025 and contributed materials and training to the ISMB 2026 tutorial on visual–omics foundation models.
