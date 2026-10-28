---
layout: page
title: CV
permalink: /cv/
description: Machine Learning Researcher | Multimodal AI & Computational Biology. Houston, TX (open to relocation). Available early 2027.
nav: true
nav_order: 3
---

<!-- _pages/cv.md -- the CV, transcribed verbatim from assets/pdf/CV-WeiqingChen.pdf
     (section order, wording and dates match the PDF). The PDF is the source of
     truth: when it changes, replace the file and mirror the edits here. -->
<div class="cv-page" markdown="1">

<div class="research-links cv-actions" aria-label="CV downloads, contact and profiles">
  <a href="{{ '/assets/pdf/CV-WeiqingChen.pdf' | relative_url }}">Download PDF <span aria-hidden="true">&rarr;</span></a>
  <a href="mailto:{{ site.email | encode_email }}">Email</a>
  <a href="https://www.linkedin.com/in/{{ site.linkedin_username }}">LinkedIn</a>
  <a href="https://github.com/{{ site.github_username }}">GitHub</a>
  <a href="https://scholar.google.com/citations?user={{ site.scholar_userid }}">Google Scholar</a>
  <a href="{{ '/publications/' | relative_url }}">Publications</a>
</div>
<p class="cv-updated">PDF version: October 2026.</p>

## Profile

Machine-learning researcher developing multimodal foundation models and research tools for computational pathology, single-cell biology, spatial biology, dynamical modeling of biological systems, and multi-omics analysis, including transcriptomics, proteomics, and metabolomics. Led end-to-end development of **OmiCLIP, a visual-omics foundation model, and its downstream platform, Loki** (**Nature Methods**), from model design and data curation through training, evaluation, and software release, including downstream task development and applications to biological research. International and interdisciplinary background: trained in computer science in China, theoretical biology in Japan, and AI for biomedicine in the United States. First and co-first author of work published in **Nature Methods**, **Nature Communications**, and **Circulation Research**, with a first-author manuscript in third-round revision at **Nature**.

## Technical expertise

<dl class="cv-skills">
  <div><dt>Programming &amp; Frameworks</dt><dd>Python (PyTorch, Hugging Face, scikit-learn, NumPy/pandas, AnnData/Scanpy, Squidpy), R (Seurat, DESeq2), MATLAB; Linux, HPC (Slurm), Git, Docker, AWS; cloud workflow deployment.</dd></div>
  <div><dt>Machine Learning</dt><dd>Foundation models, multimodal representation learning, contrastive (CLIP-style) vision–language pretraining, vision transformers, transfer learning and fine-tuning, zero-shot retrieval and linear probing, Bayesian modeling, classical machine learning (logistic regression, random forests, SVMs), multi-GPU training on HPC, production deployment of foundation models.</dd></div>
  <div><dt>Computational Biology</dt><dd>Computational pathology, transcriptomics, proteomics, metabolomics, spatial omics (10x Visium / Visium HD / Xenium / MERFISH / Stereo-seq / CODEX), single-cell omics, multi-omics integration, dynamical modeling of biological systems.</dd></div>
  <div><dt>Imaging &amp; Data</dt><dd>OpenSlide, OpenCV, QuPath, Cellpose, OME-Zarr; H&amp;E, IHC, mIF, and CODEX image analysis; whole-slide images and TB-scale pathology datasets.</dd></div>
  <div><dt>Languages</dt><dd>Chinese (native), English, Japanese (JLPT N1).</dd></div>
</dl>

## Education

<article class="cv-entry">
  <header>
    <h3>Cornell University, Weill Cornell Graduate School of Medical Sciences</h3>
    <p class="cv-dates">Aug. 2022 – 2027 (Expected)</p>
  </header>
  <p class="cv-role">Ph.D. Candidate, Physiology, Biophysics and Systems Biology | Advisor: Guangyu Wang, Ph.D.</p>
</article>

<article class="cv-entry">
  <header>
    <h3>Kyoto University</h3>
    <p class="cv-dates">Oct. 2019 – Sep. 2021</p>
  </header>
  <p class="cv-role">Master of Science, Systemic Life Science | Advisor: Naoki Honda, Ph.D.</p>
</article>

<article class="cv-entry">
  <header>
    <h3>Nanjing University of Posts and Telecommunications</h3>
    <p class="cv-dates">Sep. 2015 – Jun. 2019</p>
  </header>
  <p class="cv-role">Bachelor of Computer Science and Technology</p>
</article>

## Research &amp; engineering experience

<article class="cv-entry">
  <header>
    <h3>Houston Methodist Research Institute / Weill Cornell Medicine</h3>
    <p class="cv-dates">Aug. 2022 – Present</p>
  </header>
  <p class="cv-role">Visiting Graduate Research Fellow | Houston, TX</p>
  <ul>
    <li>Led <strong>OmiCLIP</strong>, a visual-omics foundation model, from model design and data curation through training and evaluation, aligning histopathology with transcriptomics via contrastive learning on <strong>2.2 million paired tissue patches</strong> from <strong>1,007 samples across 32 organs</strong>, curated from <strong>113 studies</strong>. Benchmarked the model and its downstream platform, Loki, against <strong>22 state-of-the-art methods across five core downstream task categories</strong>; co-first author, <strong>Nature Methods</strong> (2025).</li>
    <li>Built and released <strong>Loki</strong>, the open-source downstream platform that translates OmiCLIP into five capabilities for biological research: tissue alignment, molecular annotation, cell-type decomposition, image-transcriptomics retrieval, and spatial gene-expression prediction from H&amp;E images. Across visual-omics projects and Loki2, worked with <strong>TB-scale pathology datasets spanning over 100,000 images</strong>. <span class="cv-links"><a href="https://github.com/GuangyuWangLab2021/Loki">Code</a> · <a href="https://huggingface.co/WangGuangyuLab/Loki">Model weights</a> · <a href="{{ '/projects/loki/' | relative_url }}">Project page</a></span></li>
    <li>Led end-to-end development of a <strong>single-cell pathology foundation model</strong> for molecular decoding of H&amp;E images, spanning model design, data curation, training, evaluation, software development, downstream task development, and applications to biological research; first-author manuscript in <strong>third-round revision at Nature</strong>.</li>
    <li>Led downstream application design and analysis for <strong>Thor</strong>, integrating histology and spatial transcriptomics at cellular resolution to enable CNV-based tumor mapping in ductal carcinoma in situ and identify vascular PLA2G2A enrichment in post-LVAD heart tissues; co-first author, <strong>Nature Communications</strong> (2025). <span class="cv-links"><a href="https://github.com/GuangyuWangLab2021/Thor">Code</a> · <a href="{{ '/projects/thor/' | relative_url }}">Project page</a></span></li>
    <li><strong>Collaborative biological discovery:</strong> Computational analyses with experimental teams linked LATS1/2-CD38 signaling to endothelial senescence and thrombosis, mTORC1 and AIBP-VEGFR3 to lymphatic development, and metastatic precursor cells to candidate HSP90AA1/HSP90AB1 biomarkers; co-first author, <strong>Circulation Research</strong>; contributing author, <strong>Developmental Cell</strong> and <strong>Nature Communications</strong>.</li>
    <li><strong>Technical mentoring and training:</strong> Mentored <strong>five</strong> junior Ph.D. students, rotation students, and research assistants through shared pipelines, code review, and result reproduction; trainee analyses supported downstream applications and one trainee built an independent pipeline. Contributed materials and training for the <strong>ISMB 2026 tutorial</strong> on visual-omics foundation models; coordinated compute needs with HPC platform providers.</li>
  </ul>
</article>

<article class="cv-entry">
  <header>
    <h3>Houston Methodist Research Institute</h3>
    <p class="cv-dates">Sep. 2021 – Jun. 2022</p>
  </header>
  <p class="cv-role">Research Assistant Intern | Remote</p>
  <ul>
    <li>Analyzed single-cell data and evaluated model robustness for <strong>cellDancer</strong>, a deep-learning method for cell-dependent RNA velocity and cell-state dynamics; contributing author, <strong>Nature Biotechnology</strong>. <span class="cv-links"><a href="https://github.com/GuangyuWangLab2021/cellDancer">Code</a> · <a href="{{ '/projects/celldancer/' | relative_url }}">Project page</a></span></li>
  </ul>
</article>

<article class="cv-entry">
  <header>
    <h3>Kyoto University</h3>
    <p class="cv-dates">Apr. 2020 – Mar. 2021</p>
  </header>
  <p class="cv-role">Research Assistant | Kyoto, Japan</p>
  <ul>
    <li>Developed a Bayesian active-inference framework for gradient sensing in goal-directed migration, connecting theoretical biology with computational modeling; presented the work at national biophysics and mathematical biology meetings in Japan.</li>
  </ul>
</article>

<article class="cv-entry">
  <header>
    <h3>Gausscode AI Automotive Solution</h3>
    <p class="cv-dates">Sep. 2018 – Sep. 2019</p>
  </header>
  <p class="cv-role">Software Engineer and Data Analyst Intern | Nanjing, China</p>
  <ul>
    <li>Built data-collection pipelines and analysis workflows for an AI and big-data company serving the automotive industry, and contributed to the development of its internal data platform.</li>
  </ul>
</article>

## Selected publications

<p class="cv-note">*Co-first authors. The <a href="{{ '/publications/' | relative_url }}">publications page</a> has links to every paper.</p>

1. **W. Chen\***, Q. Li\*, H. Cheng\*, et al. A single-cell pathology foundation model for molecular decoding of H&E images. Under revision in **Nature**, third round.
2. **W. Chen\***, P. Zhang\*, et al. A visual-omics foundation model to bridge histopathology with spatial transcriptomics. **Nature Methods**, 2025. [Paper](https://www.nature.com/articles/s41592-025-02707-1)
3. P. Zhang\*, **W. Chen\***, et al. Thor: a platform for cell-level investigation of spatial transcriptomics and histology. **Nature Communications**, 2025. [Paper](https://www.nature.com/articles/s41467-025-62593-1)
4. S. Kotla\*, J. Lee\*, K. A. Ko\*, **W. Chen\***, et al. LATS1/2-CD38 metabolic rewiring links senescence to intraplaque thrombosis. **Circulation Research**, 2026. [Paper](https://www.ahajournals.org/doi/full/10.1161/CIRCRESAHA.125.327427)
5. S. Li\*, P. Zhang\*, **W. Chen**, et al. A relay velocity model infers cell-dependent RNA velocity. **Nature Biotechnology**, 2024. [Paper](https://www.nature.com/articles/s41587-023-01728-5)
6. X. Wang, M. Duan, A. J. Snyder, …, **W. Chen**, et al. Deep-learning-enabled multi-omics analyses for prediction of future metastasis in cancer. **Nature Communications**, 2026. [Paper](https://www.nature.com/articles/s41467-026-76277-x)
7. F. Han, S. Simeroth, J. Zhu, I. Gryniuk, A. Pranay, **W. Chen**, et al. Lymphatic endothelial mTORC1 instructs metabolic and developmental signaling during lymphangiogenesis. **Developmental Cell**, 2025. [Paper](https://www.cell.com/developmental-cell/fulltext/S1534-5807(25)00250-3)
8. J. Kim, S. Chaudhary, **W. Chen**, et al. APOA1 binding protein promotes lymphatic cell fate and lymphangiogenesis by relieving caveolae-mediated inhibition of VEGFR3 signaling. **Nature Communications**, 2025. [Paper](https://www.nature.com/articles/s41467-025-60611-w)

## Selected presentations &amp; awards

<ul class="cv-list">
  <li><strong>ISMB 2026</strong> | Tutorial on visual-omics foundation models; contributed materials and training. <span class="cv-dates">Jul. 2026</span></li>
  <li><strong>ICIBM 2025</strong> | Presentation on OmiCLIP, a visual-omics foundation model. <span class="cv-dates">Aug. 2025</span></li>
  <li><strong>Texas Single Cell &amp; Spatial Genomics Seminar Series</strong> | Presentation. <span class="cv-dates">Nov. 2024</span></li>
  <li><strong>DeBakey Heart and Vascular Center Research Day</strong> | Poster; Best Poster Award. <span class="cv-dates">May 2024</span></li>
  <li><strong>8th Annual Cardiovascular Bioengineering Symposium</strong> | Poster. <span class="cv-dates">May 2024</span></li>
</ul>

**Awards &amp; honors:** Best Poster Award, PBSB Program Annual Retreat, Weill Cornell Medicine (Apr. 2026); JASSO Honors Scholarship, Japan Student Services Organization (2019, 2020); NJUPT: Academic Excellence Award (2018), Excellent Student Cadre and Social Work Excellence Awards (2017–2019), Vice Chairman of the Student Association for Science and Technology (2017–2018).

</div>
