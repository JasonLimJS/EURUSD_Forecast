# Prediction of EUR/USD with Neural Network Ensemble

# 1.Data Extraction

This Python notebook details all the steps involved in importing all relevant data sets via Exchange rates API and Federal Reserve Bank of of St. Louis API.

Target variable: Daily EUR/USD exchange rate

Predictors considered:

1. Daily 1- Month USD London Interbank Offered Rate (LIBOR)
2. Daily 3- Month USD London Interbank Offered Rate (LIBOR)
3. Daily 1- Month EUR London Interbank Offered Rate (LIBOR)
4. Daily 3- Month EUR London Interbank Offered Rate (LIBOR)
5. Daily Last Price of Standard & Poor (S&P) 500 Index
6. Daily Last Price of Chicago Board of Exchange (CBOE) Volatility Index (VIX)
7. Daily Moody's Seasoned AAA Bond Spread
8. Daily 2- Year Intercontinental Exchange (ICE) Swap Rate
9. Daily 3- Year Intercontinental Exchange (ICE) Swap Rate
10. Daily 5- Year Intercontinental Exchange (ICE) Swap Rate
11. Daily 7- Year Intercontinental Exchange (ICE) Swap Rate

# 2.Training Deep Learning Model

This Python notebook details all the steps involved in training a neural network ensemble. After some hyperparameter tuning, it has been observed that EUR/USD exchange rate could be most accurately being predicted with an ensemble of 10 neural networks where each neural network contains 2 hidden layers that come with sigmoid activation function whereas the output layer is activated via linear function.

EUR/USD exchange rate would be most accurately predicted with only USD 3M LIBOR and EUR 3M LIBOR as inputs. The reasons for that might be due to the usage of these 2 rates in a lot of derivatives fixing.

Model performance:

RMSE: 0.13987 (Around 88 pips difference with the actual exchange rate on average)
