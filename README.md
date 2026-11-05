# 🏘️ A Proximity-Based Early Warning System for Gentrification in California


## 📌 Project Overview
This machine learning project aims to classify California Census tracts based on whether they experienced a positive housing cost increase during the **2012–2016** period using demographic, socio-economic, and spatial proximity data available prior to 2012.

The key hypothesis investigated is whether **spatial features** (such as pre-2012 housing/income changes in neighboring tracts and spatial clustering indicators) improve machine learning model performance in forecasting gentrification trends.

---

## 📊 Key Findings & Results
* **Best Model:** Regularized **XGBoost Classifier** evaluated on feature set `D_core` (10 core tract & spatial proximity features).
* **Held-Out Test Performance:**
  * **ROC-AUC:** `0.6398` (95% CI: 0.591 – 0.694)
  * **Accuracy:** `60.65%` (Baseline majority-class: 51.63%)
  * **Precision:** `58.82%` | **Recall:** `62.18%` | **F1-Score:** `0.6045`
* **Spatial Impact:** Feature importance and ablation studies confirm that spatial features (e.g., `spatial_lag_housing_pre2012` and tract-vs-neighbor contrasts) contribute significantly to early warning predictions.

---

## Quick Setup & Running Instructions
* Option A: Running on Google Colab
Open notebooks/gentrification_final.ipynb in Google Colab.

Upload the model-ready CSV dataset from the data/ folder to your Colab session.

Update the DATA_PATH variable in the notebook to point to your dataset location.

Execute all cells (Ctrl + F9).
* Option B: Local Setup
Clone the repository:
git clone [https://github.com/Zaid5172/Gentrification_California.git](https://github.com/Zaid5172/Gentrification_California.git)
cd Gentrification_California

Install required dependencies:
pip install pandas numpy scikit-learn xgboost scipy matplotlib seaborn jupyter

Launch the Jupyter Notebook:
jupyter notebook notebooks/gentrification_final.ipynb




