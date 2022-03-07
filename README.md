# ML-SP-500

Get my notebook: https://colab.research.google.com/drive/10ZDiH_W0ZCLICRZA5oHJqYyj-lwKTx-Q?usp=sharing

I. Introduction: Research Question and Problem for Management

The S&P 500 dataset consists of the Date, Open price, high price, low price, closing price, adjusted closing price, and volume of the S&P 500. The values were taken from the Yahoo Finance website for the timeframe starting with January 2, 2014 and ending December 28, 2018. This specific time period was selected in order to create a model that could predict the last 20% of the data, and the timeframe during the pandemic was not chosen due to the volatility of the market between 2019 and 2022. A model that can correctly predict the S&P adjusted closing price would be extremely beneficial to future investors. It could also aid to prepare for periods of sudden depression in the market and give time to react.

II. Analysis of Dependent Variable (Adjusted Close Price)

An initial analysis of the dependent variable 'Adj Close**' shows that the overall trend of the data was to increase with time. The minimum adjusted closing price was $1741.89 and the maximum adjusted closing price was $2930.75. The mean was $2255.74 with a standard deviation of $312.63. The dataset consisted of 1257 dates which each had a given adjusted closing price and other key variables (such as open, high, and low price). 

![image](https://user-images.githubusercontent.com/97359451/156949143-6d729268-dc46-49ab-94e5-3dad867e4399.png)
Figure 1. Adjusted Closing Price over Time between 2014 and 2019

III. Models

The full dataset was split with the first 80% of the data being the training set and the last (most recent) 20% of the data being the test set. Minmax scaler was used to scale the data, which was next transformed and reshaped to put into the models. The following models were created for the training data: RNN, univariate LSTM, vanilla LSTM, stacked LSTM, bidirectional LSTM, and CNN LSTM. Prediction vs real S&P 500 adjusted closing prices for each model can be seen in the figures below. Root mean square error was taken for the train and test data. The best model was the Stacked LSTM, with an rmse train score of 17.80 and an rmse test score of 48.11. 

![image](https://user-images.githubusercontent.com/97359451/156949318-b1190bc4-5544-481c-94aa-9ae9d0622345.png)
Figure 2. RNN Model Prediction

![image](https://user-images.githubusercontent.com/97359451/156949340-8549cb84-7805-4947-a99f-eac9a551b463.png)
Figure 3. Vanilla LSTM Model Prediction

![image](https://user-images.githubusercontent.com/97359451/156949351-46d465eb-ff0d-404f-8344-b8d2bef29a59.png)
Figure 4. Stacked LSTM Model Prediction

![image](https://user-images.githubusercontent.com/97359451/156949366-934355bd-5604-4a44-9803-a0329012cc78.png)
Figure 5. Bidirectional LSTM Model Prediction

![image](https://user-images.githubusercontent.com/97359451/156949377-0a940d99-7421-4712-afb2-06f9bbcea8fc.png)
Figure 6. CNN LSTM Model Prediction

IV. Conclusions

After initial analysis of the adjusted closing price for the S&P 500 data, a plot showed that the price increased between 2014 and 2019. The models tested were able to follow the general trend of the data, but missed accurately and precisely predicting the price for the test data. Overall, the stacked LSTM model performed the best on the test data and also had the highest rmse score for the train data. This model can be iteratively trained to make better predictions, and ultimately used to predict fluctuations in the market from day to day. Accurate predictions can help investors know when to move money around, and can also help to predict steep drops or inclines in the changing market. 
