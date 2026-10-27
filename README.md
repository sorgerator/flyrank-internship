# Content Opportunity Scoring and Refresh Pipeline

**Author:** Tarik Sorguč (Machine Learning Intern, FlyRank AI)
**Awards:** 2nd Place at Prolog EXPO (September 2026)

## 📌 The Problem
Content decay is a persistent challenge in SEO and digital publishing. Traffic for high-performing articles naturally degrades over time, and identifying which pages to update is often a reactive, manual process. This project introduces a predictive Machine Learning pipeline that scores content opportunity and forecasts refresh decay risk, enabling content teams to prioritize updates proactively before significant traffic drops occur.

## 📈 The Result
During my Machine Learning internship at FlyRank AI, I developed an end-to-end analytics and prediction pipeline to solve this issue. 
* Engineered a highly efficient data processing workflow using **DuckDB** to handle search performance records.
* Trained and optimized **Random Forest** models to predict content decay risk and score refresh opportunities.
* Authored the comprehensive research paper *"Content Opportunity Scoring and Refresh pipeline"*.
* Presented this capstone project at the Prolog EXPO showcase (organized by Naučno društvo "Vladimir Prelog"), winning 2nd place.

## 🛠️ How to Reproduce
The pipeline is modularized into sequential scripts located in the `scripts/` directory. To reproduce the environment and run the pipeline:

1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. You can execute the entire pipeline at once by running the master script:
   ```bash
   python scripts/run_all.py
   ```

3. Alternatively, run the pipeline steps individually in this exact order:
   - `python scripts/01_prepare_features.py`
   - `python scripts/02_baseline_score.py`
   - `python scripts/03_train_model.py`
   - `python scripts/04_evaluate_and_export.py`
   - `python scripts/05_build_pdf_report.py`

## 🔒 Gated-Dataset Note
Please note that the raw analytics data (`data/raw/content_refresh_anonymized.csv`) used to train this model contains proprietary and anonymized FlyRank AI search performance records. Due to confidentiality and company policy, access to the raw dataset is strictly restricted. The repository provides the complete codebase, feature engineering logic, and model architecture for full transparency and demonstration of the methodology.
