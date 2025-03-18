# CNN-Model-covid-19

## Project Description
This project compares two models for classifying lung images into COVID-19, Normal, and Viral Pneumonia categories:
- **Model 1: MobileNetV2**
- **Model 2: Custom CNN Model**

The main goal is to determine which model provides better prediction accuracy using Cohen's Kappa and ROC-AUC metrics.

## Model Comparison Results

### Cohen's Kappa (Prediction Consistency)
Cohen's Kappa measures the agreement between model predictions and true labels, adjusted for chance agreement.
- **MobileNetV2 (Model 1):** **0.7933** → Strong agreement
- **CNN Model (Model 2):** **0.7474** → Moderate to strong agreement

**Conclusion:** MobileNetV2 provides more reliable predictions.

### ROC-AUC Comparison (Classification Performance)
#### COVID-19 Detection:
- **MobileNetV2:** **AUC = 0.99** → Near-perfect classification
- **CNN Model:** **AUC = 0.96** → Very high accuracy, but slightly lower

#### Normal Case Detection:
- **MobileNetV2:** **AUC = 0.81** → Good classification performance
- **CNN Model:** **AUC = 0.79** → Slightly lower, but still strong

#### Viral Pneumonia Detection:
- **MobileNetV2:** **AUC = 0.87** → Strong classification performance
- **CNN Model:** **AUC = 0.86** → Almost identical performance

**Conclusion:** MobileNetV2 outperforms in COVID-19 and Normal detection, while both models show similar performance in Viral Pneumonia detection.

### Prediction Accuracy Comparison
#### MobileNetV2 (Model 1):
- COVID-19: **26/26** (100%)
- Normal: **13/20**, **7 misclassified as Viral Pneumonia**
- Viral Pneumonia: **18/20**

#### CNN Model (Model 2):
- COVID-19: **25/26**
- Normal: **12/20**, **8 misclassified**
- Viral Pneumonia: **18/20** (same as MobileNetV2)

## Final Conclusion
- **MobileNetV2 outperforms the CNN Model** in all key metrics.
- The biggest advantage of MobileNetV2 is its superior COVID-19 detection.
- Both models perform well in Viral Pneumonia classification, but MobileNetV2 is slightly better at distinguishing Normal cases.

## Possible Improvements
1. **Data Augmentation** to enhance generalization.
2. **Model Ensembling** by combining MobileNetV2 with other architectures.
3. **Hyperparameter Optimization** to improve the CNN model.
4. **Attention Mechanisms** (e.g., SE blocks) to enhance classification accuracy.
5. **Grad-CAM Visualization** to understand which image regions influence model decisions.







