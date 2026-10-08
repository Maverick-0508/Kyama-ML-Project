# KYAMA: Financial Inclusion Pipeline for Informal Workers

A hybrid machine learning framework designed to strengthen financial inclusion and address credit readiness among informal sector workers (e.g., Mama Mbogas, Boda Boda operators) in Kenya. Built using Python, Scikit-Learn, and Google Colab.

## 🚀 Active Project State & Architecture
- **Data Scope:** 6,068 Kenyan household records processed.
- **Unsupervised Model:** K-Means Clustering (3 distinct worker profiles generated).
- **Supervised Model:** Random Forest Classifier optimized with SMOTE resampling.
- **Explainability Suite:** Integrated SHAP (Shapley Additive exPlanations).

## 📊 Current Metric Baseline
- **Supervised Area Under Curve (ROC-AUC):** 0.7797 (Baseline) | 0.7780 (SMOTE Optimized)
- **Target Optimization:** Successfully elevated `Has Account` Recall from 49% to 57% to address institutional gender and rural exclusion biases.

## 🔍 Key Findings & Insights

### Fairness Analysis (Recall for 'Has Account' Class):
- **Gender:**
  - Female Slot | Account Detection Rate (Recall): 41.4%
  - Male Slot | Account Detection Rate (Recall): 54.4%
- **Location:**
  - Rural Slot | Account Detection Rate (Recall): 36.8%
  - Urban Slot | Account Detection Rate (Recall): 57.0%

*Note: SMOTE resampling significantly improved 'Has Account' recall, helping to mitigate observed biases.*

### Feature Importance:
The model's predictions are primarily driven by:
1.  **Age of Respondent**
2.  **Education Level**
3.  **Household Size**
4.  **Job Type**
5.  **Worker Profile Cluster** (our custom unsupervised segment)

### Worker Segment Profiles:
- **Segment 0:** Older (avg 63.1 years), smaller households (avg 3.1 members), predominantly Farming/Fishing, Rural.
- **Segment 1:** Younger (avg 33.5 years), average households (avg 3.4 members), predominantly Informally employed, Urban.
- **Segment 2:** Young (avg 31.6 years), larger households (avg 5.1 members), predominantly Farming/Fishing, Rural.

## 🛠️ How to Run This Project
1.  **Clone the Repository:** Download the project files to your local machine.
2.  **Open in Google Colab:** Upload the `KYAMA_Pipeline.ipynb` notebook to Google Colab.
3.  **Mount Google Drive:** Run the first cell to mount your Google Drive. Ensure your `KYAMA_ML_Project/data/` folder (containing `financial-inclusion-in-africa/Train.csv`, `Test.csv`, `VariableDefinitions.csv`) is correctly placed in `My Drive`.
4.  **Run All Cells:** Execute all cells in sequential order. The notebook will automatically perform data loading, preprocessing, clustering, supervised learning, and explainability analysis.

## 📁 Repository Directory Matrix
- `/data/` : Holds the proxy training sets.
- `KYAMA_Pipeline.ipynb` : The main execution pipeline synced with Google Colab.
