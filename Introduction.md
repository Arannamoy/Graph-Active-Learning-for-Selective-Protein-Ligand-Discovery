# Graph Active Learning for Docking-Efficient Protein-Ligand Discovery

## Overview

This project proposes a Graph Active Learning (GAL) framework for efficient Protein-Ligand Discovery.

Traditional virtual screening requires docking thousands or millions of molecules against a target protein, which is computationally expensive and time-consuming.

The proposed system combines:

* Graph Isomorphism Network (GIN)
* Graph Active Learning (GAL)
* AutoDock Vina Validation

to identify promising protein-binding molecules while significantly reducing the number of required docking evaluations.

The framework will be evaluated on:

* HER2
* EGFR
* KRAS

as benchmark oncology targets.

---

# Motivation

In conventional drug discovery pipelines:

```text
Protein
   ↓
Millions of Molecules
   ↓
Docking
   ↓
Ranking
```

every molecule must be evaluated, making the process expensive.

This project investigates whether Graph Active Learning can intelligently select only the most informative molecules for docking while preserving discovery performance.

---

# Research Question

Can Graph Active Learning reduce expensive docking evaluations while maintaining high-quality protein-ligand discovery performance?

---

# Core Idea

The framework consists of three major components:

## GIN (Graph Isomorphism Network)

Acts as the molecular intelligence engine.

Responsibilities:

* Learn molecular structure representations
* Understand atom-bond relationships
* Predict protein-ligand affinity

## Graph Active Learning (GAL)

Acts as the decision-making strategy.

Responsibilities:

* Identify uncertain predictions
* Select informative molecules
* Reduce unnecessary docking evaluations

## AutoDock Vina

Acts as the external validator.

Responsibilities:

* Validate predicted interactions
* Generate docking scores
* Provide feedback for model improvement

---

# System Architecture

```mermaid
flowchart TD

A[Protein Target]
B[Molecule Dataset]

A --> C
B --> C

C[GIN Affinity Predictor]

C --> D[Predicted Affinity]

D --> E[Graph Active Learning]

E --> F[Selected Molecules]

F --> G[AutoDock Vina]

G --> H[Docking Score]

H --> I[Feedback]

I --> C
```

---

# Active Learning Cycle

```mermaid
flowchart LR

A[Molecule Pool]
B[GIN Prediction]
C[Uncertainty Estimation]
D[Molecule Selection]
E[Docking Validation]
F[Feedback]
G[Model Update]

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> B
```

---

# Benchmark Targets

The framework will initially be evaluated using three oncology-related proteins.

## HER2

Human Epidermal Growth Factor Receptor 2

## EGFR

Epidermal Growth Factor Receptor

## KRAS

Kirsten Rat Sarcoma Viral Oncogene

These proteins serve as benchmark targets for validating the proposed framework.

---

# Datasets

## Protein-Ligand Interaction Data

* BindingDB
* ChEMBL
* PDBbind

## Molecular Libraries

* ChEMBL
* ZINC

---

# Technology Stack

## Graph Machine Learning

* PyTorch
* PyTorch Geometric

## Molecular Informatics

* RDKit
* Open Babel

## Docking

* AutoDock Vina

## Visualization

* PyMOL
* Discovery Studio Visualizer

## Data Processing

* NumPy
* Pandas

---

# Evaluation Metrics

## Prediction Metrics

* RMSE
* MAE
* Pearson Correlation
* Spearman Correlation

## Discovery Metrics

* Top-K Hit Rate
* Docking Success Rate
* Docking Cost Reduction

## Docking Metrics

* Binding Affinity
* Interaction Score
* Top Candidate Recovery

---

# Experimental Setup

## Baseline

GIN + Random Sampling

```text
GIN
 ↓
Random Molecule Selection
 ↓
Docking
```

## Proposed Method

GIN + Graph Active Learning

```text
GIN
 ↓
Graph Active Learning
 ↓
Smart Molecule Selection
 ↓
Docking
```

---

# Expected Contributions

1. Graph Active Learning Framework for Protein-Ligand Discovery
2. Docking-Efficient Virtual Screening Pipeline
3. Reduced Docking Computational Cost
4. Intelligent Molecule Selection Strategy
5. Automated Protein-Ligand Ranking Workflow

---

# Repository Structure

```text
project/
│
├── data/
├── notebooks/
├── models/
│   ├── gin/
│   └── active_learning/
│
├── docking/
├── evaluation/
├── visualization/
├── results/
└── README.md
```

---

# Development Environment

Recommended:

* macOS (Apple Silicon)
* Linux

Minimum Hardware:

* 16 GB RAM
* Modern Multi-Core CPU
* SSD Storage

Recommended Hardware:

* Apple M5
* 24–32 GB RAM
* 512 GB SSD

---

# Future Extensions

The following features are intentionally excluded from the initial undergraduate implementation and may be explored in future work:

* Toxicity Prediction
* Off-Target Interaction Analysis
* Multi-Objective Optimization
* Molecular Dynamics Simulation
* Diffusion-Based Molecule Generation
* Foundation Models for Drug Discovery

---

# Current Status

Phase 0 — Research Planning

Planned Pipeline:

Protein → GIN → Graph Active Learning → AutoDock Vina → Feedback Loop

Target Scope:

HER2, EGFR, KRAS
