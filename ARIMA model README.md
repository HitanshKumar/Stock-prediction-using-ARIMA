
# ARIMA price prediction

OBJECTIVE: Arima model is one of the models that we have to predict the value of a time series upto n number of steps in the future




## Strategy Idea

- BACKEND: Arima model works by taking three parameters (p,d,q): . where p stands for AR- Aturo regressive . where d stands for I- Integrated . where q stands for MA- moving average this is also know as the order of the model


- Process: we start by import the nessecary libraries:

then we split the data into training and testing, and from  ---> pmdarima we will run this to our train data to find the best order of the model and then apply that order and train our model




## Important code1

This is the import snipt it from the code where i import auto_arima from pmdarima and fidn the best (p,d,q) order for the model

```bash
from pmdarima import auto_arima
p_d_q = auto_arima(df_train, trace = True, supress_warnings = True)

```


## Important code2
This code represents the main loop that we are going to run to get the ARIMA predictions and then appending the actual value of ARIMA and again forming the model, meaning doing 1 prediction at a time, and considering the new/actual values

```bash
predictions = []
for i in range(len(df_test_l)):
    
    model = ARIMA(df_train_l, order=(2,1,2))
    model_fit = model.fit()
    output = model_fit.forecast()
    yhat = output[0]

    predictions.append(yhat)
```
    