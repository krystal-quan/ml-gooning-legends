# Approach
## 7. Optimizing parameters by QWK score
Since the results is evaluated with QWK score, instead of optimizing the models by default means, we will be trying to maximize the QWK score received instead.
We will optimize the parameters by QWK score instead of RMSE for CatBoost and Accuracy for XGBoost. We will be using voting model for this approach.

![image](https://github.com/user-attachments/assets/b172e79c-13a4-4253-9a1d-144238ce769f)


CatBoost optimized by QWK score

![image](https://github.com/user-attachments/assets/af817f9a-2f82-4962-8d97-ccd7ff0c0121)
![image](https://github.com/user-attachments/assets/9bdde12a-7755-4e46-b301-cd0824a99324)

XGBoost optimized by QWK score

![image](https://github.com/user-attachments/assets/4b68e12f-f4fc-4f19-b8ec-1fbd8f8e1b8f)

Train the model with acquired parameters

