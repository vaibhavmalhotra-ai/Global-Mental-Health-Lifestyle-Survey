# 🧠 Global Mental Health & Lifestyle Survey — ML Prediction Project

> **Predicting mental health outcomes using supervised machine learning on a dataset of 10,000 individuals across 50 lifestyle, demographic, and psychological features.**

---

## 📌 Project Overview

Mental health issues are increasingly prevalent yet often go undetected until they become severe. This project builds a **binary classification model** to predict whether an individual has a mental health issue (`Has_Mental_Health_Issue`: 0 = No, 1 = Yes), using lifestyle habits, demographic data, work conditions, and psychological symptoms.

The project is structured around **7 Research Questions (RQs)**, each addressed in a separate Jupyter Notebook.

---

## 📂 Repository Structure

```
├── RQ1_Baseline_Models.ipynb
├── RQ2_Model_Comparison.ipynb
├── RQ3_Lifestyle_Factors.ipynb
├── RQ4_Feature_Importance.ipynb
├── RQ5_Preprocessing_Impact.ipynb
├── RQ6_Model_Stability.ipynb
├── RQ7_Deployment_Readiness.ipynb
├── results/
│   ├── RQ1_table.csv
│   ├── RQ2_table.csv
│   ├── RQ3_table.csv
│   ├── RQ4_table.csv
│   ├── RQ5_table.csv
│   ├── RQ6_table.csv
│   ├── RQ7_metrics_table.csv
│   ├── RQ7_cv_table.csv
│   ├── RQ7_threshold_table.csv
│   ├── RQ1_figure.pdf
│   ├── RQ2_figure.pdf
│   ├── RQ3_figure.pdf
│   ├── RQ4_figure.pdf
│   ├── RQ5_figure.pdf
│   ├── RQ6_figure.pdf
│   └── RQ7_figure.pdf
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

| Field | Details |
|---|---|
| **Name** | Global Mental Health & Lifestyle Survey Dataset |
| **Source** | [Kaggle — Dhrubang Talukdar](https://www.kaggle.com/datasets/dhrubangtalukdar/global-mental-health-and-lifestyle-survey-dataset/data?select=mental_health.csv) |
| **Rows** | 10,000 |
| **Columns** | 51 (50 features + 1 target) |
| **Target Variable** | `Has_Mental_Health_Issue` (0 = No, 1 = Yes) |
| **Task Type** | Binary Classification |

### ⬇️ How to Download the Dataset

1. Go to the [Kaggle dataset page](https://www.kaggle.com/datasets/dhrubangtalukdar/global-mental-health-and-lifestyle-survey-dataset/data?select=mental_health.csv)
2. Click **Download** (you need a free Kaggle account)
3. Extract and place `mental_health.csv` in your working directory
4. On **Kaggle Notebooks**, the file is available at:
   ```
   /kaggle/input/mental-health-dataset/mental_health.csv
   ```

---

## 🔬 Research Questions

| RQ | Research Question |
|---|---|
| **RQ1** | How effectively can baseline supervised learning models predict mental health risk? |
| **RQ2** | Which supervised learning model provides the most accurate prediction, and how do ensemble models compare with traditional models? |
| **RQ3** | How do key lifestyle factors (sleep, physical activity, screen time, social interaction) influence predictive performance? |
| **RQ4** | Which lifestyle and demographic features are the strongest predictors of poor mental health outcomes? |
| **RQ5** | How do preprocessing techniques (missing values, encoding, scaling) affect model performance? |
| **RQ6** | How stable is the selected model across different validation strategies and under noisy or incomplete data? |
| **RQ7** | Can the developed model be reliably used as an early mental health risk detection tool for digital health platforms? |

---

## 🤖 Models Used

- Logistic Regression *(baseline)*
- Random Forest *(ensemble)*
- Support Vector Machine — SVM *(traditional)*
- XGBoost *(ensemble — primary model)*

---

## 📈 Evaluation Metrics

| Metric | Why It Matters |
|---|---|
| **F1-Score** | Primary metric; balances Precision and Recall under class imbalance |
| **Recall** | Minimizes missed at-risk individuals |
| **Precision** | Reduces false alarms |
| **AUC-ROC** | Overall model discrimination ability |
| **Specificity** | True negative rate for healthy individuals |
| **Accuracy** | General reference metric |

---

## ⚙️ How to Run

### Option A — Kaggle Notebooks *(Recommended)*

1. Upload each `.ipynb` file to [Kaggle Notebooks](https://www.kaggle.com/code)
2. Add the dataset via **Add Data → Search "Global Mental Health Lifestyle Survey"**
3. Run each notebook independently from top to bottom using **Run All**

### Option B — Local Machine

1. Clone this repository:
   ```bash
   git clone https://github.com/vaibhavmalhotra-ai/Global-Mental-Health-Lifestyle-Survey
   cd mental-health-ml
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset from Kaggle and place `mental_health.csv` in the project folder

4. Update the dataset path in each notebook:
   ```python
   # Change this line in each notebook
   df = pd.read_csv("/kaggle/input/mental-health-dataset/mental_health.csv")

   # To this for local run
   df = pd.read_csv("mental_health.csv")
   ```

5. Launch Jupyter and run each notebook:
   ```bash
   jupyter notebook
   ```

---

## 📋 Requirements

See [`requirements.txt`](requirements.txt) for the full list. Key libraries:

```
pandas
numpy
scikit-learn
xgboost
matplotlib
jupyter
```

---

## 📁 Results

All generated tables (`.csv`) and figures (`.pdf`) are saved in the `results/` folder after running each notebook.

---

## ⚠️ Important Notes

- The dataset has a **class imbalance** (92% positive, 8% negative) — use F1-Score and Recall as primary metrics, not Accuracy alone
- All notebooks are **self-contained** — each one loads, encodes, and preprocesses the data independently
- Notebooks are designed to run on **Kaggle** but work locally with a path change (see above)

---

## 📜 License

This project is for academic research purposes only.
