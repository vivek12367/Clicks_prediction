# Property Interaction Prediction

## Overview
This project aims to develop a predictive model to estimate the number of interactions a property will receive within **3 days** and **7 days** of activation. The analysis is based on property details, user interactions, and additional features like photo count.

## Dataset
The project utilizes three datasets:
1. **Property Dataset (`property_data_set.csv`)**
   - Contains details about properties, such as type, furnishing status, location, rent, etc.
2. **Interaction Dataset (`property_interactions.csv`)**
   - Records user interactions with properties over time.
3. **Photo Count Dataset (`property_photos.tsv`)**
   - Provides the number of photos associated with each property.

## Objective
- **Predict the number of interactions** a property will receive within **3 days** and **7 days** of activation.
- Utilize **machine learning models** to estimate the engagement level of properties.

## Steps in Analysis
### 1. Data Preprocessing
- Load datasets and merge them based on `property_id`.
- Convert date columns (`activation_date`, `request_date`) into datetime format.
- Handle missing values in the datasets.

### 2. Feature Engineering
- Compute the **interaction count** within **3-day and 7-day windows** from activation.
- Extract numerical and categorical features from property details.
- Create additional variables such as:
  - **Property size, location, rent, and furnishing status**.
  - **Number of photos available**.
  
### 3. Exploratory Data Analysis (EDA)
- Visualize the distribution of interactions over time.
- Analyze the impact of property characteristics on engagement.
- Correlation analysis between different features and interaction count.

### 4. Model Development
- Train **machine learning models** such as:
  - **Linear Regression**
  - **Random Forest**
  - **Gradient Boosting Machines (GBM)**
- Evaluate model performance using **R-squared, MAE, and RMSE**.

## Results & Insights
- Properties with more photos tend to have higher engagement.
- Furnished properties receive more interactions compared to unfurnished ones.
- Location and rental price significantly impact the number of views.

## Future Enhancements
- Incorporate **more advanced ML models** like **Neural Networks**.
- Experiment with **different time windows** for interaction prediction.
- Use **external data sources** (e.g., market trends) to improve predictions.

## How to Run
1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
2. Run the Jupyter Notebook `clicks_prediction.ipynb`.
3. Review the predictions and model evaluation metrics.

## Author
Developed as part of a property analytics project to enhance market insights using data-driven methods.

