---
layout: project
title: cellDancer
description: A deep-learning framework that infers cell-specific RNA velocity and transcription, splicing and degradation rates from single-cell RNA-seq.
img: /assets/img/projects/celldancer_card.jpg
importance: 3
category: work
venue: Nature Biotechnology, 2024
role: Co-author
github: https://github.com/GuangyuWangLab2021/cellDancer
links:
  - label: Paper
    url: https://www.nature.com/articles/s41587-023-01728-5
  - label: Code
    url: https://github.com/GuangyuWangLab2021/cellDancer
  - label: Documentation & tutorials
    url: https://guangyuwanglab2021.github.io/cellDancer_website/
---

<p class="research-lead">RNA velocity turns a single-cell snapshot into a direction of travel. cellDancer learns that direction cell by cell, so it stays accurate when different lineages and stages follow different kinetics.</p>

{% include figure.html path="assets/img/projects/celldancer_applications.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="cellDancer velocity fields on mouse gastrulation erythroid maturation (left) and pancreatic endocrinogenesis (right)" caption="Velocity fields inferred by cellDancer. Left: mouse gastrulation erythroid maturation, from hematoendothelial and blood progenitors to erythroid cells. Right: mouse pancreatic endocrinogenesis, with the vector field flowing from ductal and Ngn3 progenitors through pre-endocrine cells to alpha, beta, delta and epsilon fates." %}

## Why

Conventional RNA velocity models fit one set of kinetic rates to every cell in an experiment. Real tissues contain several lineages and stages at once, so that assumption breaks and the inferred arrows can point the wrong way. cellDancer drops the shared-rate assumption.

## What cellDancer does

- A deep neural network infers velocity for each cell from its neighbours, then relays those local velocities across the manifold to reach single-cell resolution.
- Estimates cell-specific transcription (α), splicing (β) and degradation (γ) rates for every gene, which reveal RNA turnover strategies and can mark cell identity better than expression alone.
- Robust across kinetic regimes, high dropout ratios and sparse datasets in simulation benchmarks.
- Resolves cases where earlier models fail, including erythroid maturation with a transcriptional boost and branching lineages in hippocampus development, and improves downstream vector-field analysis in the mouse pancreas.
- Modular, parallelised and scalable; released on PyPI with tutorials for each case study.

{% include figure.html path="assets/img/projects/celldancer_workflow.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="cellDancer workflow: a deep neural network maps each cell's unspliced and spliced counts to its own alpha, beta and gamma rates, trained by minimising the angle between predicted and observed neighbour directions on the phase portrait" caption="How it works. A deep neural network maps each cell's unspliced and spliced counts to its own transcription, splicing and degradation rates (step 1); the loss is the angle between the predicted velocity and the direction to neighbouring cells on the phase portrait (step 2); minimising it yields cell-specific kinetics (step 3). Adapted from Fig. 1b of the Nature Biotechnology paper (CC BY 4.0)." %}

{% include figure.html path="assets/img/projects/celldancer_kinetics.jpg" class="img-fluid rounded z-depth-1" zoomable=true alt="Phase portrait of Ntrk2 with cellDancer velocities, and cell-specific alpha, beta, gamma rates and expression on the hippocampus t-SNE" caption="Cell-specific kinetics. For the branching gene <em>Ntrk2</em> in mouse hippocampus development, cellDancer projects velocities on the spliced–unspliced phase portrait and maps each cell's transcription, splicing and degradation rates alongside its expression." %}

## My contributions

Co-author. As a research assistant intern (2021–2022) I analysed single-cell datasets and evaluated the robustness of the model.
