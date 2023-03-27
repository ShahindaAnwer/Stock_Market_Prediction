# Air Passengers

## Problem Statement
Airlines use time series prediction to predict the number of passengers they would be getting per month, based on previous calculations as well as the current day's data. The model tries to predict the number of passengers (in units of thousands) in one month, given the number of passemgers the previous month

<p align="center">
    <img src = 'https://user-images.githubusercontent.com/62629426/224588514-bd9f8ffb-b0ea-44b4-8b85-bb6853598fda.PNG' width = '800'>
</p>

## Model

I used Long short term memory (LSTM) as we are dealing with time steps. LSTMs have memory blocks that help them remember previous data. Each memory block has gates, which manage its state and the output. Using the Sigmoid activation function, each block decides whether or not it gets triggered, upon receiving an input sequence. Hence, the state change and information addition both flow conditionally.

![lstm](https://user-images.githubusercontent.com/62629426/225827754-b2d1d573-7c7e-4d64-b9ef-2041cbd12517.png)

Each LSTM has: 
1. Forget gate: Determines which information should be discarded
2. Input Gate: Picks input values that would update the memory state
3. Output Gate: Given the chosen inputs and block's memory, it decides exactly what to output

    and all are conditional

### Libraries: 
- [Tensorflow - Keras](https://www.tensorflow.org/api_docs/python/tf/keras)
- [Numpy](http://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [Scikitlearn](https://scikit-learn.org/stable/)
- [Math](https://docs.python.org/3/library/math.html)

### Accuracy:
- Train loss: 0.0024 
- val_loss: 0.0079
- RMSE: 30.34
