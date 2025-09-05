# pi-shaped-deep-learning-shreyaawasthi

# Core Concept Questions & Answers
**1. What is the role of feature scaling/normalization in training neural networks?**

Neural networks work better when all input features are on a similar scale.
For example, if one feature (like "age") is in the range 20–80 and another (like "salary") is in the range 20,000–80,000, the larger numbers can dominate learning.
Scaling (e.g., bringing values between 0 and 1) makes training faster and more stable.

**2. Why do we split data into training and testing sets?**

We split so that the model can learn from one set (training) and then we check how well it generalises on unseen data (testing).
If we only test on the data it trained on, we might fool ourselves into thinking it’s smarter than it really is.

**3. What is the purpose of activation functions like ReLU or Sigmoid?**

Activation functions add non-linearity. Without them, a neural network would just be a complicated straight line.

ReLU (Rectified Linear Unit): Turns negative values into 0, keeps positives as they are fast and works well in deep nets.

Sigmoid: Squeezes values between 0 and 1 which is good for probabilities in binary classification.

**4. Why is binary cross-entropy commonly used as a loss function for classification?**

Binary cross-entropy measures how far off the predicted probability is from the actual class (0 or 1).
It punishes confident wrong answers more than small mistakes, helping the model learn good probability estimates.

**5. How does the optimizer (e.g., Adam) affect training compared to plain gradient descent?**

Gradient Descent: Takes equal-sized steps for all features. Can be slow or get stuck.

Adam: Adjusts learning speed for each feature automatically, often training much faster and better.
Think of Adam as "smart gradient descent with turbo boost".

**6. What does the confusion matrix tell you beyond just accuracy?
**
A confusion matrix shows how mistakes are made, not just how many.

It shows true positives, true negatives, false positives, and false negatives.
Example: Accuracy might be 95%, but the confusion matrix could reveal that most errors happen when detecting "malignant" tumours, which is more serious.

**7. How can increasing the number of hidden layers or neurons impact model performance?**
More layers/neurons: The network can learn more complex patterns.

But too many, may overfit (memorise training data instead of generalising).
It’s like making a student read more books: helpful up to a point, but too much and they just memorise instead of understanding.

**8. What are some signs that your model is overfitting the training data?**

Very high accuracy on training data but low accuracy on test data.

Loss keeps dropping in training but gets worse on testing.

The model performs too well on known examples but fails on new ones.

**9. Why do we evaluate using precision, recall, and F1-score instead of accuracy alone?**

Accuracy can be misleading when classes are imbalanced.
Example: If 95% of patients are healthy and 5% have cancer, a model that always predicts "healthy" has 95% accuracy but is useless.

Precision: Of all predicted positives, how many were correct?

Recall (Sensitivity): Of all actual positives, how many did we catch?

F1-Score: Balance between precision and recall.

**10. How would you improve the model if it performs poorly on the test set?**
Some common fixes:

Collect more training data.

Try a deeper or different model.

Use dropout or regularisation to reduce overfitting.

Tune hyperparameters (learning rate, batch size, etc.).

Try feature engineering or better scaling.
