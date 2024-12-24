# Approach
## 6. Encode the Time series data
In this approach, we will be dealing with the time series data instead. This time we will encode this data to check for the model performance on the encoded time series data. The autoencoder class is a custom pytorch model used for dimensionality reduction and construction. And the performautoencoder will encode the time series data.
Doing this will extract latent features from complex, high-dimensional data such as actigraphy or accelerometer readings. Also, it can provide compressed yet meaningful inputs for predictive models targeting the Severity Impairment Index (SII) or related metrics.

![image](https://github.com/user-attachments/assets/b765b797-3995-49f5-904a-bc902b51001e)

**Pytorch AutoEncoder class**

![image](https://github.com/user-attachments/assets/8e382872-8769-42cb-8d26-9046d5cffe17)
![image](https://github.com/user-attachments/assets/cf8c5b7a-2156-4fc9-8e1e-d6bac74dc1bb)

**Perform Encoding for Train and Test**

After encoding the data, we will impute the missing data of numerical columns using KNN with neighbor = 5, and then train the model using the imputed data.

![image](https://github.com/user-attachments/assets/032dfce0-cbb6-438d-a29e-c6e9d40c8a96)

**Impute the missing data**

The rest is unchanged.
