# Approach
## 3. Voting
The Voting Regressor is an ensemble learning technique that combines the predictions of multiple regression models to improve overall performance. 
By averaging the outputs of the individual models, it reduces variance and leverages the strengths of each model, making it robust and effective for tasks where a single model might underperform.
We will use 3 models: CatBoost, XGBoost and LGBM, put them all in a voting model. The optimized parameters will still be used in this approach.


![image](https://github.com/user-attachments/assets/10db4d30-48f1-4284-8418-3d140fd0de82)
Voting of LGBM, XGBoost and CatBoost
