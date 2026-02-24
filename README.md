# COVID19_CT_SCAN
In this project, we aim to develop a deep learning model that classifies whether a patient has COVID-19 based on CT scan images of their lungs

# COVID-19 CT Scan Classification Project

## 📂 Dataset Description
In the **`Data`** folder, you will find the **transformed database**:
- **72 COVID-19 images**
- **72 Non-COVID-19 images**

These images were collected from the **Pulmonology** and **Radiology** departments of **Hédi Chaker** and **Habib Bourguiba** hospitals in **Sfax**.

---

## 🧪 Data Preprocessing
The script **`Covid19_CT_SCAN_PreProcessing`** contains the steps applied to the **initial CT_SCAN images**.

### **Transformation Workflow**
1. **Initial dataset**:  
   - On average, **512 CT_SCAN images per patient**  
   - Total: **136 × 512 images**

2. **Manual selection**:  
   - Radiologists manually selected **260 relevant CT_SCAN images per patient** based on clinical importance.

3. **Image fusion using Discrete Wavelet Transform (DWT)**:  
   - The 260 selected images for each patient were **fused** using **DWT** for **dimensionality reduction**.  
   - Result: **68 images for COVID-19 patients** and **68 images for non-COVID-19 patients**.

4. **LBP Histograms transformation**:  
   - The 136 resulting fused images were transformed into **Local Binary Pattern (LBP) histograms**.

---

## 🤖 Modeling and Classification

### **1. CNN Modeling**
- Script: **`Covid19_CNN_best_results`**  
- Uses **TensorFlow + Keras**  
- **Goal**: Achieve the **best results** using **fused images without LBP histograms**.

---

### **2. Traditional Machine Learning Models**
- Script: **`Covid19_classification_results`**
- Algorithms implemented:
  - Random Forest
  - Neural Network (MLP)
  - Extra Trees
  - Gradient Boosting
  - XGBoost
- **Output**: Best performance for each algorithm based on the optimal configuration.

---

## 🗂 Project Structure

