<<<<<<< HEAD
# Walmart Sales Forecast

End-to-end sales forecasting project using Python, LightGBM, and advanced feature engineering. Includes **data preprocessing**, **model selection**, **hyperparameter tuning**, and **residual analysis** to evaluate model assumptions and performance.

---

## 📌 Highlights
- Full workflow in a single Jupyter notebook: from data cleaning to model evaluation
- **LightGBM** selected as the optimal model
- **Step 27 — Residual Analysis** to check non-linearity, heteroskedasticity, and outliers
- Clear visuals for residual diagnostics

---

## 📂 Project Structure
├─ notebooks/

│ └─ walmart_sales_forecast.ipynb

├─ src/ # utility functions

├─ data/ # (ignored) raw and intermediate data

├─ models/ # (ignored) trained models

├─ reports/

│ └─ figures/

│ ├─ residuals_vs_features.png

│ └─ residuals_vs_fitted.png

├─ requirements.txt

├─ .gitignore

└─ README.md


---

## 🧠 Approach
1. Load & clean Walmart sales data
2. Engineer features (lags, rolling means, calendar effects, promotions)
3. Compare models → select optimal LightGBM
4. Perform **Residual Analysis**:
   - Pairplot of residuals vs features
   - Residuals vs fitted values

---

## 📊 Residual Analysis
Residuals vs features (left) and vs fitted values (right):

<img src="reports/figures/residuals_vs_features.png" width="420"> <img src="reports/figures/residuals_vs_fitted.png" width="420">

**Interpretation guide:**
- Random scatter around 0 → good
- Curves or patterns → non-linearity
- Funnel shape → heteroskedasticity
- Extreme points → possible outliers

---

## How to Run

Follow these steps to set up and run the project locally.

### 1. Clone the repository
git clone https://github.com/Amin3502/Walmart-sales-forecast.git
cd Walmart-sales-forecast

### 2. Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows

### 3. Install dependencies
pip install -r requirements.txt

### 4. Run the notebook
Open Jupyter Notebook or Jupyter Lab and navigate to:
notebooks/your_notebook_name.ipynb
Run all cells to train the model and see results.

### 5. View generated figures
After running the notebook, residual plots will be saved in:
reports/figures/
You can also see example plots below.

---

## Example Plots

### Residuals vs Fitted
![Residuals vs Fitted](reports/figures/residuals_vs_fitted.png)

### Residuals vs Features
![Residuals vs Features](reports/figures/residuals_vs_features.png)
