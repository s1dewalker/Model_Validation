<img src="sc/MODEL VALIDATION.png" alt="Description" width="1000">
<br/>

## Example 1: Model validation of Assumptions of OLS regression in Fama French 3-Factor Model

### 1. Checking Multicollinearity of features or independent variables w/ Correlation matrix
### 2. Checking Llinearity w/ Scatter plots
### 3. Checking Idependence of of residuals w/ Autocorrelation Function (ACF) and D-W test
### 4. Checking Normality of residuals w/ histogram
### 5. Checking Homoscedasticity of Residuals w/ scatter plot of residuals and fitted values
<br/>

### [Check out Model Validation for OLS Regression in Factor analysis in Python](https://github.com/s1dewalker/Model_Validation/blob/main/Multi_Factor_Analysis3.ipynb)

<br/>

## Example 2: Model validation and tuning in Random Forest Regression, on a continuos data

### 1. Get the data
### 2. Define the target (y) and features (X)
### 3. Split the data into training and testing set (validation if required)
### 4. Initiate a model, set parameters, and Fit the training set | `X_train, y_train`
### 5. Predict on `X_test`
### 6. Accuracy or Error metrics on `y_test` | Ex: R squared
### 7. Bias-Variance trade-off check | Balancing underfitting and overfitting
### 8. Iterate to tune the model (from step 4)
### 9. Cross Validation | if model not generalizing well
### 10. Selecting the best model w/ Hyperparameter tuning
<br/>

### [Check out Model Validation and Tuning for RFC in Python](https://github.com/s1dewalker/Model_Validation/blob/main/Model_Validation.ipynb) 

<br/><br/>

Few Details:

## Bias-Variance trade-off

<img src="sc/biasvariance.JPG" alt="Description" width="500">


**Bias = failing to find relationship b/w data and response** = ERROR due to OVERLY SIMPLISTIC models (underfitting) <br/>

**Variance = following training data too closely** = ERROR due to OVERLY COMPLEX models (overfitting) that are SENSITIVE TO FLUCTUATIONS (noise) in the training data <br/>
<br/>
<br/>

High Bias + Low Variance: Underfitting (simpler models) <br/>
Low Bias + High Variance: Overfitting (complex models) <br/>
<br/>
### **Training error high = Underfitting** 
### **Testing error >> Training error = Overfitting** <br/>
 <br/>


## Cross Validation 
<img src="sc/cvimg2.png" alt="Description" width="500">

###### by sharpsightlabs.com

### Splitting data into distinct subsets. Each subset used once as a test set while the remaining as training set. Results from all splits are averaged. <br/>
<br/>
Why use? <br/>

- Better Generalization: If our models are not generalizing well (Generalization refers to a model's ability to perform well on new, unseen data, not just the data it was trained on)
- Reliable Evaluation
- Efficient use of data (if we have limited data)
 <br/>
 
Types: <br/>
1. **cross_val_score**
<img src="sc/cvs.JPG" alt="Description" width="500">

 <br/>
 
2. **Leave-one-out-cross-validation (LOOCV)**

Use when data is limited, but computationally expensive <br/>
**Each data point is used as a test set** <br/>

`cv = X.shape[0]`

<br/>



