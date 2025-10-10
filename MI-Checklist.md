# 🧾 MI-CLAIM Checklist  
**Source:** *Minimum Information about Clinical Artificial Intelligence Modeling (MI-CLAIM)*  
[https://www.nature.com/articles/s41591-020-1041-y/tables/1](https://www.nature.com/articles/s41591-020-1041-y/tables/1)

This checklist documents transparency, reproducibility, and methodological rigor for the project:  
**“Identification of Regenerative Organizing Cells (ROCs) in the *Xenopus* Tail”**  
by **Chi Zhang**, Columbia University, 2025.

---

## 🧩 Part 1. Study Design

| Requirement | Completed | Notes |
|--------------|------------|-------|
| The biological problem is clearly detailed in the paper. | Yes | ROC identification during *Xenopus* tail regeneration. |
| The research question is clearly stated. | Yes | Determine which clusters represent ROC-like populations. |
| The characteristics of datasets (training/test sets) are detailed. | Yes | scRNA-seq dataset from *Aztekin et al.*, 2019 (*Science*). |
| Cohorts are representative of the biological system. | Yes | Includes skin, muscle, and notochord cells from regenerative tissue. |
| Baseline comparison identified and detailed. | Yes | Compared to published ROC markers in Supplementary Table 3. |

---

## ⚙️ Part 2–3. Data and Optimization

| Requirement | Completed | Notes |
|--------------|------------|-------|
| Data origin and format described. | Yes | Public dataset from *Science* (2019) and EBI repository. |
| Transformations of the data before model application are described. | Yes | Log normalization, scaling, HVG selection, PCA (50 PCs). |
| Details of evaluated models provided. | Yes | Louvain vs Leiden clustering compared. |
| Input data type (structured/unstructured). | Yes Structured | Gene-expression matrix (cells × genes). |

---

## 📈 Part 4. Model Performance

| Requirement | Completed | Notes |
|--------------|------------|-------|
| Primary evaluation metric clearly stated. | Yes | Silhouette score ≈ 0.51 (BBKNN), 0.37 (Scanorama). |
| Clinical utility metric stated. | N/A | Non-clinical biological dataset. |
| Performance comparison between baseline and model shown. | Yes | ARI ≈ 0.81–0.87; Leiden preserved structure better than Louvain. |

---

## 🔍 Part 5. Model Examination

| Requirement | Completed | Notes |
|--------------|------------|-------|
| Examination technique 1 (e.g., feature importance). | Yes | Logistic-regression marker ranking (`sc.tl.rank_genes_groups(method='logreg')`). |
| Examination technique 2 (e.g., visualization). | Yes | UMAP colored by ROC markers (egfl6, nid2, pltp). |
| Discussion of result relevance. | Yes | ROC markers align with cluster 19 expression patterns. |
| Discussion of interpretability. | Yes | Marker-based interpretation allows clear biological insight. |
| Discussion of robustness. | Yes | Cluster topology consistent after batch correction (Scanorama & BBKNN). |

---

## ♻️ Part 6. Reproducibility Tier

| Tier | Description | Selected | Notes |
|------|--------------|-----------|-------|
| **Tier 1** | Complete sharing of the code | Yes | Full code and notebook available at [https://github.com/Chi123Zhang/frog-tail-regeneration/blob/main/Frog_and_tail_ChiZhang.ipynb] |
| **Tier 2** | Third-party evaluation only | ☐ | — |
| **Tier 3** | Virtual-machine binary | ☐ | — |
| **Tier 4** | No sharing | ☐ | — |

---

## Technical Environment

- **Language:** Python 3.12  
- **Packages:** `scanpy ≥ 1.9`, `bbknn`, `scanorama`, `matplotlib`, `numpy`, `pandas`  
- **Execution:** Fully runnable on Google Colab (GPU optional)  
- **Random seed:** Fixed for consistent clustering reproducibility  

---

##  References
1. Aztekin, C., Hiscock, T. W., Marioni, J. C., Gurdon, J. B., Simons, B. D., & Jullien, J. (2019).  
   *Identification of a regeneration-organizing cell in the Xenopus tail.* **Science**, 364(6441), 653–658.  
   [https://doi.org/10.1126/science.aav9996](https://doi.org/10.1126/science.aav9996)

---
