# Comparative Analysis of Imputation Techniques in Australian Rainfall Data

## Project Overview
This project investigates various **imputation techniques** for handling **missing data** in the **Australian Rainfall Dataset**. Missing data is a common challenge in real-world datasets, and accurately imputing values is critical to maintaining the integrity of data analysis and predictive modeling. The project compares the performance of different imputation techniques and evaluates their impact on the accuracy of **rain prediction models**.

## Key Objectives
- Compare the performance of **multiple imputation techniques** on the Australian Rainfall Dataset.
- Assess the impact of these techniques on the accuracy of **machine learning models**.
- Analyze the **correlation** between imputed values and actual outcomes to evaluate imputation effectiveness.
- Explore **overfitting risks** and model stability through cross-validation and learning curve analysis.

## Dataset
The dataset used is the **Weather in Australia** dataset, which includes weather-related data such as rainfall, temperature, and other environmental features. The dataset contains missing values that were the focus of this project.

- **Dataset Source**: [Weather in Australia Dataset](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package)
  
## Methods and Techniques
### Imputation Techniques:
- **MICE (Multivariate Imputation by Chained Equations)**: Performed the best in this analysis.
- **Mean Imputation**
- **KNN Imputation**
  
### Machine Learning Models:
- **Random Forest Classifier**
- **Decision Tree**
  
### Key Analysis:
- **Cross-Validation**: To ensure model generalizability and avoid overfitting.
- **Learning Curves**: Analyzed the effect of the training data size on model performance.
- **Overfitting Analysis**: Examined the balance between model complexity and accuracy on unseen data.

## Tools & Technologies
- **Python** for scripting and analysis.
- **Pandas**, **NumPy** for data manipulation.
- **Scikit-learn** for machine learning models.
- **MICE (through `statsmodels`)** for imputation.
- **Matplotlib**, **Seaborn** for data visualization.

## Key Findings
- The **MICE imputation technique**, combined with the **Random Forest (Scaled)** model, demonstrated the highest prediction accuracy for Australian rainfall.
- **MICE** achieved:
  - **Accuracy**: 88.34%
  - **Precision**: 82.04%
  - **ROC/AUC**: 78.54%
- **Cross-validation** confirmed model stability, and **overfitting risks** were minimized by balancing model complexity (maximum depth between 6-8 for Random Forest).
- **Feature selection** did not significantly improve model performance, suggesting all features contributed effectively to the model's predictive ability.

## Recommendations
- **MICE** is recommended as the most effective imputation technique for similar datasets with missing values.
- **Random Forest** offers high predictive power with reasonable computational overhead, especially when combined with **MICE**.
- Care should be taken to monitor model complexity and apply cross-validation to avoid **overfitting**.

## Conclusion
This project successfully demonstrated the efficacy of **MICE imputation** in handling missing data for **rainfall prediction** in Australia. The **Random Forest (Scaled)** model, when paired with **MICE**, provides robust performance in terms of accuracy, precision, and ROC/AUC. Although **feature selection** did not improve performance significantly, further research could investigate other advanced techniques or larger datasets for even better results.

## Future Enhancements
- Explore **additional imputation techniques** like deep learning-based imputation models.
- Expand the study to include **other weather datasets** from different regions.
- Implement **ensemble models** to further boost predictive accuracy.
