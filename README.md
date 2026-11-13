# NASA-GeneLab-EDGE-Workflows

[![NASA OSDR Working Group](https://img.shields.io/badge/NASA-OSDR%20AWG-blue.svg)](https://genelab.nasa.gov/)
[![Platform](https://img.shields.io/badge/Platform-GeneLab%20EDGE%20%2F%20Nextflow-green.svg)](https://nasa.edgebioinformatics.org/)
[![Status](https://img.shields.io/badge/Status-Beta%20Testing%20&%20Pipeline%20Evaluation-orange.svg)]()

This repository documents the evaluation, beta testing feedback, and execution workflows for the **NASA GeneLab Amplicon Illumina Sequencing Data Processing Workflow (AmpIllumina)** within the NASA EDGE bioinformatics platform.

## 🔬 Overview & Objectives
As a member of the **NASA OSDR Microbes and Multi-Omics Analysis Working Group**, this workspace records practical explorations of Illumina amplicon sequencing data processing utilizing Nextflow DSL2 workflows, Singularity containers, and OSDR spaceflight datasets.

---

## ⚙️ Project Configuration & Parameters (`OSD-386`)
The execution parameters and pipeline configuration for the test project (`OSD-386_Test_Priti`) are structured as follows:

| Parameter | Configuration Setting | Description / Value |
| :--- | :--- | :--- |
| **Input Type** | Accession | Fetched directly from NASA OSDR |
| **Target Accession** | `OSD-386` | Spaceflight microbial / environmental sequencing dataset |
| **Target Region** | `16S` | Marker gene amplicon sequencing |
| **Filtering & Trimming** | Anchor Primers / Cutadapt | Anchor primers: `TRUE`, Min Cutadapt Length: `150`, Discard untrimmed: `TRUE` |
| **Error Control & Depth** | Max EE / Rarefaction | Left/Right max EE: `1`, Rarefaction Depth: `500` |
| **Statistical Methods** | Differential Abundance | Method: `all` (ANCOMBC1, ANCOMBC2, DESeq2) |

---

## 📊 Pipeline Results & Analytical Modules
* **Alpha Diversity:** Evaluated richness and evenness metrics (Observed features, Chao1, Shannon, and Simpson indices) across sample groups.
* **Beta Diversity:** Generated Bray-Curtis dissimilarity matrices and PCoA hierarchical clustering plots.
* **Taxonomy Profiling:** Mapped amplicon sequence variants (ASVs) across Phylum, Class, Order, Family, and Genus levels using the SILVA database.
* **Differential Abundance (DESeq2 / ANCOMBC):** Processed comparative abundance testing across experimental groups, generating comprehensive volcano plots and statistical significance tables. Handled low sample size edge cases gracefully via automated protocol logging.

---

## 🚀 Key Beta Testing Feedback & Insights
* **Platform Efficiency:** Seamless integration with OSDR accession retrieval (`OSD-386`) for rapid pipeline initiation.
* **Proposed Enhancements:** 
  * Integration of upfront dataset quality metrics (read depth, Phred scores).
  * Addition of automated interactive visualizations (dynamic stacked bar plots and heatmaps).
  * Implementation of proactive job-completion notifications and bulk download features (`.zip` archive exports).

---

## 👩‍💻 Author
**Priti Rooj**  
*M.Sc. in Biotechnology (University of Burdwan, Silver Medalist)*  
*NASA OSDR Microbes and Multi-Omics Analysis Working Group Member*
