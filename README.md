# Stock-Price-Prediction-using-Stacked-LSTM

**Step 1: Dataset Acquisition**

- Begin by obtaining historical stock price data for AAPL. You can find this data from various financial sources, such as Yahoo Finance or a dedicated financial data provider.
- The dataset typically includes information such as Date, Open, High, Low, Close, Volume, and potentially other columns. For this project, we're primarily interested in the 'Close' price, which represents the closing price of AAPL stock for each trading day.

**Step 2: Data Preprocessing**

- Load the acquired dataset into a Pandas DataFrame, a powerful data manipulation tool in Python.
- Convert the 'Date' column to a datetime data type and set it as the DataFrame's index. This enables us to work with time-series data effectively.
- Explore the dataset by printing the first few rows to understand its structure and contents. You can also use data.info() to obtain basic information about the dataset, including data types and missing values.

**Step 3: Exploratory Data Analysis (EDA)**

- To gain insights into the data, perform exploratory data analysis.
- Visualize the AAPL stock price data over time using a line plot. This allows you to observe trends, patterns, and potential outliers in the historical prices.
- Calculate and visualize daily returns, which show how much the stock price changes from one day to the next. This helps identify periods of growth and decline.

**Step 4: Data Normalization**

- Normalize the 'Close' price data using Min-Max scaling. This scaling technique transforms the values to a consistent range between 0 and 1, making it easier for the neural network to learn.

**Step 5: Data Splitting**

- Split the normalized data into training and testing sets. In this project, we use 80% of the data for training and the remaining 20% for testing. This separation allows us to evaluate the model's performance on unseen data.

**Step 6: Model Building**

- Define the architecture of the LSTM (Long Short-Term Memory) model. LSTMs are well-suited for time series prediction tasks because they can capture long-term dependencies.
- Create a stacked LSTM model with multiple LSTM layers. Stacked LSTMs can capture complex temporal patterns in the data.

**Step 7: Model Compilation**

- Compile the LSTM model by specifying the optimizer and loss function. In this case, we use the 'adam' optimizer and mean squared error (MSE) as the loss function. MSE is commonly used for regression tasks like stock price prediction.

**Step 8: Model Training**

- Train the LSTM model using the training dataset. During training, the model learns to make predictions based on the historical stock price data.
- Monitor the training process, including changes in training and validation loss, over multiple training epochs.
- I have trained the model for 200 epochs.

**Step 9: Model Evaluation (Not performed)**

- After training, you can evaluate the model's performance on the testing dataset to assess how well it generalizes to unseen data. However, this tutorial focuses on prediction and visualization.

**Step 10: Prediction**

- Utilize the trained LSTM model to make predictions on the testing dataset. Predictions are generated in sequences of data points.

**Step 11: Inverse Scaling**

- Inverse transform the predicted and actual values to bring them back to their original scale (USD) from the normalized scale. This step is crucial for comparing predictions with actual stock prices.

**Step 12: Result Visualization**

- Finally, visualize the actual and predicted stock prices over time. Plotting these values on a graph allows you to assess how effectively the LSTM model predicts future stock prices based on historical data.
