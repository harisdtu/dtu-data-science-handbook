# Correlation Coefficients

## What it is
Correlation measures the **strength and direction of a relationship** between two variables.

---

# Classical Correlation Measures

## Pearson Correlation
- Measures **linear relationships**
- Sensitive to outliers

## Spearman Correlation
- Rank-based
- Captures **monotonic relationships**
- More robust to outliers

## Kendall Correlation
- Rank-based
- Suitable for **small datasets**
- Robust to noise

---

## When to use (summary)

| Situation | Method |
|----------|--------|
| Linear relationship | Pearson |
| Monotonic (nonlinear) | Spearman |
| Small / noisy data | Kendall |

---

## When NOT to use
- Non-monotonic relationships (e.g. U-shaped data)
- Presence of strong outliers (for Pearson)
- Interpreting correlation as causality

---

## Key limitation
Correlation measures can fail when relationships are **nonlinear and non-monotonic**.

### Example
Temperature vs energy consumption often shows a **U-shape**:
- Pearson → ≈ 0  
- Misleading despite strong dependence  

---

# Advanced Dependence Measures

## Maximal Information Coefficient (MIC)

### What it is
Measures dependence using **mutual information**, capturing both **linear and nonlinear relationships**.

### Key idea
- Pearson → linear  
- Spearman → monotonic  
- MIC → **any functional relationship**

### Range
MIC ∈ [0, 1]  
- 0 → no relationship  
- 1 → strong relationship

### When to use
- Detecting nonlinear relationships
- Exploratory analysis
- Feature selection

### Advantages
- Flexible (captures many relationship types)
- Equitable across noise levels
- No functional assumption

### Limitations
- Computationally expensive
- Less interpretable
- Sensitive to sample size
- Not standard in workflows

---

## Xi Correlation Coefficient (ξ)

### What it is
Measures **general statistical dependence** by checking whether X provides information about Y.

### Key idea
- Detects **any type of dependence**
- Based on predictability of ordering

### Range
ξ ∈ [0, 1]  
- 0 → independence  
- 1 → strong dependence  

### When to use
- Unknown or nonlinear relationships
- Exploratory analysis
- When classical correlation fails

### Advantages
- Captures general dependence
- Simple interpretation (0 = independent)
- Efficient compared to MIC

### Limitations
- Does not describe relationship form
- Less widely adopted
- Can be sensitive in small samples

---

# Practical Insight

For **nonlinear relationships (e.g. U-shape)**:

| Method | Output |
|------|------|
| Pearson | ≈ 0 |
| Spearman | low |
| MIC | high |
| ξ | high |

👉 Low Pearson ≠ independence

---

# Related Concepts
- Mutual Information
- Distance Correlation
- Maximal Correlation
