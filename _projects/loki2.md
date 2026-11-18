---
layout: project
title: Loki2
description: A biologically interpretable single-cell pathology foundation model for molecular decoding of H&E images.
importance: 0
category: work
venue: bioRxiv, 2026
role: Co-first author
links:
  - label: Read the preprint
    url: https://www.biorxiv.org/content/10.64898/2026.11.14.766416v1
---

Which molecular features of a cell can we infer from its appearance in a routine H&E stain? We trained Loki2 on **UniSeg**, a collection of 15 million cells across tissues that pairs cell segmentations and lineage annotations with measured or histology-inferred gene expression profiles.

## What cell morphology reveals

We compared the features Loki2 learned with nuclear measurements from DAPI staining. Some features tracked visible differences in nuclear morphology, providing a biological interpretation for individual dimensions of the model’s representation.

We then tested what molecular information an H&E image could reveal by retrieving transcriptomic profiles and predicting protein staining patterns. Gene expression was most recoverable for genes associated with cell identities and functions that have a distinctive appearance under the microscope.
