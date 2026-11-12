# Hi, I'm André Fischer

Junior Data Analyst at OCL, working across data engineering and machine learning. Final-year Information Systems student at Multivix (graduating December 2026), based in Vitória, Brazil.

I build the path from a raw database to a business decision: SQL and dbt pipelines underneath, machine learning models on top, and documentation good enough that someone else can pick the work up. Coming from software QA, the part I care about most happens before training: checking that the data means what it seems to mean, removing features that leak the answer, and validating the model the way it will actually be used.

---

## Current work — OCL

- **Data engineering:** incremental dbt models and PostgreSQL functions on an Airbyte-fed warehouse, cutting query times from up to 375 s to under 1.5 s. The marts feed the company's AI agent through read-only, mart-only access.
- **Machine learning:** a multiclass model that recommends the most likely resolution for ~157k delinquent contracts. Read-only MySQL extraction, a modular Python pipeline, and an MLP vs. LightGBM benchmark under the same split and decision rule (LightGBM won, confirmed with a paired bootstrap). Includes a confidence threshold and an out-of-distribution flag so the model abstains where it would be unreliable.

*(Private company code — not published here.)*

---

## Featured projects

### [B2B Credit Default Prediction — Datarisk case](https://github.com/ASFischer/datarisk-case)
Probability that a business client's charge will be paid 5+ days late.
- Historical features computed "as of" each charge date, using only outcomes already known at that point (no temporal leakage).
- Out-of-time validation replicating the gap between development and test periods.
- **LightGBM — AUC 0.932, KS 0.748.**

### [Credit Default Model & Credit Policy — DS Accelerator (WeCogno)](https://github.com/ASFischer/dsaccelerator-tcc)
Probability of a 30+ day delay in the first 12 installments, plus a credit policy by risk band.
- 104k contracts, out-of-time split (train / validation / test by decision date).
- **LightGBM AUC 0.727 vs. 0.689 for logistic regression**, with confidence intervals, KS, Gini, Brier, calibration, PSI and SHAP.
- Risk bands (approve / approve with adjustment / reject), fairness checks by sex and age, and automated tests.

### [Medallion ETL Pipeline](https://github.com/ASFischer/etl-project)
Bronze → silver → gold pipeline in Python that enriches user data with the ViaCEP public API and loads it into PostgreSQL running on Docker.

### [Credit Card Default — cost-based threshold](https://github.com/ASFischer/credit_risk)
XGBoost on 30k clients (UCI dataset) with feature engineering, SHAP explanations and a decision threshold calibrated on asymmetric costs (a missed default costs ~16× a wrong refusal), simulated across three risk-appetite scenarios.

### [Industrial Predictive Maintenance](https://github.com/ASFischer/industrial-predictive-maintenance)
Failure prediction from 220k+ minute-level readings of 52 industrial sensors: cleaning, EDA, feature selection and a Random Forest classifier, with evaluation plots.

### [Neural Network from Scratch](https://github.com/ASFischer/neural-network)
A two-layer neural network implemented in NumPy (forward and backward propagation) on MNIST, compared with a Keras model.

---

## Stack

**Languages & ML:** Python (pandas, NumPy, scikit-learn, LightGBM, XGBoost, PyTorch, Keras, SHAP)
**Data:** SQL (PostgreSQL, MySQL), dbt, Airbyte, Docker
**BI & tools:** Power BI, Looker Studio, Git/GitHub, Jira, Postman

**Languages:** Portuguese (native) · English (C1) · Spanish (B2)

---

## Contact

- **LinkedIn:** [linkedin.com/in/andresouzafischer](https://www.linkedin.com/in/andresouzafischer/)
- **E-mail:** dedesfischer@gmail.com

Open to Data Scientist, Data Analyst and Analytics/Data Engineer roles.
