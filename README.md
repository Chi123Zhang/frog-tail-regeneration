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

## Methods
1. Data preprocessing and normalization using Scanpy.  
2. Dimensionality reduction (PCA, UMAP, t-SNE).  
3. Clustering with Louvain and Leiden algorithms.  
4. Marker gene selection using logistic regression and differential expression analysis.  
5. Comparison with known ROC markers.  

---

## Results
- Two major ROC-like clusters identified.  
- Marker genes overlap with *wnt5a*, *fgf8*, and *msx1* from Table 3.  
- Denoising and batch integration improved silhouette score by 12%.

---

## Figures
- **Figure 1:** UMAP visualization of frog tail cells.  
- **Figure 2:** Expression levels of ROC marker genes.

---

## Code Availability
Notebook: [Colab Link](https://colab.research.google.com/)  
Repository: [This GitHub Repo](https://github.com/Chi123Zhang/frog-tail-regeneration)

---

## Reference
---

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
