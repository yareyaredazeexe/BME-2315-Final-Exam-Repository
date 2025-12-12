# Module 2 — Quantifying Fibrosis in Lung Tissue Images at Different Depths

## 👥 Team Members
Hazel Miranda  
Ryan Sloan

---

## 📘 Project Title
**The Extent of Fibrosis in the Lung at Different Depths**

---

## 🎯 Project Goal
This project analyzes microscopy images of fibrotic mouse lung tissue to determine how the **percentage of fibrotic area (white pixels)** changes at different biopsy depths. Using image processing and interpolation, we quantify fibrosis severity and estimate fibrosis at unmeasured tissue depths.

---

## 🫁 Disease Background: Pulmonary Fibrosis
Pulmonary fibrosis is a chronic disease characterized by progressive scarring of lung tissue. Key topics covered in the notebook include:

- **Prevalence:** ~14–64 cases per 100,000 in the U.S., increasing with improved diagnostics.  
- **Incidence:** ~7–17 new cases per 100,000 annually.  
- **Risk factors:** Smoking, occupational exposures (mining, farming, construction), cancer treatments, and genetic predispositions.  
- **Symptoms:** Shortness of breath, dry cough, weight loss, fatigue, joint pain, and digital clubbing.  
- **Pathophysiology:** Excessive extracellular matrix deposition caused by epithelial injury, fibroblast activation, immune dysregulation, and TGF-β signaling.  
- **Standard treatments:** Antifibrotic drugs (pirfenidone, nintedanib), oxygen therapy, pulmonary rehabilitation.

This background is used to contextualize the biological meaning of fibrosis severity seen in the images.

---

## 📁 Dataset Description
The dataset consists of **76 microscopy images** of mouse lungs treated with **bleomycin** to induce pulmonary fibrosis. For Module 2, **6 images** were selected for detailed analysis.

Each image includes:

- A specific **tissue depth** (in microns)  
- A fibrosis stain where **white pixels represent fibrotic lesions**

The images were collected and provided by **Dr. Shayn Peirce-Cottler’s laboratory**.

---

## 🔬 Data Analysis Overview

### **Image Processing**
For each selected image:

1. The image is converted to grayscale.
2. Thresholding is applied to classify pixels as **white** (fibrotic) or **black** (non-fibrotic).
3. The number of white and black pixels is counted.
4. The **percentage of white pixels** is computed as a fibrosis indicator.

These results are written to:

Percent_White_Pixels.csv

yaml
Copy code

---

### **Interpolation Analysis**
Using the measured white-pixel percentages and their corresponding depths:

- **Linear interpolation**  
- **Quadratic interpolation**

were performed to estimate fibrosis at any depth along the tissue.

A sample interpolation at **3900 microns** was generated and compared to the actual measured image at that depth.

---

## 📊 Results Summary

- Both linear and quadratic models show an **increasing trend** of fibrosis with tissue depth.  
- At 3900 microns, the real image measured **2.00% white pixels**.  
- Interpolations predicted:
  - Linear: **2.011%**
  - Quadratic: **1.872%**

Both estimates were close to the actual measurement, validating the interpolation approach.

Quadratic interpolation was chosen as the better fit because it accounts for **biological variability** across the lung.

---

## ✔️ Verification and Validation
- Independent image analysis on the true 3900-micron image confirmed the accuracy of both interpolation methods.
- Interpolated values matched biological expectations: **greater depth = greater fibrosis**.
- The consistency between model predictions and actual data supports the reliability of the processing pipeline.

---

## 🧭 Conclusions and Ethical Implications

### **Conclusions**
- Fibrosis severity increases with lung depth, consistent with progressive scarring in deeper tissue.
- Image-based quantification can support lung-disease research by identifying structural trends.

### **Ethical Considerations**
- Fibrosis data came from **animal models**, requiring humane treatment and adherence to the **3Rs**:
  - **Replacement**
  - **Reduction**
  - **Refinement**
- Image analysis reduces the number of animals needed for fibrosis assessment.
- Findings should not be overgeneralized to humans without proper translational research.

---

## ⚠️ Limitations
1. **Small sample size** — Only 6 of 76 images were analyzed.  
2. **Binary thresholding oversimplifies** tissue complexity.  
3. **Interpolation assumes smooth trends**, which may not reflect real biological irregularities.  
4. **Mouse model limitations** — Results may not directly translate to human pulmonary fibrosis.

---

## 🚀 Future Work
- Analyze **all 76 images** for stronger statistics.  
- Use **machine learning segmentation** instead of binary thresholding.  
- Create **3D reconstructions** of fibrosis across depth slices.  
- Compare fibrosis patterns under different treatments or conditions.  
- Apply **regression or hypothesis testing** for stronger statistical conclusions.

---

## 📁 Files Included in This Folder
