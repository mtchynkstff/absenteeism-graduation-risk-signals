# Absenteeism–Graduation Risk Signals

## Key Takeaway
Chronic absenteeism is meaningfully associated with graduation outcomes, but explains only a small share of the variation. Its greatest value lies in early risk stratification and residual-based prioritization—helping identify districts that miss graduation expectations even when attendance levels appear favorable.

## Overview
This project examines whether **chronic absenteeism can function as an early risk signal for graduation outcomes** at the U.S. school district (LEA) level. Using public federal education data, the analysis integrates school-level absenteeism from the Civil Rights Data Collection (CRDC) with district-level graduation rates from EDFacts.

Rather than attempting to predict graduation outcomes or claim causal effects, the project focuses on **risk stratification and prioritization**: identifying where absenteeism provides meaningful signal, where it does not, and how districts might decide **where to intervene first**.

---

## Key Questions
- How strongly is chronic absenteeism associated with graduation outcomes at the district level?
- Does absenteeism meaningfully differentiate graduation risk across districts?
- Which districts perform better or worse than expected given their attendance levels?
- How can attendance data be used responsibly to guide intervention priorities?

---

## Data Sources
- **Civil Rights Data Collection (CRDC), 2017–18**
  - School-level chronic absenteeism counts
  - Aggregated to districts using enrollment-weighted rates
- **EDFacts, 2017–18**
  - District-level four-year adjusted cohort graduation rates (ACGR)

The final analytic sample includes **3,341 districts** with enrollment ≥100 students and complete absenteeism and graduation data.

---

## Methodology (High Level)
1. **School → District Aggregation**  
   School-level absenteeism is aggregated to LEAs using enrollment-weighted rates to reflect student exposure.

2. **Descriptive Analysis**
   - Scatter plots
   - Correlation
   - Simple linear regression (one predictor, fully interpretable)

3. **Residual Analysis**
   - Compare actual graduation rates to rates predicted by absenteeism
   - Identify districts that significantly over- or under-perform expectations

The analysis is intentionally simple and transparent, prioritizing interpretability over model complexity.

---

## Key Findings
- **Negative but modest association:**  
  - Pearson correlation: **−0.16 (p < 0.001)**
  - Regression estimate: **+1 pp absenteeism ≈ −0.38 pp graduation**
  - Model explains **~3% of variance (R² ≈ 0.03)**

- **Risk stratification, not prediction:**  
  - Graduation rates decline from ~**85%** among districts with <5% absenteeism to ~**75%** among those above 20%.
  - Substantial variability exists at all absenteeism levels.

- **Residuals are highly informative:**  
  - Some districts graduate students **20–40 points above expectations** despite high absenteeism.
  - More concerning are districts with **low absenteeism but extremely low graduation rates**, missing expectations by **60–80 points**.

---

## Decision Insight
**Absenteeism is most useful as an early warning signal, not a standalone predictor.**

Districts that:
- have **low to moderate absenteeism**, but
- show **large negative graduation residuals**, and
- serve **substantial student populations**

should be prioritized for deeper diagnostic review and intervention. In these contexts, attendance alone is unlikely to be the binding constraint.

---

## Limitations
- The analysis is **correlational**, not causal.
- Graduation outcomes are available only at the district level for this year.
- Within-district variation is not observed.
- Other important predictors (course completion, credit recovery, program structure) are not included by design.

Results should be used for **prioritization and hypothesis generation**, not attribution.

---

## Repository Structure
```
├── data/
│ ├── raw/ # Original CRDC and EDFacts files
│ └── processed/ # Cleaned, analysis-ready datasets
├── notebooks/
│ ├── 01_build_lea_absenteeism_2017_18.ipynb
│ ├── 02_build_lea_graduation_2017_18.ipynb
│ ├── 03_merge_and_qc_2017_18.ipynb
│ ├── 04_analysis_and_insights_2017_18.ipynb
│ └── 05_residuals_and_prioritization_2017_18.ipynb
├── reports/
│ └── decision_memo.md
└── README.md
```

---

## Why This Project
This project emphasizes:
- Working with **messy, real-world public data**
- Making principled choices under **data availability constraints**
- Prioritizing **interpretability and judgment** over model complexity
- Translating analysis into **decision-relevant insights**

---

## How to Run
1. Place raw CRDC and EDFacts files in `data/raw/`
2. Run notebooks 01–03 to build processed datasets
3. Run notebooks 04–05 for analysis and prioritization

---

## Next Steps
Possible extensions include:
- Incorporating additional early indicators (course failure, mobility)
- Examining stability across multiple years
- Conducting qualitative follow-up on high-residual districts

---

*This project is intended as an applied data science portfolio artifact demonstrating end-to-end analysis, data judgment, and decision-oriented thinking.*
