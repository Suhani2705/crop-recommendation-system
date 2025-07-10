# 🌾 Crop Recommendation System

A machine learning project designed to recommend the **most suitable crop** for cultivation based on soil and climatic conditions. This system leverages **Random Forest** and **Support Vector Machine (SVM)** models and integrates **model explainability** using **SHAP** and **LIME** to promote transparency and trust in AI predictions.

---

## 📊 Features

- **Dataset**: [Crop Recommendation Dataset](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset)
- **Algorithms Used**:
  - Random Forest Classifier (RF)
  - Support Vector Machine (SVM) with RBF kernel
- **Model Evaluation**:
  - Accuracy Score
  - Classification Report & Confusion Matrix
  - Cross-validation accuracy
- **Dimensionality Reduction & Visualization**:
  - PCA for crop clustering visualization
  - Correlation heatmap for feature insight
- **Explainability**:
  - **SHAP** (global + local explanations for RF)
  - **LIME** (local interpretation for SVM)
- **Confidence-based Crop Recommendation System**:
  - Uses predicted **probability scores** from both models
  - Recommends crop from the model with **higher prediction confidence**

---

## 🧪 Inputs Required

To make a prediction, the following environmental and soil parameters are required:

- Nitrogen (N)
- Phosphorus (P)
- Potassium (K)
- Temperature (in °C)
- Humidity (in %)
- pH value of the soil
- Rainfall (in mm)

---

## 🧠 How Crop Prediction Works

### 🔍 Step-by-step Prediction Logic

1. **Preprocessing**: 
   - Inputs are scaled if passed into SVM.
2. **Model Inference**:
   - Both **SVM** and **Random Forest** make a prediction and return **class probabilities** using `.predict_proba()`.
3. **Confidence Scoring**:
   - The **maximum class probability** from each model is treated as a confidence score.
   - The prediction with the **higher confidence** is selected.
4. **Final Output**:
   - Displays both model predictions, their confidence scores, and the final recommended crop with the source model used.

---

