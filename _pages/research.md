---
layout: page
permalink: /research/
title: Research
description: 
nav: true
nav_order: 2
---

## Project: CQ-VAE: Coordinate-Quantized VAE for Shape Uncertainty Estimation

{% include figure.html path="assets/img/cq_vae.jpg" title="example image" class="img-fluid rounded z-depth-1" %}

- Motivation:
    - Formulated to address shape uncertainty estimation on lumbar spine MR images, specifically motivated by inter-annotator disagreement on lumbar spine disc boundaries.
    - Traditional models often struggle to quantify the reliability of reconstructed geometries when expert labels vary.

- Brief description of our work:
    - I designed **CQ-VAE**, a generative network utilizing a coordinate-quantized discrete latent space that learns shape distributions from multi-annotator lumbar spine MR images.
    - Developed a global-greedy shape sampling-matching strategy to balance generative diversity against accuracy on existing ground truth shapes.
    - Demonstrated a strong correlation between estimated uncertainty and true shape error, achieving state-of-the-art results in shape variation analysis.

- Please read our [ICMLA paper](https://arxiv.org/abs/2010.08713) for details.

---

## Project: Attention-Based Shape-Deformation Networks for Lumbar Spine MR Imaging

<div class="row justify-content-sm-center">
    <div class="col-sm-12 mt-3">
        {% include figure.html path="assets/img/transdeformer.jpg" title="Top Image Description" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-12 mt-3">
        {% include figure.html path="assets/img/transdeformer_eval.jpg" title="Bottom Image Description" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

- Motivation:
    - Aimed at reconstructing artifact-free lumbar spine meshes with inter-patient correspondence to enable consistent and accurate measurement of medical parameters related to disc degeneration.
    - Standard networks often fail to capture long-range spatial dependencies between mesh and image features required for complex geometry reconstruction.

- Brief description of our work:
    - I designed two novel attention-based shape-deformation networks, **UNet-DeformSA** and **TransDeformer**, which integrate self- and cross-modal attention to capture long-range dependencies.
    - Proposed a three-mode training strategy that ensures robust deformation even under imperfect template initialization.
    - Built a TransDeformer variant for point-wise shape error estimation, enabling reconstructed geometries to be ranked by predicted error for prioritized clinician review.

- Please read our [TMI paper](https://ieeexplore.ieee.org/document/11080083) for details.

---

## Project: Structured Quad-Mesh Reconstruction of the Aortic Valve from 3D CT

{% include figure.html path="assets/img/aortic_mesh_eval.jpg" title="example image" class="img-fluid rounded z-depth-1" %}

- Motivation:
    - Traditional automated aortic valve meshing often relies on unstructured triangular meshes that require complicated loss functions and produce lower element quality.
    - High-quality, consistent correspondence across patient datasets is necessary for accurate finite element analysis.

- Brief description of our work:
    - Developed a template-fitting remeshing pipeline to produce annotated datasets of high-quality structured quad meshes for the aortic valve.
    - Simplified the training process to only two loss terms while preserving mesh smoothness and element quality, achieving a 20-25% improvement in specific metrics over unstructured triangular meshes.
    - This work enables more efficient patient-specific modeling for thoracic aortic aneurysm analysis.

- Please read our [SPIE presentation](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/13929/139291I/Shape-deformation-networks-for-automated-aortic-valve-finite-element-meshing/10.1117/12.3087767.short) and [paper](https://arxiv.org/pdf/2511.03890) for details.
