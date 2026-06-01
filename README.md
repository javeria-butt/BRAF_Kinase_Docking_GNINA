# BRAF_Kinase_Docking_GNINA

## High-Resolution Molecular Docking Pipeline: Human B-Raf Kinase Domain vs. Lingand Dabrafenib

This repository implements a two-phase structural bioinformatics pipeline to evaluate the small-molecule interaction landscape of the **human B-Raf proto-oncogene, serine/threonine kinase (BRAF)**. Leveraging state-of-the-art computational frameworks for both macromolecular structural prediction (**AlphaFold Server**) and machine learning-driven structural binding evaluation (**GNINA**), this project provides an end-to-end simulation workflow targeting oncogenic kinase signaling.

---

## Repository Architecture

The project files are organized into clean, modular subdirectories to ensure transparency and computational reproducibility. Click on any file below to explore the data directly:

```text
BRAF_Kinase_Docking_GNINA/
│
├── Data/
│   ├── [braf_dna.fasta](Data/braf_dna.fasta)               # Input genomic DNA template sequence
│   ├── [braf_mrna.fasta](Data/braf_mrna.fasta)             # Transcribed mRNA sequence output (Notebook 1)
│   ├── [braf_protein.fasta](Data/braf_protein.fasta)          # Reference primary amino acid sequence (Notebook 1)
│   └── [dabrafenib_ligand.sdf](Data/dabrafenib_ligand.sdf)       # 3D optimized ligand conformation via RDKit
│
├── Structures/
│   ├── [fold_braf_structure.cif](Structures/fold_braf_structure.cif)      # Native 3D coordinates downloaded from AlphaFold Server
│   └── [braf_structure.pdb](Structures/braf_structure.pdb)           # Converted receptor model via Open Babel (Notebook 1)
│
├── Notebooks/
│   ├── [BRAF_Sequence_to_Structure_Prep.ipynb](Notebooks/BRAF_Sequence_to_Structure_Prep.ipynb)  # Phase 1: Sequence Processing & Structural Conversion
│   └── [BRAF_Molecular_Docking_GNINA.ipynb](Notebooks/BRAF_Molecular_Docking_GNINA.ipynb)      # Phase 2: CNN-Driven Molecular Docking & Analytics
│
├── Results/
│   ├── [braf_docking_results.png](Results/braf_docking_results.png)     # Final thermodynamic binding affinity bar chart
│   └── [docking_output.sdf](Results/docking_output.sdf)       # Multi-pose coordinate matrix containing the 9 generated poses
│
└── README.md                        # Master repository documentation
```
