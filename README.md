# 🏪 Store Sales Forecasting

Forecasting store sales using time series data and machine learning techniques.

---

🧪 Approach

 📊 Exploratory Data Analysis (EDA)
- Analyzed sales by store and product family.  
- Handled missing values.  
- Detected seasonal patterns and long-term trends.  

 ⚙️ Feature Engineering
- Created lag features: `lag_7`, `lag_14`, `lag_28`.  
- Added rolling mean features: `rmean_7`, `rmean_14`, `rmean_28`.  
- Included promotion and holiday features.  
- Built custom features like `days_since_last_nonzero` and `zero_count`.  
- Aggregated group means by `store_nbr` and `family`.

 🤖 Model Training
- Used time-based cross-validation.  
- Trained models using **XGBoost** 
- Selected the best iteration using early stopping.  
- Calculated performance metrics (RMSE, MAE, R²).

 🧾 Evaluation
- Evaluated model performance across folds.  
- Extracted feature importances.  
- Calculated feature gain and cumulative importance.
---

 📈 Results

| Metric | Value |
|--------|--------|
| RMSE | 115.61 |
| MAE | 8.99 |
| R² | 0.988 |

**Top Features:**  
'rmean_7', 'days_since_last_nonzero', 'rmedian_7', 'ewm_7_alpha0.9', 'roll_sum_7', 'lag_7', 'lag_1', 'ewm_7_alpha0.7'
---

🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/03_Modeling.ipynb


🧰 Tech Stack

Python (Pandas, NumPy, Scikit-learn, XGBoost )

Matplotlib / Seaborn

Jupyter Notebook
