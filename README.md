**# Stock-prediction-using-ARIMA
**OBJECTIVE:**
Arima model is one of the models that we have to predict the value of a time series upto n number of steps in the futer

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

**Backend:**
Arima model works by taking three parameters (p,d,q):
. where p stands for AR- Aturo regressive
. where d stands for I- Integrated
. where q stands for MA- moving average
this is also know as the order of the model

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

**Process:**
we start by import the nessecary libraries:

from statsmodels.tsa.arima.model import ARIMA
from statsmodels.tsa.stattools import adfuller

then we split the data into training and testing, and from this command ---> from pmdarima import auto_arima
we will run this to our train data to find the best order of the model
and then apply that order and train our model

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

**Result:**
The ARIMA model seems to be working very nicely but the drawback is that it cannot be put into a real trading strategy because if you see closely, it almost gives the lagged version of the times seires, in othere it is almost equal the result of

time_series.shift(n)
where 'n' is the time period roughly reffering to 1 or 2 days
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx



