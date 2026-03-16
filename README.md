# LinkedIn Job Postings Analysis (2023–2024)

Exploratory analysis of 123,849 LinkedIn job postings covering skills demand, salary distributions, and compensation drivers across industries — with a LightGBM salary estimator at the end.

---

## Key Results

| Metric | Value |
|---|---|
| Total postings analyzed | 123,849 |
| Unique companies | 24,474 |
| Salary records (normalized) | 33,520 |
| Median annual salary | $91,337 |
| Mean annual salary | $104,630 |
| Salary IQR | $59,974 – $133,000 |
| Model MAE | $32,271 |
| Model RMSE | $49,366 |
| Model R² | 0.41 |

---

## Highlights

- **Industry is the strongest compensation driver.** The gap between the highest and lowest-paying industries exceeds $100K in median annual salary — sector selection matters more than seniority when predicting pay from structural features alone.

- **Contract roles command a real premium over full-time.** Median annual salary for Contract positions is $101,920 vs. $92,500 for Full-time, consistent with the market compensating for reduced stability and absence of benefits.

- **Mid-size companies are more competitive on salary than commonly assumed.** The 11–50 employee band shows the highest median salary ($95,137), matching or exceeding large enterprises (5,001+: $88,660) — likely driven by the weight of tech and finance startups in that tier.

- **Experience-level gradient is clean but the Entry-level floor is low.** The step from Associate ($75,920) to Mid-Senior ($110,000) represents a 45% salary increase. Entry-level median of $58,248 suggests many such roles are located in lower-cost markets or are effectively part-time in scope.

- **Benefits count does not predict salary.** Postings with zero benefits listed show a median salary of $92,500 — higher than most multi-benefit tiers. High-paying contract and senior roles rarely disclose benefits; lower-paying corporate roles compensate with extensive packages.

- **Soft skills dominate the demand landscape.** Communication, Management, and Customer Service rank ahead of every technical skill in overall frequency. With only 35 distinct skill codes in the dataset, the taxonomy is directional but not granular enough to identify hard-skill premiums by role type.

---

## Notebook Structure

| Section | Description |
|---|---|
| Problem Context | Dataset origin, analytical framing, and business relevance |
| Objectives | Five analytical questions the notebook addresses |
| Data Loading | Eleven relational files loaded from Kaggle input path |
| Postings Overview | Null rate audit, work type and experience level distributions |
| Top Industries | Volume ranking across 422 classified industries |
| Company Size | Distribution of postings by LinkedIn employee count bands |
| Most In-Demand Skills | Top 25 global skills + top 10 per industry for the 5 largest sectors |
| Salary Analysis | Distribution, salary by experience level, industry, work type, and company size |
| Benefits Analysis | Benefit frequency ranking and relationship between benefit count and salary |
| Skills Count vs. Salary | Median salary as a function of number of required skills per posting |
| Data Treatment | Modeling dataset assembly, ordinal encoding, null handling |
| Modeling | LightGBM regressor with early stopping |
| Evaluation | MAE, RMSE, R², MAPE, actual vs. predicted scatter, feature importance, residuals, MAE by experience level |
| Conclusion | Findings grounded in observed values, confirmed/refuted hypotheses, practical implications |

---

## Stack

pandas · numpy · matplotlib · seaborn · scikit-learn · lightgbm

---

## How to Run

1. Go to [Kaggle](https://www.kaggle.com) and create a new notebook
2. Attach the dataset: **LinkedIn Job Postings** (`arshkon/linkedin-job-postings`)
3. Import the `.ipynb` file via *File → Import Notebook*
4. Run all cells — no additional configuration required

---

## Data Source

[LinkedIn Job Postings (2023–2024) — Kaggle](https://www.kaggle.com/datasets/arshkon/linkedin-job-postings)
