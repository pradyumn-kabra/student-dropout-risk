# Student Dropout Risk Prediction

A machine learning project to predict student dropout risk from academic and engagement features. 
Built as a portfolio-ready project showcasing end‑to‑end workflow: **EDA → Modeling → Evaluation → Insights**.

> **Highlights**
> - Dataset: ~500 records, 15 features (e.g., GPA, attendance, engagement metrics)
> - Supervised model: **K‑Nearest Neighbors (KNN)** (baseline accuracy ~85%)
> - Unsupervised analysis: **K‑Means** to explore natural student segments
> - Clean, reproducible setup with `requirements.txt` and clear run steps

---

## 🔧 Tech Stack
- Python 3.9+
- pandas, numpy
- scikit‑learn
- matplotlib, seaborn (for EDA)
- jupyter / jupyterlab
- joblib (for saving models)

---

## 📁 Repository Structure (suggested)
```
student-dropout-risk/
├─ data/
│  ├─ raw/               # raw datasets (keep private if needed)
│  └─ processed/         # cleaned/engineered datasets
├─ notebooks/
│  ├─ 01_eda.ipynb
│  └─ 02_modeling_knn.ipynb
├─ src/
│  ├─ train.py           # optional: script version of training
│  └─ evaluate.py        # optional: script for evaluation/inference
├─ models/
│  └─ dropout_knn.pkl
├─ reports/
│  └─ images/            # EDA charts, confusion matrix, ROC, etc.
├─ README.md
└─ requirements.txt
```

> You can adapt the structure to what you already have; the goal is to keep it tidy and easy to navigate.

---

## 🚀 Quickstart

### 1) Clone the repository
```bash
git clone https://github.com/yourusername/student-dropout-risk.git
cd student-dropout-risk
```

### 2) Create a virtual environment (recommended)
**Windows (PowerShell):**
```bash
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3) Install dependencies
```bash
pip install -r requirements.txt
```

### 4) Run the project
**Option A — Jupyter Notebooks**
```bash
jupyter notebook
# open notebooks/01_eda.ipynb and notebooks/02_modeling_knn.ipynb
```

**Option B — Python scripts (if you use them)**
```bash
python src/train.py       # trains the model and saves to models/dropout_knn.pkl
python src/evaluate.py    # loads the model and prints metrics
```

> If your dataset is private, place it under `data/raw/` and update paths inside your notebook/script.

---

## 🧹 Data Notes
- Typical features: GPA, attendance %, prior failures, participation/engagement scores, etc.
- Handle missing values, encode categoricals, and scale numeric features for KNN.
- Split into train/test (e.g., 80/20) with `random_state=42` for reproducibility.

---

## 📊 Results (example)
| Model | Accuracy | F1-Score | Notes |
|------|---------:|---------:|------|
| KNN (k=5) | ~0.85 | ~0.83 | Tuned via GridSearchCV |
| Baseline (most frequent) | ~0.50 | ~0.33 | Baseline for comparison |

> Replace with your actual metrics. Add charts like confusion matrix, ROC/AUC in `reports/images/` and embed them below:
>
> ```markdown
> ![Confusion Matrix](reports/images/confusion_matrix.png)
> ![ROC Curve](reports/images/roc_curve.png)
> ```

---

## ⚙️ Reproducibility
- Set seeds: `numpy` / `scikit-learn` with `random_state=42`.
- Keep environments consistent using `requirements.txt` (see below). To update it from your env:
```bash
pip freeze > requirements.txt
```

---

## 📚 References
- Scikit‑learn Docs: https://scikit-learn.org/stable/
- pandas Docs: https://pandas.pydata.org/

---

## 👤 Author
**Pradyumn Kabra**  
LinkedIn: https://www.linkedin.com/in/your-linkedin

> Replace the LinkedIn URL with your profile link.

---

## 🔒 License
This project is for educational purposes. If you want an open‑source license, consider MIT:
```text
MIT License — Copyright (c) 2025 Pradyumn Kabra
Permission is hereby granted, free of charge, to any person obtaining a copy...
```
