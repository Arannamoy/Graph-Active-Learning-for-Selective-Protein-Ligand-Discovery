# AI-Driven-Discovery-of-Novel-Inhibitors-for-KRAS-HER2-Target-in-Colorectal-Gastric-Cancer
### Step 1: Cheminformatics
- Deep Learning for the Life Sciences by Bharath Ramsundar (O'Reilly)
- Practical Cheminformatics by Pat Walters
- MoleculeNet: A benchmark for molecular machine learning (Wu et al., 2018).

### Step 2: Deep Learning for Drug Discovery
- Artificial Intelligence in Drug Design by Alexander Heifetz
- MIT 6.874 (Deep Learning in the Life Sciences)
- Analyzing Learned Molecular Representations for Property Prediction
- Automatic Chemical Design Using a Data-Driven Continuous Representation of Molecules

### Step 3: Structural Biology & Molecular Docking
- Molecular Modelling: Principles and Applications by Andrew Leach
- Molecular Docking Tutorial with AutoDock Vina
- AutoDock Vina: Improving the speed and accuracy of docking with a new scoring function (Trott & Olson, 2010)

### Tech Stack
1. [x] RDKit
2. [ ] PyTorch Geometric
3. [ ] DeepChem
4. [ ] TorchDrug
5. [ ] ESM
6. [ ] OpenFold
7. [ ] AutoDock Vina
8. [ ] OpenMM
9. [ ] Scanpy
10. [ ] Captum
11. [ ] MLflow
12. [ ] FastAPI
13. [ ] Docker

### RDKit Must-Know Checklist

## 1. Molecule Basics

- [x] Install RDKit
- [x] Chem.MolFromSmiles()
- [x] Chem.MolToSmiles()
- [X] Canonical SMILES
- [X] Explicit vs Implicit Hydrogens
- [X] Atom Objects
- [X] Bond Objects
- [X] Atom Indexing
- [X] Molecular Formula

---

## 2. SMILES Fundamentals

- [X] Organic Subset Atoms
- [X] Branches ()
- [X] Ring Closures (1,2,3...)
- [X] Aromatic Atoms (c, n, o)
- [X] Charges ([NH4+])
- [X] Isotopes ([13C])
- [X] Chirality (@, @@)
- [X] Dative Bonds (->)
- [X] Quadruple Bonds ($)

---

## 3. SMARTS Fundamentals

- [ ] Chem.MolFromSmarts()
- [ ] Atom Queries ([#6], [#7])
- [ ] Logical Operators (, ; &)
- [ ] Recursive SMARTS
- [ ] QueryAtom
- [ ] DescribeQuery()
- [ ] SMARTS vs SMILES

---

## 4. Substructure Searching

- [ ] HasSubstructMatch()
- [ ] GetSubstructMatch()
- [ ] GetSubstructMatches()
- [ ] SMARTS Pattern Search
- [ ] Functional Group Detection

---

## 5. Molecular Properties

- [ ] Molecular Weight
- [ ] Exact Molecular Weight
- [ ] LogP
- [ ] TPSA
- [ ] H-Bond Donors
- [ ] H-Bond Acceptors
- [ ] Rotatable Bonds
- [ ] Ring Count

---

## 6. Molecular Fingerprints

- [ ] Morgan Fingerprint (ECFP)
- [ ] RDK Fingerprint
- [ ] MACCS Keys
- [ ] Bit Vectors
- [ ] Fingerprint Similarity
- [ ] Tanimoto Similarity

---

## 7. Molecular Visualization

- [ ] Draw Molecules
- [ ] Draw Grids
- [ ] Highlight Substructures
- [ ] Export Images

---

## 8. Molecular Graphs (GNN Preparation)

- [ ] Atoms as Nodes
- [ ] Bonds as Edges
- [ ] Atom Features
- [ ] Bond Features
- [ ] Mol → Graph Conversion
- [ ] PyTorch Geometric Integration

---

## 9. Dataset Processing

- [ ] Read SMILES Dataset
- [ ] Molecule Validation
- [ ] Invalid SMILES Removal
- [ ] Canonicalization
- [ ] Deduplication

---

## 10. Drug Discovery Essentials

- [ ] ChEMBL Data Processing
- [ ] PubChem Data Processing
- [ ] Descriptor Generation
- [ ] Fingerprint Generation
- [ ] QSAR Features
- [ ] DTI Feature Engineering

---

# Optional (Later)

- [ ] Conformers
- [ ] 3D Coordinates
- [ ] UFF/MMFF Optimization
- [ ] Murcko Scaffold
- [ ] BRICS Fragmentation
- [ ] Reaction SMARTS
- [ ] CXSMILES / CXSMARTS
- [ ] Pharmacophore Features

---

# Ignore for Now

- [ ] RDKit C++ Internals
- [ ] Polymer Chemistry Features
- [ ] Substance Groups
- [ ] Advanced QueryQuery Matching
- [ ] Rare Organometallic Edge Cases

---

# Target Outcome

- [ ] Read SMILES
- [ ] Generate Descriptors
- [ ] Generate Fingerprints
- [ ] Perform SMARTS Search
- [ ] Convert Molecule to Graph
- [ ] Train GNN
- [ ] Build DTI Pipeline

### Resources
- [ ] https://github.com/nrflynn2/ml-drug-discovery
- [ ] https://greglandrum.github.io/rdkit-blog/?utm_source=chatgpt.com
- [ ] https://projects.volkamerlab.org/teachopencadd/?utm_source=chatgpt.com
- [ ] https://docs.datamol.io/stable/
  
  
