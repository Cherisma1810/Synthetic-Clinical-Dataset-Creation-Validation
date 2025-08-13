# Synthetic Clinical Dataset Generator — Early-stage Ovarian Cancer
**Region-tuned: Armenian/Eastern European Populations**

## 📌 Project Overview
This project generates a **synthetic clinical dataset** tailored for early-stage ovarian cancer research. The model parameters are tuned to reflect **Armenian/Eastern European** epidemiological patterns, especially for **BRCA mutation prevalence**, **menopause onset**, **BMI ranges**, and **tumor marker distributions**.

The dataset is **artificially generated** using statistical distributions and domain-informed rules. It can be used for **machine learning experimentation, feature engineering, exploratory data analysis**, and **risk model prototyping** — without involving real patient data.

---

## 🎯 Key Features
- **Demographic & Clinical Variables**
  - Age distribution stratified by health status and BRCA+
  - Menopausal status via logistic probability model
  - Family history probabilities tuned to regional clustering
  - BMI distributions adjusted for regional averages
  - Tumor size, ultrasound risk, and CA-125 biomarker modeling
  - Symptom severity scores with BRCA+ adjustment

- **Epidemiology-driven Modeling**
  - Cancer prevalence: 35% (configurable)
  - BRCA+ higher among cancer cases (18%) than healthy controls (12%)
  - Earlier menopause onset (~48 years) compared to US averages
  - CA-125 levels modeled as **log-normal distributions** with tumor-size correlation
  - Ultrasound risk modeled using **beta distributions** + tumor-size boost

- **Outputs**
  - Synthetic CSV dataset (`synthetic_clinical_dataset.csv`)
  - Statistical summary (Markdown or PDF)
  - Visualization plots:
    - CA-125 distribution by diagnosis
    - Tumor size distribution by diagnosis
    - Ultrasound risk distribution by diagnosis
    - Correlation matrix heatmap
    - Tumor size vs CA-125 scatter plot

---

## 📂 Project Structure
```plaintext
project_root/
├── data/
│   └── synthetic_clinical_dataset.csv
├── plots/
│   ├── ca125_by_diagnosis.png
│   ├── tumor_size_by_diagnosis.png
│   ├── ultrasound_by_diagnosis.png
│   ├── correlation_matrix.png
│   └── tumor_vs_ca125.png
├── Synthetic_Clinical_Report.pdf (or .md)
└── synthetic_dataset_generator.ipynb
```

---

## ⚙️ Installation & Requirements
**Python version:** 3.8+  
**Required libraries:**
```bash
pip install numpy pandas matplotlib reportlab
```

---

## 🚀 Usage
1. **Clone or download** the project.
2. **Open** the Jupyter Notebook:
   ```bash
   jupyter notebook synthetic_dataset_generator.ipynb
   ```
3. **Run all cells** to:
   - Generate the dataset
   - Produce summary statistics
   - Save plots to `/plots`
   - Export dataset to `/data`

---

## 📊 Example Output Summary
*(Example values from a recent run)*
```
Records: 800
Cancer prevalence: 35.0%
BRCA+ overall prevalence: 14.7%
Healthy with CA-125 < 35 U/mL: 86.0%
Cancer with CA-125 > 200 U/mL: 80.5%
```

---

## ⚠️ Disclaimer
This dataset is **entirely synthetic** and generated from modeled distributions informed by literature and domain expertise.  
It contains **no real patient information** and must **not** be used for actual clinical decision-making.
