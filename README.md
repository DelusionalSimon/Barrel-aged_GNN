# Barrel-aged SweetNet: Graph Neural Networks for Glycomics

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-Geometric-orange)](https://pytorch-geometric.readthedocs.io/)

**An investigation into transfer learning efficacy by integrating Graph Neural Networks (SweetNet) with pre-trained Language Model (GlyLM) embeddings.**

This repository contains the **official clean implementation** of the Hyperautomated Barrel-Batching System (HBBS), a pipeline designed to rigorously test the "Infusion" hypothesis: that injecting semantic embeddings from a Glycan Language Model would enhance the predictive performance of a GNN on sparse glycomics data.

> **Note:** The complete dataset used for this study is available on Zenodo: [Record 15548889](https://zenodo.org/records/15548889)

---

## The Research Question

Glycans are the "dark matter" of biology—structurally complex, non-linear, and notoriously data-scarce.

This project challenged the conventional wisdom of glycan property prediction. The core inquiry was whether **"Infusion"**, integrating a Graph Neural Network (SweetNet) with pre-trained Glycan Language Model (GlyLM) embeddings, could bridge the knowledge gap through transfer learning.

## Methodology: The HBBS Pipeline

To ensure reproducibility and manage extensive experimentation, I engineered the **Hyperautomated Barrel-Batching System (HBBS)**.

This pipeline systematically processed hundreds of independent experimental runs across diverse glycan datasets and model configurations.

## Key Insights & Results

Contrary to the initial hypothesis, the infusion of GLM embeddings **did not** improve performance. In fact, it often degraded it.

Rather than discarding the negative result, I performed a deep analysis of the embedding space dynamics using Euclidean distance metrics and t-SNE visualization.

**The Discovery:**
The analysis revealed that the pre-trained embeddings were not functioning as complex semantic carriers within the GNN context. Instead, they acted as simple, distinguishable **glycoletter identifiers**. The GNN prioritized distinct labeling over the "rich" semantic information provided by the language model.

This finding is critical for future glycoinformatics architectures: it suggests that for current GNN models, **topological clarity outweighs semantic pre-training.**
