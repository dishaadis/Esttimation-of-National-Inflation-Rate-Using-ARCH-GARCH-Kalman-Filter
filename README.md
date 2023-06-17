# Estimation of National Inflation Rate Using ARCH-GARCH Kalman Filter

<p align="center">
Undergraduate Final Project on behalf of Radisha Fanni Sianti
</p>

## Abstract
<p align="justify">
The national inflation rate is an important indicator in analyzing a country's economic growth. Inflation rates that are managed properly can prevent a country's economy from declining. In the national inflation rate data, the ARIMA (Autoregressive Integrated Moving Average) model was used, and heteroscedasticity was detected, so the ARCH-GARCH (Autoregressive Conditional Heteroskedasticity-Generalized Conditional Heteroskedasticity) time series model was used. The appropriate model is ARCH(1), with a very large MAPE (Mean Absolute Percentage Error) value of 34.662%. Therefore, error correction is carried out using the Kalman Filter to get a smaller error value. The final results show that the Kalman Filter can improve the estimation results marked by the MAPE ARCH-Kalman Filter value being smaller than the ARCH model. The best estimation result on the national inflation rate data is the Kalman Filter polynomial of degree 2 with a value of Q=R=0.01, with the smallest MAPE value of 1.0035%.
</p>

## Dataset
<p align="justify">
The data used is national inflation rate secondary data from the official website of Bank Indonesia from January 2011 to December 2020. The data is divided into 2, namely in-sample data and out-sample data. The in-sample data used is 108 (January 2011 – December 2019), while the out-sample data is 12 (January 2020 – December 2020). In-sample data is used to construct the model, and out-sample data is used to check the model's accuracy. In this study, the national inflation rate data is represented by $X_t$.
</p>

## Visualization of National Inflation Data
<div align="center">
  
  ![image](https://github.com/dishaadis/Estimation-of-National-Inflation-Rate-Using-ARCH-GARCH-Kalman-Filter/assets/82490582/f0189a17-8354-4558-8928-a83586245284)

</div>
<p align="justify">
Visually it can be seen that the time series plot of national inflation rate data has an irregular and fluctuating pattern so that the data can be categorized into data that is not stationary concerning the mean. In addition, it can be seen that the data does not fluctuate around the median value, and the trend does not follow the horizontal axis. So the national inflation rate data is not stationary concerning the mean.
</p>
<div align="center">
  
  ![image](https://github.com/dishaadis/Estimation-of-National-Inflation-Rate-Using-ARCH-GARCH-Kalman-Filter/assets/82490582/f258cf31-3954-4bd2-9728-ea5aebd3073a)

</div>
<p align="justify">
The Box-Cox plot shows the value of λ with a 95% confidence value between -0.43 and 0.62 with an estimated value of 0.07 and a rounded value of 0. This shows that the national inflation rate data is not stationary concerning the variance because the rounded value is not equal to 1. To overcome this problem, a Box-Cox Transformation can be performed to obtain a rounded value equal to 1.
</p>

## Analysis Results
### 1. Stasionarity
#### 1.1 Stationarity of Variance
<p align="justify">
It is known that the national inflation rate is not stationary with respect to the variance, it is necessary to carry out a transformation using the following formula:
<p align="center">
  $Y_t = ln(X_t)$ 
</p>
</p>

#### 1.2 Stationarity of Mean
<p align="justify">
Stationarity of time series data can be done by carrying out the Augmented Dickey-Fuller (ADF) test. The Augmented Dickey-Fuller test is a formal concept introduced by David Dickey and Wayne Fuller to determine whether data has a unit root. Based on the time series plot, it can be seen that the national inflation rate is not stationary concerning the mean, so it is necessary to do differencing on the national inflation rate data. Differentencing can be done with the following formula:
<p align="center">
  $Z_t = Y_t - Y_{t-1}$ 
</p>
After transformation and differencing, to prove the stationary national inflation rate data, it is necessary to carry out the Augmented Dickey-Fuller (ADF) test with the following results:

<div align="center">
  
![image](https://github.com/dishaadis/Estimation-of-National-Inflation-Rate-Using-ARCH-GARCH-Kalman-Filter/assets/82490582/19e554a6-d57c-435d-ad67-8af4a853e622)
</div>
Based on the second Augmented Dickey-Fuller (ADF) test, it is proven that the national inflation rate data is stationary concerning the variance and the mean, so the inflation rate data can be continued by identifying the ARIMA model by checking the ACF (Autocorrelation Function) plot and PACF (Partial Autocorrelation Function).
</p>

### 2. ARIMA Model Identification


















<p align="justify">
</p>
<p align="justify">
</p>
<p align="justify">
</p>



