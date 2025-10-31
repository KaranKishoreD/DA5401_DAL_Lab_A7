# DA5400 – Assignment 7  
**Name:** Karan Kishore  
**Roll Number:** DA25D400

## 📘 Overview
This assignment focused on comparing multiple classification models' performance on a multiclass dataset  (UCI LANDSAT) using **Weighted F1**, **Macro ROC–AUC**, and **Macro PRC–AP** metrics.

Models evaluated include:
- K-Nearest Neighbors (KNN)  
- Decision Tree  
- Logistic Regression  
- Gaussian Naive Bayes  
- Support Vector Machine (SVM)  
- Random Forest  
- XGBoost  
- Dummy Classifiers (Prior, Stratified)  
- Inverse Random Forest (flipped predictions – weak model)

All models were trained and tested using **scaled data** for fair comparison.



## Evaluation Metrics
| Metric | Description |
|---------|-------------|
| **Weighted F1** | Balances precision and recall, weighted by class support |
| **Macro ROC–AUC** | Measures separability averaged over all classes |
| **Macro PRC–AP** | Evaluates precision–recall trade-off for each class |


## Key Findings
1. [BROWNIE TASK]**XGBoost** achieved the **best overall performance**, with the highest ROC–AUC and PRC–AP scores followed by **Random Forest**.  
2. **SVM** and **Random Forest** performed consistently well across all metrics, close to XGBoost.  
3. **KNN** provided balanced results but slightly lagged behind ensemble models.  
4. **Dummy (Stratified)** and **Inverse Random Forest** acted as weak baseline models for contrast.  
5. Minor variations due to random state were observed, but rankings remained stable.


## Best Model
**XGBoost Classifier**  
- **Weighted F1:** ~0.918  
- **Macro ROC–AUC:** ~0.990  
- **Macro PRC–AP:** ~0.940  

XGBoost was selected as the **final best model** due to its consistent superiority across all macro-level metrics.

## Brownie Points
- Implemented **RandomForest** and **XGBoost** for comparison.  
- Designed an **Inverse Random Forest** (flipped predictions) as a low-AUC baseline < 0.5 (around 0.01).  
- Added **Dummy (Stratified)** baseline has AUC < 0.5 (~0.49)  
- Visualized results using a **Radar Plot** for quick comparison between the models for various models.

---

## Summary
The task successfully explored multiple classification models, assessed their comparative performance, and identified **XGBoost** as the optimal choice based on macro-level evaluation metrics.
