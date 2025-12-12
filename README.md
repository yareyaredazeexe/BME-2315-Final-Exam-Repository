# Module 1 — Sex-Based Differences in the Aβ42/Aβ40 Ratio in Alzheimer’s Disease

## 📘 Overview
This project investigates whether males and females with Alzheimer’s disease show differences in the **Aβ42/Aβ40 ratio**, a widely used biomarker of amyloid pathology. The analysis uses donor-level biochemical and neuropathological data from the **SEA-AD** cohort.

We merged metadata with Luminex assay measurements, calculated biomarker ratios for each donor, and restricted our analysis to individuals with **high or intermediate Alzheimer’s disease neuropathological change (ADNC)**.

---

## 🧠 Research Question
**Do males and females with Alzheimer’s disease differ in their Aβ42/Aβ40 ratio?**

---

## 🧪 Methods
The following steps were performed in Python (Jupyter Notebook):

- Import and clean metadata and Luminex assay data  
- Merge datasets using donor IDs  
- Compute the **Aβ42/Aβ40 ratio** for each subject  
- Filter donors based on neuropathology severity  
- Compare sexes using:
  - **Two-sample Student’s t-test**
  - **Linear regression (OLS) controlling for age at death**

Libraries used:
- `pandas`
- `numpy`
- `matplotlib`
- `scipy.stats`

---

## 📊 Results
- The **two-sample t-test** indicated *no statistically significant difference* in Aβ42/Aβ40 ratios between males and females.
- A linear regression model including **sex** and **age at death** also found **no independent effect of sex** on the biomarker ratio.
- These results agree with previous findings suggesting sex alone is not a strong predictor of amyloid burden measured by this ratio.

---

## 📁 Repository Structure
This folder contains:

- **Module1_Alzheimers.ipynb** — Full Jupyter Notebook with code, figures, and analysis  
- **Module1_Alzheimers.pdf** — PDF export of the notebook  
- **Data folder** — Contains:
  - `UpdatedMetaData.csv`
  - `UpdatedLuminex.csv`
  - Any other required files for reproducibility

---

## 🧰 Skills Demonstrated
- Data cleaning and merging  
- Visualization and exploratory analysis  
- Statistical testing and interpretation  
- Regression modeling  
- Translating computational results into biological meaning  

---

## 📚 Data Source
SEA-AD postmortem dataset (publicly available, de-identified donor metadata and Luminex protein quantification).

---

## 👥 Authors
Course: **BME 2315 — Computational Biomedical Engineering**  
Module 1 Project Team
