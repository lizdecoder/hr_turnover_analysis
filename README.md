# Turnover Drivers — Mini Case Study

**Goal**  
Pinpoint why employees quit and provide data-backed levers for retention.

**Dataset**  
Synthetic HR file (`fake_hr_turnover_data.csv`, 300 records) generated in Python, featuring tenure, engagement, performance, commute time, promotion history, and a voluntary-exit flag.

**Exported Artifacts**
- `fake_hr_turnover_data.csv` — Full employee dataset with turnover flags
- `correlation_matrix.csv` — Wide-format correlation matrix between numerical variables
- `hr_turnover_with_predictions.csv` — Includes predicted quit probability from logistic regression
- `log_reg_coefficients.csv` — Shows strength/direction of each predictor used in the logistic model

**Stack**
- **Python 3.12**: Pandas, Scikit-learn for data prep, correlation, linear and logistic regression  
- **Looker Studio**: Interactive visuals (trend line, heatmap table, scatter + trend, scorecards)

**Key Visuals & Findings**
1. **Turnover Trend (Line)** – Q1 exit surge → focus stay-interviews before bonus season.  
2. **Correlation Heatmap (Table)** – Low engagement (–0.50) & long commutes (+0.40) top risk indicators.  
3. **Commute vs Exit (Scatter)** – Each 10-min commute increase adds ~1.5 pp quit risk.  
4. **Logistic Regression** – 5-factor model, ROC-AUC 0.79, confirms engagement & commute as primary levers.

**Run It Yourself**
1. `pip install -r requirements.txt`  
2. Run `turnover_notebook.ipynb` to recreate the dataset and exported files  
3. Upload the following to [lookerstudio.google.com](https://lookerstudio.google.com):
   - `fake_hr_turnover_data.csv`
   - `correlation_matrix.csv`
   - `hr_turnover_with_predictions.csv`
   - `log_reg_coefficients.csv`
4. Follow `/docs/dashboard_setup.md` for visual configuration steps

**Business Impact**
Insights support flexible-work policies, engagement pulse checks, and commute-focused retention incentives—practical steps to curb predicted turnover by up to **15 %**.
