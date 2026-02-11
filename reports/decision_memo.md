# Decision Memo: Using Chronic Absenteeism as an Early Risk Signal for Graduation Outcomes

## Context
This analysis examines whether chronic absenteeism can serve as a practical early risk signal for graduation outcomes at the district (LEA) level. Using 2017–18 public data, we combine school-level chronic absenteeism from the Civil Rights Data Collection (CRDC), aggregated to LEAs, with district-level graduation rates from EDFacts. The goal is not to establish causality, but to inform prioritization: **which districts should intervene first, and why**.

The final analytic sample includes **3,341 LEAs** with enrollment ≥100 students and complete absenteeism and graduation data.

---

## Key Findings

1. **Absenteeism is negatively associated with graduation, but explains limited variance.**  
   - Pearson correlation: **−0.16 (p < 0.001)**  
   - Simple OLS estimate: **+1 pp absenteeism ≈ −0.38 pp graduation rate**  
   - Model fit is low (**R² ≈ 0.03**), indicating most variation in graduation outcomes is driven by factors beyond absenteeism alone.

2. **Average graduation rates decline across absenteeism bands.**  
   - LEAs with **<5% absenteeism** average ~**85% graduation**.  
   - LEAs with **>20% absenteeism** average ~**75% graduation**.  
   - The steepest drop occurs between the lowest absenteeism band (0–5%) and the 5–10% band, after which declines are more gradual.

3. **Residuals reveal meaningful over- and under-performance.**  
   - Some LEAs graduate students **20–40 points above expectations** given very high absenteeism, suggesting mitigating supports or alternative pathways.  
   - More concerning are LEAs with **very low absenteeism (<5%) but extremely low graduation rates (<15%)**, missing expectations by **60–80 points**, often serving hundreds or thousands of students.

---

## Recommendation: Who Should Intervene First

**Priority should be given to LEAs with large negative graduation residuals**, particularly those that:
- Have **low to moderate absenteeism**, yet  
- Exhibit **graduation rates far below what absenteeism levels would predict**, and  
- Serve **substantial student populations**.

In these contexts, attendance does not appear to be the binding constraint. Interventions focused solely on absenteeism are unlikely to close graduation gaps; instead, these districts may face structural, programmatic, or pathway-related challenges that require targeted support.

Conversely, LEAs with large positive residuals represent **learning opportunities**. While not immediate intervention targets, they may warrant qualitative follow-up to identify practices that help mitigate attendance-related risk.

---

## Implications for Practice

- **Absenteeism should be used for early risk stratification, not prediction.**  
- **Residual-based prioritization** offers a practical way to allocate limited intervention resources.  
- Attendance data is most useful when combined with additional indicators (e.g., course completion, alternative pathways, student supports).

---

## Limitations
This analysis is correlational and conducted at the district level, which may mask within-district variation. Graduation outcomes are available only at the LEA level for this year, and the model intentionally excludes other predictors to preserve interpretability. Findings should be used to guide prioritization and hypothesis generation, not causal attribution.

---

**Bottom line:** Chronic absenteeism provides meaningful signal, but **who misses expectations matters more than who has high absenteeism alone**. Residuals offer a scalable, data-informed way to decide where to act first.
