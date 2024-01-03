# Google Stock Price Prediction using LSTM :chart_with_upwards_trend:

![image](https://github.com/rhythmbhavsar/Google-Stock-Price-Prediction/assets/98228696/94b593c7-97a7-4830-8131-00d5c9ed5110)



## :pushpin: Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Data](#data)
- [Model](#model)
- [Results](#results)

  
## Overview

The Stock Price Prediction using LSTM is a project aimed at forecasting the closing prices of stocks by employing deep learning techniques, specifically utilizing Long Short-Term Memory (LSTM) neural networks. This project focuses on analyzing historical stock market data and building an LSTM model capable of predicting future stock prices based on past trends.



## Features

- **LSTM Model:** Utilizes a deep learning LSTM architecture known for capturing long-term dependencies within sequential data.
- **Data Preprocessing:** Includes data cleaning, normalization, and feature selection to prepare the dataset for training the model.
- **Prediction:** Generates predictions for the closing prices of stocks based on historical data.
- **Evaluation:** Assesses the model's performance using metrics like Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE).
- **Visualization:** Provides visual representations of predicted vs. actual stock prices through graphs and charts for better comprehension.

## Installation


```bash
# Clone the repository
git clone https://github.com/your-username/stock-price-prediction.git

# Navigate to the project directory
cd stock-price-prediction

```


## Data

- Dataset Name: [[Google Stock Dataset](https://www.kaggle.com/datasets/shreenidhihipparagi/google-stock-prediction)]
- Description: This dataset compiles crucial stock metrics like close, high, low, and open prices, alongside volume, adjusted prices, dividend cash, and split factors. These metrics provide a comprehensive view of a stock's trading activity, price adjustments due to corporate events, and assist in historical analysis and predictions for analysts and traders.

## Model

The LSTM2 model is a sequential neural network comprised of three LSTM layers followed by a final prediction layer. Each LSTM layer contains a certain number of units (memory cells) and is followed by a dropout layer, aimed at preventing overfitting by randomly dropping a fraction of neurons during training. The architecture is as follows:

1. **First LSTM Layer (150 Units):**
   - Input shape: (length, X_train.shape[2])
   - Return sequences: True
   - Dropout rate: 0.2

2. **Second LSTM Layer (100 Units):**
   - Input shape: (length, X_train.shape[2])
   - Return sequences: True
   - Dropout rate: 0.2

3. **Third LSTM Layer (100 Units):**
   - Input shape: (length, X_train.shape[2])
   - Return sequences: False (Last LSTM layer doesn't return sequences)
   - Dropout rate: 0.2

4. **Final Prediction Layers:**
   - Dense layer with 50 units
   - Dense layer with 5 units (number of features)
   - Output layer with the same number of units as the input shape (X_train.shape[2])

## Results

- Displaying the Comparative Visualization between Actual and Predicted Closing Prices

 ![image](https://github.com/rhythmbhavsar/Google-Stock-Price-Prediction/assets/98228696/b1be59dc-cb67-4f7b-a00f-d70d30d81d23)


- Visulizing Loss and Mean Absolute Error vs. Epochs

![image](https://github.com/rhythmbhavsar/Google-Stock-Price-Prediction/assets/98228696/a9408852-f152-4276-ba4f-c5c2997d1e3e)



