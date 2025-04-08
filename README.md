# Predicting 10-Year Risk of Coronary Heart Disease (CHD)  

## Project Overview  
This project aims to analyze and predict the 10-year risk of coronary heart disease (CHD) using patient data from the Framingham Heart Study. The dataset contains over 4,240 records with 15 attributes, allowing for exploration, feature engineering, and the development of classification models.  

## Dataset Description  
- **Source:** Framingham Heart Study  
- **Records:** Over 4,240  
- **Attributes:** 15 features including demographics, health metrics, and lifestyle information relevant to cardiovascular health.  

## Objective  
The objective is to classify whether a patient is at risk of developing CHD within the next decade.  

## Exploratory Data Analysis (EDA)  

### 1. Distribution of Age Feature  
- **Analysis:** The age feature's distribution was analyzed using histograms and boxplots. This helped identify potential outliers in the age dataset.  
- **Visualizations:** [Include generated plots here]  

### 2. Correlation Analysis  
- **Top Correlated Features:**  
    - **sysBP**: Correlation value: [insert value]  
    - **totChol**: Correlation value: [insert value]  
    - **BMI**: Correlation value: [insert value]  
- **Interpretation:** A strong correlation suggests a significant impact of these features on predicting CHD risk.  

### 3. Categorical Feature Imbalance  
- **Imbalanced Features Identified:**   
    - **currentSmoker**  
    - **diabetes**  
- **Impact of Imbalance:** Class imbalance can lead to biased model predictions and decreased sensitivity towards minority classes.  
- **Suggested Technique:** Utilize **SMOTE** (Synthetic Minority Over-sampling Technique) to balance classes.  

### 4. Visualization of Numerical Features  
- **Analyzed Relationship:** [Specify which two numerical features were analyzed]  
- **Interpretation of Plots:** [Insert your interpretation here]  

## Feature Engineering  

### 1. Encoding Categorical Variables  
- **Encoding Applied:**  
    - **Nominal Features**: One-Hot Encoding for `sex`, `currentSmoker`, `BPMeds`, `prevalentStroke`, `prevalentHyp`, and `diabetes`.  
  
### 2. Feature Scaling  
- **Scaling Type:** StandardScaler applied to numerical features like `age`, `cigsPerDay`, `totChol`, `sysBP`, `diaBP`, `BMI`, `heartRate`, and `glucose`.  
- **Justification:** Scaling is crucial for models sensitive to feature scales, particularly those using distance metrics.  

### 3. New Feature Creation  
- **Feature Created:** **Pulse Pressure** = `sysBP - diaBP`  
- **Relevance:** Provides insights into arterial health and might correlate with CHD risk.  

### 4. Dimensionality Reduction  
- **Technique Used:** PCA (Principal Component Analysis)  
- **Benefits:** Reduces feature space while preserving variability, potentially improving model performance and reducing overfitting.  

## Prediction and Model Comparison  

### 1. Classification Models Built   
- **Models Used:**  
    - Logistic Regression  
    - Decision Tree Classifier  
- **Hyperparameters:** [Specify the hyperparameters used for each model]  

### 2. Model Evaluation  
- **Accuracy Results:**  
    - **Logistic Regression**: Train Accuracy: [insert], Test Accuracy: [insert]  
    - **Decision Tree**: Train Accuracy: [insert], Test Accuracy: [insert]  
- **Best Performing Model:** [Identify which model performed better on the test set along with reasons]  

### 3. Consistency of Train-Test Accuracies  
- **Observations:** Discuss any inconsistencies and whether models are overfitting or underfitting.   
- **Potential Solutions:**  
    - **Logistic Regression**: [Suggest a solution]  
    - **Decision Tree**: [Suggest a solution]  

### 4. Model Recommendation  
- **Recommended for Deployment:** [Choose between models]  
- **Reasons:** Consider interpretability, performance, and computational efficiency in your recommendation.  

## Conclusion  
This project highlights the process from data exploration to model implementation for predicting CHD risk. Insights gained from this analysis may assist in early diagnosis and treatment strategies in clinical settings.  

## Getting Started  
1. Clone the repository.  
2. Install required packages by running `pip install -r requirements.txt`.  
3. Run the Jupyter notebooks to reproduce the analysis and results.  

## Acknowledgments  
- The dataset from the Framingham Heart Study.  
- References to literature and methodologies used in the project.  
