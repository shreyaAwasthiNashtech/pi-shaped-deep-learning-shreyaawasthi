## Day 2: Core Concept Questions

### Q1. What is the benefit of using RNNs (or LSTMs) over traditional feedforward networks for time-series data?

Traditional feedforward networks treat each input separately, without remembering what came before. RNNs, and especially LSTMs, are built to remember patterns over time. This memory helps them understand trends, sequences, and context, which is very important for time-series data like stock prices.


### Q2. Why is sequence framing (input windows) important in time series forecasting?

In time-series forecasting, the future depends on the past. Sequence framing (like using sliding windows) helps the model look at a chunk of past values together before making the next prediction. Without it, the model would miss the connection between yesterday and tomorrow.


### Q3. How does feature scaling impact training of RNN/LSTM models?

Feature scaling makes all numbers fall into a similar range (like 0 to 1). This helps the model learn faster and prevents large values (like trading volume) from dominating smaller ones (like stock price changes). It’s like levelling the playing field for every feature.


### Q4. Compare SimpleRNN and LSTM in terms of handling long-term dependencies.

* **SimpleRNN**: Good for short sequences, but it forgets information quickly because of the vanishing gradient problem.
* **LSTM**: Designed with special “memory cells” that can remember things for longer, making it better for long-term dependencies in time-series.


### Q5. What regression metrics (e.g., MAE, RMSE) are appropriate for stock price prediction, and why?

* **MAE (Mean Absolute Error):** Tells us the average absolute difference between actual and predicted prices. Easy to understand.
* **RMSE (Root Mean Squared Error):** Penalises larger mistakes more, so it highlights big errors.
  Both are common because stock predictions care about how close the prediction is, and big mistakes can be costly.


### Q6. How can you assess if your model is overfitting?

You can check if the training loss is going down but the validation loss is getting worse. This means the model is “memorising” the training data but not generalising well to unseen data. Visualising training vs validation curves helps spot overfitting.


### Q7. How might you extend the model to improve performance (e.g., more features, deeper network)?

* Add more features like volume, moving averages, or news sentiment.
* Use a deeper or more complex network like stacked LSTMs or GRUs.
* Try dropout or regularisation to avoid overfitting.
* Tune hyperparameters such as learning rate or sequence length.


### Q8. Why is it important to shuffle (or not shuffle) sequential data during training?

For time-series, the order of data matters. If you shuffle blindly, the model will lose the sense of sequence. Normally, you don’t shuffle the data but you might shuffle batches carefully when working with multiple sequences (like from different stocks).


### Q9. How can you visualize model prediction vs actual values to interpret performance?

You can plot actual stock prices and predicted stock prices on the same line chart. If the lines follow each other closely, the model is doing well. Scatter plots (predicted vs actual) are also useful to see how close the predictions are to reality.


### Q10. What real-world challenges arise when using RNNs for stock price prediction?

* Stock prices are influenced by unpredictable events (like news or politics).
* Data can be noisy and volatile.
* Models can easily overfit to historical data but fail in real trading.
* Sudden market shifts (like COVID-19) break old patterns, making past data less useful.

