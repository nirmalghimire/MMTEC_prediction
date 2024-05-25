# MMTEC_prediction
This project focuses on forecasting the future stock prices of MMTec. It leverages historical stock price data, utilizing both ARIMA and LSTM models to predict potential price trends over different time horizons. The data is sourced from a CSV file named "MTC.csv," containing daily stock prices with attributes like 'Date,' 'Open,' 'High,' 'Low,' 'Close,' 'Adj Close,' and 'Volume.'

The initial steps involve mounting Google Drive to access the dataset and importing essential libraries such as Keras, NumPy, Pandas, and Matplotlib. The dataset is then loaded, and the 'Date' column is converted to datetime format and set as the index for time series analysis.

The 'Close' prices are extracted and normalized using MinMaxScaler to prepare the data for the LSTM model. The dataset is split into training and testing sets, with 80% allocated for training and 20% for testing.

An ARIMA model is fitted to the training data, and predictions are made for one week, one month, and six months ahead. The results are plotted, showcasing the training data, test data, and the forecasted values for each time horizon.

The program proceeds to build an LSTM model for forecasting. It defines a function to create datasets for training and testing, reshapes the input data, and constructs the LSTM model with specified layers and an Adam optimizer. The model is trained on the training data, and predictions are made for the same time horizons as the ARIMA model.

The LSTM predictions are then inverse transformed to their original scale, and the results are plotted alongside the training and test data. The plot illustrates the actual stock prices and the forecasted values using the LSTM model.

In the subsequent sections, the code refines the data preprocessing and model building steps. It normalizes the entire dataset, splits it into training and testing sets, and creates datasets for the LSTM model. The LSTM model is rebuilt and trained, and predictions are made for the specified time horizons.

Finally, the code generates a plot displaying the actual stock prices and the LSTM model's predictions for one week, one month, and six months. The plot provides a visual representation of the model's performance in forecasting future stock prices.
