# Data Preprocessing

This dataset supports the creation of predictive models to identify a participant's **Severity Impairment Index (SII)**—a standardized measure of problematic internet use (PIU).  

## SII Categories
- **0**: None  
- **1**: Mild  
- **2**: Moderate  
- **3**: Severe  

## Dataset Description
- **Parquet (Actigraphy) Files**: Continuous wrist accelerometer readings spanning many days per participant, with key values such as `emo`, `wear_flag`, etc.  
- **CSV Files**: Includes training and testing data, providing labels and features.

![image](https://github.com/user-attachments/assets/a8082111-7b92-4ef5-995f-0459870f411a)
We start with function used for loading time series data (parquet files)

![image](https://github.com/user-attachments/assets/6284ef85-bc16-4d08-9861-c02365a778a3)
Train data and test data is then loaded and merge with its corresponding data by participant’s id. ID column is then removed for better performance

![image](https://github.com/user-attachments/assets/8793c670-4bc3-4afa-861b-44342b5afd5d)
Features columns are merged with the columns from the time series data. Drop all row with label having NaN value

![image](https://github.com/user-attachments/assets/24d8880e-4fae-4ce9-b688-0e983b39ddaa)
We then update the data by filling the categorical columns NaN values for “Missing” to encode

![image](https://github.com/user-attachments/assets/0cfc55e8-5341-4160-80f3-1f11b8e1cf43)
Finally, we use Integer Encoding to encode the values in all Categorical columns

# Methods

## Evaluation Function
The competition required a specific way to evaluate the result, which is using Quadratic Weighted Kappa.
![image](https://github.com/user-attachments/assets/2032fae4-ed53-488c-9b91-0dd10105cfb5)

## Train model Function
Model trained using RepeatedKFold and evaluate with QWK score
![image](https://github.com/user-attachments/assets/8387b852-9b75-4825-a2ce-f67fc1a37a72)

![image](https://github.com/user-attachments/assets/053c727c-144a-49b5-bde0-08ad5a3ee36f)

![image](https://github.com/user-attachments/assets/3968eaf6-0e19-48c2-bf68-3e5684174b8e)

# Approach
## 1. Using Boosting Model
We will use 3 models in the competition, including:
- **LightGBM**: A gradient boosting framework that is highly efficient and optimized for speed. It uses a histogram-based algorithm to reduce memory usage and computation time, making it well-suited for large datasets and high-dimensional data
- **XGBoost**: A powerful and flexible gradient boosting framework designed for performance and scalability. It supports regularization to prevent overfitting and is widely used in competitions for its robust handling of structured/tabular data.
- **CatBoost**: A gradient boosting framework tailored for categorical data. It automatically handles categorical features without requiring extensive preprocessing, making it user-friendly and effective for datasets with mixed data types.

Each models are first run with default parameters to see the performance. The files you see in this branch is the first 3 submissions, 1 for each Model, all with default parameters.
