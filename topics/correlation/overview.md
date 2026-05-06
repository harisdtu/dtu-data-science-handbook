# Correlation Coefficients

## What it is
Correlation measures the **strength and direction of a relationship** between two variables.

---

## Classical correlation measures
- **Pearson** → linear relationships (sensitive to outliers)  
- **Spearman** → rank-based, monotonic, more robust  
- **Kendall** → rank-based, robust, suitable for small datasets  

---

## Key limitation
Correlation fails for **nonlinear, non-monotonic relationships** (e.g. U-shape)  
→ **Low correlation ≠ independence**

---

## Advanced dependence measures

### Maximal Information Coefficient (MIC)
- **Idea:** captures linear + nonlinear relationships via mutual information  
- **Range:** [0, 1] (0 = none, 1 = strong)  
- **Use:** nonlinear detection, EDA, feature selection  
- **Pros:** flexible, no functional assumption, equitable  
- **Cons:** expensive, less interpretable, sample-size sensitive  

---

### Xi correlation (ξ)
- **Idea:** measures general dependence via predictability of ordering  
- **Range:** [0, 1] (0 = independent, 1 = dependent)  
- **Use:** unknown / nonlinear relationships  
- **Pros:** captures general dependence, simple interpretation, efficient  
- **Cons:** does not describe relationship form, less common, noise-sensitive  

---

## Quick comparison
| Method | Captures |
|--------|----------|
| Pearson | Linear |
| Spearman | Monotonic |
| Kendall | Monotonic (robust) |
| MIC | Nonlinear |
| ξ | General dependence |

---

## Notebook (interactive example)
📄 [notebooks/DS_correlations.ipynb](../../notebooks/DS_correlations.ipynb)
▶️ https://colab.research.google.com/github/harisdtu/dtu-data-science-handbook/blob/main/notebooks/DS_correlations.ipynb
