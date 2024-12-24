# Approach
## 8. Pipeline Integration, Simple Imputer and Voting
We use three different submission strategies in this approach.  

### Submission Strategy 1: Median Imputation with Ensemble Model  
- **Imputation**: Missing data is handled using a simple imputer, specifically the **median**.  
- **Ensemble Model**:  
  - Composed of five different regressor models (e.g., 'lgb', 'xgb', etc.).  
  - Each regressor is implemented as a **Pipeline**, combining preprocessing steps (like imputation) with the regression model (e.g., `LGBMRegressor`, `XGBRegressor`, etc.).  
  - This ensures that preprocessing (e.g., imputing missing data) is handled independently within each estimator before applying the regression algorithm.  

### Submission Strategy 2: Pre-Built Models  
- In this implementation:  
  - Each estimator (e.g., 'lightgbm', 'xgboost', etc.) is assigned a **pre-built model** (`LightGBM_Model`, `XGB_Model`, `CatBoost_Model`, etc.).  
  - These models are already configured and assume that preprocessing (such as imputing missing values) has either been handled separately or is not required.  

### Combined Strategy  
- All models use the same method to handle missing data.  
- Models contribute collectively to the **final prediction**.  
- We combine:  
  1. The ensemble model described above.  
  2. Two **voting models** with the best results.
 

![image](https://github.com/user-attachments/assets/c16247fc-d24e-4643-a15c-b64c61f95e51)

**Define the model**

![image](https://github.com/user-attachments/assets/21cfeb14-6073-4724-ad1b-1df0abff7a23)
![image](https://github.com/user-attachments/assets/53d47127-e702-4941-a862-a6566fe3f16d)
![image](https://github.com/user-attachments/assets/96cc0619-2604-4c38-b324-d2530dd93241)

**Training**

![image](https://github.com/user-attachments/assets/35f27057-6258-4cc2-8164-7b29f373a75d)
Final Voter and Result


# Results
![image](https://github.com/user-attachments/assets/51a48f55-bf13-415e-b533-0d3ccd3b5297)
![image](https://github.com/user-attachments/assets/3ef2bc05-1aa4-4559-8b9d-3e4795155e40)


# Submission Proofs
![image](https://github.com/user-attachments/assets/c4931143-b46b-46f8-9032-4d8ab101c42e)
![image](https://github.com/user-attachments/assets/4b24aa04-d599-4690-b794-af9eb84877c2)
