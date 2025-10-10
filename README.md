# frog-tail-regeneration
Mini Project 1 for Single-Cell Biology: Identifying the Regenerative Organizing Cell (ROC) in the Frog Tail
**Course:** Single-Cell Biology  
**Author:** Chi Zhang (cz2925@columbia.edu)  
**Repository:** Public for submission  
**Goal:** Identify the Regenerative Organizing Cell (ROC) in the *Xenopus* tail using clustering and marker gene analysis.

---

## Abstract
We identify the regenerative organizing cell population in the frog tail through single-cell transcriptomic clustering and gene marker comparison with Supplementary Table 3 from [1].

---

## Overview
This repo reproduces a minimal single-cell RNA-seq pipeline on *Xenopus* tail:
- Preprocessing (normalize/log1p/HVG)
- PCA + UMAP
- Clustering (Louvain, Leiden)
- Marker selection (t-test, logistic regression)
- Quality (ARI, silhouette)
- Denoising (PCA truncation, regress-out + neighborhood smoothing)
- **Comparison to Supplementary Table 3 (ligands/receptors & ROC markers)**

---

## Figures
- `fig1_clustering.png`: UMAP colored by Leiden/Louvain
- `fig2_markers.png`: UMAP of top markers in the ROC-like cluster

## Data
- Input: `cleaned_processed_frogtail.h5ad` (path ...)
- Output: `Frogtail_processed_results.h5ad` (optional)

## Code Availability
- GitHub: this repo  
- Colab (one-click run): 

## Repro
```bash
pip install -r requirements.txt
open the notebook under notebooks/ and Run All
```


## 📚 Reference Materials

1. **Main Paper [1]:** *Identification of a regeneration-organizing cell in the Xenopus tail*  
   [Nature Biotechnology (2025)](https://www.nature.com/articles/s41587-025-02694-w)

2. **Supplementary Material:** [Download Link](https://www.nature.com/articles/s41587-025-02694-w#Sec22)

3. **Starter Kit:** [Frog and tail.ipynb](./Frog_and_tail.ipynb)

4. **Single-cell Biology Help:**  
   [EBI Bioinformatics for Immunologists 2024 (GitHub)](https://github.com/noHup-cc/EBI_Bioinformatics_for_Immunologists_2024)

5. **Tutorials:**  
   [Scanpy Official Tutorials](https://scanpy.readthedocs.io/en/stable/tutorials.html)

6. **Visualization Tools:**  
   - [Adobe Color Wheel](https://color.adobe.com/create/color-wheel)  
   - [Ten Simple Rules for Better Figures | PLOS Computational Biology](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003833)

7. **Formatting Resources:**  
   - [Nature Communications Submission Guidelines](https://www.nature.com/ncomms/submit/article)  
   - [Overleaf LaTeX Editor](https://www.overleaf.com/)  
   - [GitHub Getting Started Guide](https://docs.github.com/en/get-started/start-your-journey)
