## Pre-Provision Net Revenue (PPNR) Modeling using LSTM Networks
This project demonstrates the development of an advanced PPNR model using Long Short-Term Memory (LSTM) networks, a type of recurrent neural network that is well-suited to modeling time series data.

# Overview
Pre-Provision Net Revenue (PPNR) modeling is a critical component of the Comprehensive Capital Analysis and Review (CCAR) process established by the Federal Reserve in the United States. It is a projection of a bank's net revenue, excluding loan loss provisions and extraordinary items. PPNR is a key input into stress testing exercises and is used to assess a bank's capital adequacy.

# Data
In this project, we use hypothetical data for the following variables:

Loan Balance
Deposit Balance
Non-Interest Income
Non-Interest Expense
Net Charge-Offs
We generate this data for 20 quarters (5 years).

#vModel
We use an LSTM network to model the time series data. The model has the following architecture:

First LSTM layer with 50 units and 'relu' activation function. We return sequences from this layer because we have another LSTM layer following this one.
Second LSTM layer with 50 units and 'relu' activation function.
Dropout layer to prevent overfitting. We drop 20% of the neurons.
Dense layer to produce the output. Since we have 5 features in our data, we have 5 units in the dense layer.
Results
The LSTM model is trained on the historical data and used to make predictions for the next 5 quarters. The predictions are then plotted along with the actual historical data.

# Usage
To run the notebook, you need to have Python and the following libraries installed:

numpy
pandas
matplotlib
sklearn
keras
