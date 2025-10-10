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
- **Fig 1 — Clustering:** `fig1_clustering.png` — UMAP colored by Leiden/Louvain  
- **Fig 2 — Markers:** `fig2_markers.png` — UMAP of top markers in the ROC-like cluster  

---

## Data
- **Input:** `cleaned_processed_frogtail.h5ad` (processed single-cell data from starter kit)  
- **Output:** `Frogtail_processed_results.h5ad` (optional — includes clustering and marker tables)  

---

## Code Availability
- **GitHub repository:** [this repo](https://github.com/Chi123Zhang/frog-tail-regeneration)  
- **Colab (one-click run):** [Open in Colab](https://colab.research.google.com/drive/1n-zwzKfbmK6F8lzEAfzpKAyjfyKSeYqH#scrollTo=JFrM4u5k9-8m)  

---

## Reproducibility
To reproduce the full analysis:

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Open the notebook and run all cells
cd notebooks/
jupyter notebook Frog_and_tail_ChiZhang.ipynb
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
