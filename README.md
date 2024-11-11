# Forecast-model-for-stock-data
The thought came to me before I slept -- Application of chaos theory to data analytics, and this project came out of it. 
I downloaded the Reliance stock data comprising 3454 rows and 6 columns containing date, open, high, low, close, adj close, and volume then I got to work. I first performed a time series analysis on the closing price against the date to show the trends
I moved on to checking for Stationarity using the augmented Dickey-Fuller to check if the p-value will be lower than 0.05, the first series was non-stationary—meaning it has trends, seasonality, or other patterns that evolve. Then I have to move forward to differencing it to get a stationary and then check for augmented Dickey-Fuller which gave me -10.57 indicating that it is now stationary. 
I went on to check on seasonal decomposition to show trends, seasonality, and residual(Noise). 
Trends -- The trend appears to capture a longer-term change in the data. It seems relatively stable until around 2018, after which it gradually increases until 2020.
Seasonality -- The seasonality seems to oscillate consistently over time, with a periodic pattern that doesn’t change much in amplitude.
Residual (Noise) -- there is an increase in variability in the residuals after 2020, suggesting some unexplained variability in the data, possibly due to external or unpredictable factors.
I moved on to checking for autocorrelation and partial autocorrelation; autocorrelation -- the autocorrelation is high at lag 0 (1.0), which is expected, as a time series is perfectly correlated with itself.
partial autocorrelation -- The PACF at lag 0 is 1, which is expected since any time series is perfectly correlated with itself.
Then I proceeded to build my model and forecast, I built an ARIMA model resulting in log-likelihood- -15329.427 also with AIC, BIC, and HQIC values being 30664.855, 30683.295, and 30671.441 respectively. Upon evaluation of the RMSE, the result is 19.725
