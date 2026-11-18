---
layout: project
title: Loki2
description: A biologically interpretable single-cell pathology foundation model for molecular decoding of H&E images.
img: /assets/img/projects/loki2_figure1.png
img_class: project-thumbnail-contain
importance: 0
category: work
venue: bioRxiv, 2026
role: Co-first author
links:
  - label: Read the preprint
    url: https://www.biorxiv.org/content/10.64898/2026.11.14.766416v1
---

Which molecular features of a cell can we infer from its appearance in a routine H&E stain? We trained Loki2 on **UniSeg**, a collection of 15 million cells across tissues that pairs cell segmentations and lineage annotations with measured or histology-inferred gene expression profiles.

{% include figure.html path=page.img class="img-fluid rounded z-depth-1" zoomable=true alt="Figure 1 of the Loki2 preprint, showing UniSeg, model training, and downstream analyses" caption="Figure 1 from the bioRxiv preprint shows how UniSeg was assembled, how Loki2 was trained, and how its cell representations were evaluated." %}

## What cell morphology reveals

We compared the features Loki2 learned with nuclear measurements from DAPI staining. Some features tracked visible differences in nuclear morphology, providing a biological interpretation for individual dimensions of the model’s representation.

We then tested what molecular information an H&E image could reveal by retrieving transcriptomic profiles and predicting protein staining patterns. Gene expression was most recoverable for genes associated with cell identities and functions that have a distinctive appearance under the microscope.
