# Approach
## 5. Feature Selection
Our next approach is stll related to preprocessing data, but this time instead of imputing the data, we will select the features which have most influence on the model. Feature selection is the process of identifying and selecting the most relevant features (variables) in a dataset for building a machine learning model. It helps reduce dimensionality, improve model performance, prevent overfitting, and enhance interpretability by removing redundant or irrelevant features while retaining the ones that contribute most to predictive accuracy.
We will calculate the correlation between the label and other features. In this case, we will choose the features with correlarion >0.1. After choosing the features, we will merge it with the time series data, creating a new dataframe with selected features and time series (the time series stay the same). And then we will train the model using the data we have just created.

![image](https://github.com/user-attachments/assets/5b9adf4d-4f35-4227-b4eb-c267b8db2f28)

Calculating the correlation

![image](https://github.com/user-attachments/assets/3e814cfc-0f6b-43c0-b9ea-dac339f1b2f0)

Choose only the selected features and merge

![image](https://github.com/user-attachments/assets/275f3987-5b35-4e30-b882-c18bd4af26dd)

Train the model with the selected features
