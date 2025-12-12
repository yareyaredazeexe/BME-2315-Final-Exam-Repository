# **Module 4 — Organ Fibrosis Classification Using Machine Learning**

### **Team Members:**
Hazel Miranda and Spencer Boon

---

## **📌 Project Title**

**Classifying Organ Fibrosis Using K-Nearest Neighbors and Support Vector Machines**

---

## **📘 Project Overview**

This module explores whether **machine learning models** can accurately classify tissue images as **healthy** or **fibrotic** based on quantitative pixel-intensity features. We applied two supervised learning algorithms:

* **K-Nearest Neighbors (KNN)**
* **Support Vector Machines (SVM)**

By preprocessing image data, extracting numerical features, and training classifiers, we evaluated how well each algorithm distinguishes normal tissue from disease states.

The workflow included:

* Loading and flattening image data  
* Splitting samples into training and testing sets  
* Training KNN and SVM models  
* Evaluating accuracy, confusion matrices, and misclassifications  

This module demonstrates how machine learning can support **automated pathology tools** and strengthen fibrosis-detection pipelines.

---

## **📂 Files in This Folder**

### **1. `KAMEN4_MIRANDA_BOON_MODULE_4.ipynb`**

This notebook contains:

* Background information on fibrosis  
* Dataset explanation  
* Image preprocessing  
* KNN and SVM classifier implementation  
* Confusion matrices and accuracy calculations  
* Misclassified image outputs  
* Written analysis, validation, conclusions, and ethical reflections  

### **2. `KAMEN4_MIRANDA_BOON_MODULE_4.html`**

An HTML export of the complete notebook for easy viewing.

---

## **🧬 Dataset Summary**

The dataset contains grayscale biomedical images labeled as **healthy** or **fibrotic**. Each image is represented numerically through:

* pixel intensity values  
* flattened image vectors  
* binary class labels (0 = healthy, 1 = fibrotic)

Important dataset properties:

* Images vary in texture and brightness  
* Disease vs healthy classes are unevenly distributed  
* Flattening simplifies images but removes spatial context  

---

## **🖥️ Methods Summary**

### **⭐ Preprocessing Steps**

1. Load each image with NumPy  
2. Convert to grayscale  
3. Flatten the image into a feature vector  
4. Combine all image vectors into a single dataset  
5. Label each sample as healthy or fibrotic  

### **⭐ Machine Learning Models**

#### **K-Nearest Neighbors (KNN)**  
* Classifies images by comparing them to their closest neighbors  
* Simple and intuitive  
* Struggles with complex, non-linear boundaries  

#### **Support Vector Machine (SVM)**  
* Finds the optimal hyperplane separating classes  
* Handles non-linearity well with kernel functions  
* Demonstrated superior performance in our project  

### **⭐ Model Evaluation**

We compared models using:

* Accuracy  
* Confusion matrices  
* Visual inspection of misclassified images  

---

## **📈 Key Findings**

* **SVM outperformed KNN**, showing better separation between healthy and fibrotic tissue.  
* KNN produced more misclassifications, especially where images had overlapping pixel distributions.  
* SVM captured subtle textural differences that KNN could not.  
* Both models confirmed that pixel-based image features can be used for fibrosis detection.  

---

## **🔍 Validation**

We validated the models through:

* Train–test splitting  
* Reviewing misclassification patterns  
* Checking for overfitting  
* Comparing model metrics  

SVM displayed:

* Higher sensitivity to fibrotic tissue  
* Lower false-positive/false-negative rates  
* More stable predictions across runs  

These results support SVM as the more reliable classifier for this dataset.

---

## **📌 Conclusions**

* Machine learning can classify fibrosis images with reasonable accuracy.  
* SVM is better suited to this dataset than KNN due to its ability to handle complex decision boundaries.  
* Pixel-intensity features provide enough information for initial tissue classification.  
* This approach demonstrates the potential for automated diagnostic tools in pathology.  

---

## **⚖️ Ethical Implications**

* Automated classification systems must be carefully validated before any clinical deployment.  
* Misclassification could lead to incorrect diagnoses, so human oversight is essential.  
* The dataset contains **no human subject data**, which minimizes privacy concerns.  
* Computational approaches like this may reduce the need for animal studies by improving experimental prioritization.

---

## **⚠️ Limitations**

* Relatively small dataset  
* Flattening images loses spatial structure  
* Class imbalance may bias accuracy  
* No cross-validation included  
* Only two ML models tested  

---

## **🚀 Future Work**

* Implement **Convolutional Neural Networks (CNNs)** for better image-based learning  
* Use **k-fold cross-validation** to reduce bias  
* Engineer richer features:  
  * texture descriptors  
  * GLCM (Gray-Level Co-occurrence Matrix)  
  * local edge/shape patterns  
* Test additional models such as Random Forest or Gradient Boosting  
* Incorporate image segmentation to isolate fibrotic regions before classification  

---
