# Genomic Alignment and Machine Learning Classification of Mpox Surface Protein Mutations Across Lineages

**Course:** ICS 4301 / Computing for Bioinformatics  
**Institution:** Strathmore University  
**Topic:** Mpox (Monkeypox) Surface Protein Evolution & Clade Distinction  

---

## 📌 Project Overview
This project investigates whether amino acid substitutions in key surface proteins (A29L / A35R) of recent Mpox (Monkeypox) viral strains display specific patterns that differentiate Clade I and Clade II lineages[cite: 1]. Using real biological data retrieved programmatically from NCBI Virus, we execute an end-to-end Python pipeline comprising data preprocessing, exploratory data analysis (EDA), multiple sequence alignment (MSA), phylogenetic tree reconstruction, and supervised machine learning classification evaluated against a dummy baseline[cite: 1, 2, 3, 5, 7].

---

## 👥 Group Members & Responsibilities

| Student Name | Admission No. | Primary Project Responsibilities |
| :--- | :--- | :--- |
| **Cindy Ogutu** *(Leader)* | **158842** | Project coordination, GitHub repository management, Stage 1 & 8 documentation |
| **Kristina Kemoi** | **168652** | Data acquisition via NCBI Entrez API & database source documentation (Stage 2) |
| **Dennis Mukoma** | **139360** | Data cleaning, filtering ambiguous bases, & quality control (Stage 3) |
| **Tracy Mugure Gitau** | **164643** | Exploratory Data Analysis (EDA) & sequence visualization (Stage 4) |
| **Janny Jonyo** | **166885** | Pairwise distance matrices, Multiple Sequence Alignment (MSA), & phylogenetics (Stage 5) |
| **Neema Mapelu** | **150176** | Feature encoding, machine learning classifier training (KNN/Random Forest), & baseline evaluation (Stage 6 & 7) |

---

## 🔬 Research Question & Objectives

### Research Question
> *"Do amino acid substitutions in Mpox surface proteins (A29L/A35R) distinguish Clade I from Clade II lineages, and can machine learning accurately classify isolates using these sequence features?"*[cite: 1]

### Objectives
1. **Data Acquisition & QC:** Retrieve, clean, and document FASTA surface protein sequences (A29L / A35R) for Mpox Clade I and Clade II isolates from the NCBI Virus database[cite: 1, 2, 3].
2. **Preprocessing & EDA:** Analyze sequence length distributions, trim alignment gaps, and extract amino acid composition feature vectors across viral isolates[cite: 2].
3. **Core Alignment Analysis:** Compute pairwise distance matrices, perform Multiple Sequence Alignment (MSA), and construct phylogenetic trees mapping clade divergence[cite: 2, 5].
4. **Machine Learning & Evaluation:** Train supervised classification models (KNN and Random Forest) on sequence feature vectors and evaluate performance against a dummy baseline classifier[cite: 1, 2, 5, 6].

### Hypothesis
Key amino acid substitutions alter sequence identity thresholds between Clade I and Clade II isolates, enabling supervised machine learning classifiers to distinguish clade origin with higher accuracy than dummy baseline models[cite: 1, 2].

---

## 📂 Project Workflow & Compulsory Stages

The project's Jupyter Notebook (`Mpox_Clade_Classification_Analysis.ipynb`) is organized into the compulsory 8 stages[cite: 1, 2]:

1. **Stage 1: Question & Objectives:** Problem formulation, hypothesis, and objective definition[cite: 1, 2].
2. **Stage 2: Data Acquisition:** Fetching protein FASTA files from NCBI Virus using `Bio.Entrez`[cite: 2, 3, 7].
3. **Stage 3: Preprocessing & Quality Control:** Filtering incomplete/ambiguous sequences (`X`/`?`) and verifying sequence integrity[cite: 2].
4. **Stage 4: Exploratory Data Analysis:** Sequence length histograms, clade balance bar charts, and amino acid frequency heatmaps[cite: 2].
5. **Stage 5: Core Analysis:** Multiple Sequence Alignment (MSA), identity matrix calculation, and Neighbor-Joining phylogenetic tree construction[cite: 2, 5].
6. **Stage 6: Biological Interpretation:** Mapping identified high-variability residue mutations back to functional receptor binding domains[cite: 1, 2].
7. **Stage 7: Machine Learning:** One-Hot encoding sequence features, training Random Forest & K-Nearest Neighbors (KNN) models, and scoring accuracy against a majority-class `DummyClassifier`[cite: 1, 2, 5, 6].
8. **Stage 8: Conclusions & Limitations:** Answering each research objective, documenting dataset limitations, and outlining future work[cite: 2].

---

## 💻 Installation & Dependencies

To execute this project locally or in Google Colab, install the required dependencies:

```bash
pip install biopython pandas numpy matplotlib seaborn scikit-learn
