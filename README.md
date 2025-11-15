# 🎯 CBU Coding Challenge 2025: AON Team Final Submission

## 🚀 Our Philosophy: All or Nothing

Welcome to the final submission repository for **Team AON (All or Nothing)**. Our goal was to deliver a state-of-the-art credit default prediction model that is not just statistically powerful, but also robust, interpretable, and commercially viable.

We successfully moved beyond the common AUC plateau of ~80% by implementing a sophisticated, multi-layered strategy focusing on **intelligent feature engineering** and a **powerful stacking ensemble**. This is our "All" — a complete, end-to-end solution.

---

## 📈 Our Winning Strategy: A Multi-Layered Approach

Our workflow was designed to systematically extract maximum predictive power from the data, culminating in a high-performance stacking ensemble.

### 1. **Deep EDA & Data Cleansing** `(Completed)`
- **"Garbage In, Garbage Out" is Not an Option:** We began by developing a robust automated pipeline to unify, clean, and standardize a diverse set of raw data files. We meticulously "defused" numerous data quality traps, such as inconsistent categorical values and malformed numeric fields.
- **IV-Driven Feature Selection:** Using the industry-standard **Information Value (IV)** metric, we evaluated every single feature. This allowed us to create a powerful baseline dataset (`alldata.csv`) by selecting only the features with proven predictive strength.
- **Notebook:** [`notebooks/1_EDA_AON.ipynb`](notebooks/1_EDA_AON.ipynb)

### 2. **"Golden Feature" Engineering** `(In progress)`
- **Beyond the Obvious:** To break the AUC barrier, we engineered a new set of "Golden Features" designed to capture complex, non-linear relationships that a model cannot find on its own. Highlights include:
  - **Advanced Financial Ratios:** Such as `income_to_loan_ratio` and `debt_to_credit_limit_ratio`.
  - **Behavioral & Demographic Proxies:** Like `age_to_credit_history_ratio` to model financial maturity.
  - **Unsupervised Learning:** We used **KMeans clustering** to create a powerful `customer_segment` feature, identifying natural client archetypes.
- **Notebook:** [`notebooks/2_Feature_Engineering_AON.ipynb`](notebooks/2_Feature_Engineering_AON.ipynb)

### 3. **OOF Stacking Ensemble & Interpretation** `(In progress)`
- **The Power of Synergy:** Our final model is not a single algorithm, but a powerful **Out-of-Fold (OOF) Stacking Ensemble**. This architecture combines the strengths of multiple top-tier models to achieve superior performance.
  - **Level 0 Models:** `LightGBM`, `XGBoost`, and `CatBoost` run in parallel, each learning different facets of the data.
  - **Level 1 Meta-Model:** A `LogisticRegression` model intelligently learns to weigh the predictions from the base models to produce a highly accurate and robust final prediction.
- **Full Interpretability:** We believe a powerful model must also be transparent. Our solution is fully interpretable:
  - **Global Importance:** We analyze the feature importances across all base models to identify the key business drivers of risk.
  - **Local Explanations (SHAP):** Using SHAP on our meta-model, we can explain **every single prediction** by showing how much each base model contributed to the final decision.
- **Notebook:** [`notebooks/3_Model_AON.ipynb`](notebooks/3_Model_AON.ipynb)

---

## 🛠️ Technology Stack

- **Core Libraries:** `Python`, `Pandas`, `NumPy`, `Scikit-learn`
- **Advanced Modeling:** `XGBoost`, `LightGBM`, `CatBoost`
- **Interpretability:** `SHAP`
- **Collaboration & Reproducibility:** `Google Colab`, `Git & GitHub`
- **AI Development Assistant:** `Gemini 2.5 Pro`

---

## 🤖 AI-Assisted Development

To accelerate our development process, enhance code quality, and explore advanced methodologies, we utilized the **Gemini 2.5 Pro** large language model as a collaborative tool. The AI's role included:

- **Code Generation & Refactoring:** Assisting in writing boilerplate code for data loading, cleaning pipelines, and model training loops.
- **Debugging:** Helping to identify and resolve errors in complex code blocks.
- **Strategic Brainstorming:** Providing insights and alternative approaches for feature engineering and model architecture, such as implementing the OOF stacking ensemble.

**Accountability:** All final architectural decisions, business logic, and code implementations were reviewed, validated, and ultimately directed by the human members of Team AON. We used AI as a powerful pair-programmer, not as a replacement for our own expertise.

---

## 🤝 Team AON

We are a dedicated team of data scientists who thrive on solving complex, real-world challenges. This project showcases our commitment to rigorous methodology, advanced techniques, and delivering results that are not only accurate but also understandable and actionable.

**All or Nothing.**