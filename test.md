# Graph Active Learning for Selective Protein-Ligand Discovery

## Overview

Graph Active Learning for Selective Protein-Ligand Discovery is an AI-driven drug discovery framework designed to identify novel, selective, and potentially safer molecules for target proteins while minimizing expensive computational screening costs.

Unlike traditional virtual screening pipelines that focus solely on binding affinity, this framework incorporates:

* Protein-Ligand Interaction Prediction
* Graph Active Learning
* Off-Target Interaction Analysis
* Toxicity Assessment
* Docking-Based Validation
* Multi-Objective Candidate Ranking

The system aims to discover molecules that are not only strong binders to the target protein but also exhibit lower toxicity and reduced off-target interactions.

Initial evaluation will be performed on oncology-related targets including HER2, EGFR, and KRAS.

---

# Problem Statement

Traditional drug discovery pipelines often optimize only for binding affinity.

However, in real-world pharmaceutical development:

* Strong binding alone is insufficient.
* Molecules may interact with unintended proteins.
* Off-target interactions may cause side effects.
* Toxic compounds may fail in later stages.

This project addresses these challenges by integrating Active Learning, Selectivity Analysis, and Toxicity Prediction into a unified framework.

---

# Research Question

Can Graph Active Learning reduce expensive docking evaluations while discovering highly selective and low-toxicity protein-binding molecules?

---

# Objectives

## Primary Objectives

* Protein-Ligand Affinity Prediction
* Graph Active Learning-Based Molecule Selection
* Off-Target Interaction Prediction
* Toxicity Assessment
* Docking Validation using AutoDock Vina
* Interaction Statistics Generation

## Secondary Objectives

* Molecular Diversity Optimization
* Drug-Likeness Estimation
* Docking Cost Reduction
* Multi-Objective Candidate Ranking

---

# System Architecture

```mermaid
flowchart TD

A[Protein Target]
B[Molecule Library]

A --> C
B --> C

C[GIN-Based Affinity Predictor]

C --> D[Target Affinity Score]

D --> E[Graph Active Learning]

E --> F[Selected Molecules]

F --> G[Off-Target Interaction Analysis]

G --> H[Toxicity Prediction]

H --> I[Multi-Objective Ranking]

I --> J[AutoDock Vina Validation]

J --> K[Interaction Statistics]

K --> L[Feedback Loop]

L --> C
```

---

# Active Learning Workflow

```mermaid
flowchart LR

A[Generated Molecules]
B[Affinity Prediction]
C[Uncertainty Estimation]
D[Diversity Analysis]
E[Candidate Selection]
F[Docking Validation]
G[Feedback]
H[Model Update]

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H
H --> B
```

---

# Multi-Objective Optimization

The framework does not optimize only for affinity.

Final molecule ranking considers:

```text
Target Affinity
+
Selectivity
+
Drug-Likeness
+
Molecular Diversity
-
Toxicity
-
Off-Target Binding
```

---

# Selectivity Analysis

The framework evaluates interactions against:

## Target Protein

* HER2
* EGFR
* KRAS

## Off-Target Proteins

Additional proteins may be incorporated to estimate:

* Cross-reactivity
* Potential side effects
* Selectivity score

---

# Toxicity Analysis

Toxicity estimation will be performed using machine learning models trained on:

* Tox21
* ClinTox

Predicted endpoints may include:

* Cytotoxicity
* Organ toxicity
* General toxicity risk

---

# Datasets

## Protein-Ligand Interaction

* BindingDB
* ChEMBL
* PDBbind

## Toxicity

* Tox21
* ClinTox

## Molecular Libraries

* ZINC
* ChEMBL

---

# Technology Stack

## AI & Deep Learning

* PyTorch
* PyTorch Geometric

## Molecular Modeling

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

## Drug Discovery Metrics

* Binding Affinity
* Selectivity Score
* Toxicity Score
* Drug-Likeness Score
* Molecular Diversity Score

---

# Expected Contributions

1. Graph Active Learning Framework for Drug Discovery
2. Docking-Efficient Protein-Ligand Screening
3. Selectivity-Aware Molecule Ranking
4. Toxicity-Aware Candidate Selection
5. Automated Interaction Statistics Generation
6. Multi-Objective Drug Discovery Workflow

---

# Demonstration Targets

## HER2

Human Epidermal Growth Factor Receptor 2

## EGFR

Epidermal Growth Factor Receptor

## KRAS

Kirsten Rat Sarcoma Viral Oncogene

These targets serve as benchmark proteins for evaluating the proposed framework.

---

# Future Extensions

* Molecular Dynamics Validation
* Diffusion-Based Molecule Generation
* Reinforcement Learning Optimization
* Foundation Models for Drug Discovery
* Multi-Target Drug Design
* Clinical Candidate Prioritization

---

<!-- # Repository Structure

```text
project/
│
├── data/
├── notebooks/
├── models/
│   ├── affinity/
│   ├── toxicity/
│   └── active_learning/
│
├── docking/
├── protein_processing/
├── off_target_analysis/
├── interaction_statistics/
├── evaluation/
├── visualization/
├── results/
└── README.md
```-->
## Prerequisite Knowledge

This project sits at the intersection of Graph Machine Learning, Drug Discovery, Cheminformatics, Bioinformatics, and Active Learning. The following topics are recommended before contributing to the project.

---

# 1. Programming Fundamentals

### Required Skills

* Python Programming
* Object-Oriented Programming (OOP)
* Data Structures and Algorithms
* NumPy
* Pandas
* Matplotlib

### Recommended References

#### Books

* Python Crash Course — Eric Matthes
* Fluent Python — Luciano Ramalho

#### Documentation

* Python Official Documentation
* NumPy Documentation
* Pandas Documentation

---

# 2. Machine Learning

### Required Topics

* Supervised Learning
* Regression
* Classification
* Model Evaluation
* Cross Validation
* Bias-Variance Tradeoff

### Recommended Books

* Hands-On Machine Learning with Scikit-Learn, Keras and TensorFlow — Aurélien Géron
* Introduction to Statistical Learning (ISLR)

---

# 3. Deep Learning

### Required Topics

* Neural Networks
* Backpropagation
* Loss Functions
* Optimization
* Regularization

### Recommended Books

* Deep Learning — Ian Goodfellow
* Dive Into Deep Learning (D2L)

---

# 4. Graph Neural Networks (Core Requirement)

### Required Topics

* Graph Representation
* Node Features
* Edge Features
* Message Passing
* Graph Classification
* Graph Regression

### Models to Study

* GCN
* GraphSAGE
* GAT
* GIN
* Graph Transformers

### Recommended Books

* Graph Representation Learning — William Hamilton

### Recommended Papers

#### GraphSAGE

Hamilton et al. (2017)

"Inductive Representation Learning on Large Graphs"

#### GAT

Veličković et al. (2018)

"Graph Attention Networks"

#### GIN

Xu et al. (2019)

"How Powerful are Graph Neural Networks?"

---

# 5. PyTorch & PyTorch Geometric

### Required Topics

* Dataset
* DataLoader
* Training Loop
* Custom Models
* Graph Data Structures

### Recommended References

* PyTorch Official Documentation
* PyTorch Geometric Documentation

---

# 6. Cheminformatics

### Required Topics

* Molecules as Graphs
* SMILES Representation
* Molecular Fingerprints
* Molecular Descriptors
* Drug-Likeness

### Recommended Book

* RDKit Cookbook

### Recommended References

* RDKit Documentation
* Practical Cheminformatics Tutorials

---

# 7. Drug Discovery Fundamentals

### Required Topics

* Proteins
* Ligands
* Binding Affinity
* Binding Pocket
* Drug Discovery Pipeline

### Recommended Books

* An Introduction to Medicinal Chemistry — Graham Patrick
* Drug Discovery and Development — Raymond Hill

---

# 8. Protein-Ligand Interaction

### Required Topics

* Protein Structure
* Ligand Binding
* Hydrogen Bonds
* Hydrophobic Interactions
* Salt Bridges
* Binding Energy

### Recommended Resources

* RCSB Protein Data Bank Tutorials
* Molecular Docking Tutorials

---

# 9. Molecular Docking

### Required Topics

* Docking Theory
* Search Space
* Scoring Functions
* Binding Affinity

### Tools

* AutoDock Vina
* PyMOL
* Discovery Studio Visualizer

### Recommended Papers

#### AutoDock Vina

Trott & Olson (2010)

"AutoDock Vina: Improving the Speed and Accuracy of Docking"

---

# 10. Active Learning (Core Research Area)

### Required Topics

* Uncertainty Sampling
* Diversity Sampling
* Query Strategies
* Exploration vs Exploitation

### Recommended Book

* Active Learning — Burr Settles

### Recommended Papers

#### Active Learning Literature Survey

Settles (2009)

#### MolPAL

Graff et al.

"Molecule Discovery using Active Learning"

---

# 11. Drug Discovery Datasets

### Essential Datasets

#### Protein-Ligand Interaction

* BindingDB
* ChEMBL
* PDBbind

#### Toxicity

* Tox21
* ClinTox

#### Molecular Libraries

* ZINC

---

# 12. Multi-Objective Optimization

### Required Topics

* Pareto Front
* Multi-Objective Search
* Trade-Off Analysis

### Optimization Objectives

* Binding Affinity
* Toxicity
* Selectivity
* Drug-Likeness
* Molecular Diversity

### Recommended Papers

* ParetoDrug
* MO-MEMES
* Multi-Objective Virtual Screening Literature

---

# 13. Selectivity & Off-Target Analysis

### Required Topics

* Target Proteins
* Off-Target Proteins
* Cross-Reactivity
* Selectivity Index

### Importance

A molecule with excellent affinity may still fail if it strongly binds to unintended proteins.

This project explicitly evaluates:

* Target Affinity
* Off-Target Interactions
* Toxicity Risk

before candidate prioritization.

---

# Suggested Learning Roadmap

```text
Phase 1
--------
Python
NumPy
Pandas
PyTorch

Phase 2
--------
Graph Theory
GCN
GraphSAGE
GAT
GIN

Phase 3
--------
RDKit
SMILES
Molecular Graphs

Phase 4
--------
Protein-Ligand Interaction
BindingDB
PDBbind

Phase 5
--------
AutoDock Vina
PyMOL

Phase 6
--------
Active Learning
MolPAL

Phase 7
--------
Multi-Objective Optimization
Selectivity Analysis
Toxicity Prediction

Phase 8
--------
Full Project Integration
```

---

# Expected Background

A contributor should ideally have:

* Intermediate Python Knowledge
* Basic Machine Learning Knowledge
* Basic Deep Learning Knowledge
* Interest in Drug Discovery
* Familiarity with Graph Neural Networks

No prior background in biology or chemistry is strictly required, although it is highly beneficial.

## Hardware Requirements

### Minimum Development Environment

| Component | Requirement                   |
| --------- | ----------------------------- |
| CPU       | Apple M1 / Ryzen 7 / Intel i7 |
| RAM       | 16 GB                         |
| Storage   | 256 GB SSD                    |
| OS        | Linux / macOS                 |

### Recommended Development Environment

| Component | Requirement                               |
| --------- | ----------------------------------------- |
| CPU       | Apple M5 / Ryzen 7 8845HS / Intel Ultra 7 |
| RAM       | 24–32 GB                                  |
| Storage   | 512 GB SSD or higher                      |
| OS        | Linux (Preferred) or macOS                |

---

## Development Philosophy

This project prioritizes **local reproducible development**.

Cloud notebook environments such as:

* Google Colab
* Kaggle Notebooks

are intentionally not used as primary development platforms due to:

* Frequent dependency changes
* Package version incompatibilities
* RDKit installation inconsistencies
* PyTorch Geometric version conflicts
* AutoDock Vina integration issues
* Reproducibility challenges

Instead, the project is designed to run in a controlled local environment using:

* Python Virtual Environment (`venv`)
* Conda Environment
* Docker Containers (Future Support)

---

## Local Development Stack

```text
Python 3.12
PyTorch
PyTorch Geometric
RDKit
AutoDock Vina
NumPy
Pandas
Matplotlib
Open Babel
```

---

## Reproducibility Goal

A primary goal of this project is to ensure that every experiment can be reproduced on a local machine without relying on cloud-specific configurations.

The repository will maintain:

* Fixed package versions
* Dependency lock files
* Environment setup scripts
* Reproducible training pipelines

to guarantee consistent results across different systems.

---

## Computational Considerations

The proposed Graph Active Learning framework is designed to reduce expensive docking evaluations by intelligently selecting candidate molecules.

Instead of:

```text
1,000,000 Molecules
        ↓
1,000,000 Docking Runs
```

the framework aims for:

```text
1,000,000 Molecules
        ↓
Graph Neural Network Screening
        ↓
Graph Active Learning Selection
        ↓
1,000–10,000 Docking Runs
```

thereby reducing computational cost while preserving discovery performance.

---

# Current Status

Phase 0: Research Planning & System Design

Planned Architecture:

GIN + Graph Active Learning + Selectivity Analysis + Toxicity Prediction + AutoDock Vina Validation
