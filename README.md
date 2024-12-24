# Approach
## 2. Optimizing the Parameters using Optuna
Our objective is to optimize the hyper parameters. We will be using a framework called Optuna, which is used for Hyper parameters Tuning.
Optuna is an open source hyperparameter optimization framework to automate hyperparameter search. Its library Optuna-Integration will be used to execute the process
The way we prepare the data will be the same as before. Since LGBM performance is superior comparing to the other 2 models, for LGBM we focus on maximizing its QWK score based on the given dataset. For CatBoost, we try to minimize the RMSE and for XGBoost, we try to maximize the accuracy.

![image](https://github.com/user-attachments/assets/a9ed02be-8395-4b60-8dc7-8b8c6f8f5898)

![image](https://github.com/user-attachments/assets/0d393229-0f5d-45d4-bbaa-4e2e5ebdca50)
![image](https://github.com/user-attachments/assets/29e33c5c-d480-458d-9459-136236d5635c)

**LGBM optimized by QWK score**

![image](https://github.com/user-attachments/assets/be2635b3-6b74-4ca5-879b-34bf96786066)

**CatBoost optimized by RMSE**

![image](https://github.com/user-attachments/assets/42260a46-fe00-4955-ab0c-6a21681877aa)
![image](https://github.com/user-attachments/assets/03314952-c01b-4103-a92f-311677cbff1a)

**XGBoost optimized by accuracy**

After optimizing and get the best parameters, we will test out the parameters to see how well the LGBM model perform this time. I do the same with CatBoost and XGBoost.
![image](https://github.com/user-attachments/assets/edac737e-0122-4ab5-a8f4-bca20c0e090d)

**LGBM Optimized**

![image](https://github.com/user-attachments/assets/23011deb-334e-43b8-bda2-604313915ee4)

**CatBoost Optimized**

![image](https://github.com/user-attachments/assets/54cb2115-a1d0-4bf2-8c33-175a1abade47)

**XGBoost Optimized**
