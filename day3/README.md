# Core Concepts: Convolutional Neural Networks (CNNs)

### 1. What advantages do CNNs have over traditional fully connected neural networks for image data?
CNNs are much better for image tasks because they look at smaller regions of the image (local patterns) rather than treating every pixel equally.  
This makes them:
- More efficient (fewer parameters than fully connected networks).
- Better at recognising shapes, edges, and textures.
- Able to capture spatial structure in images (like eyes on a face or stripes on a shirt).


### 2. What is the role of convolutional filters/kernels in a CNN?
Filters (also called kernels) slide over the image and detect features like edges, corners, or textures.
- Early layers learn simple patterns (lines, edges).
- Deeper layers combine these into complex features (faces, objects).
In short, kernels are like “feature detectors” that help the network understand images step by step.


### 3. Why do we use pooling layers, and what is the difference between MaxPooling and AveragePooling?
Pooling layers reduce the size of feature maps, making the model faster and less likely to overfit.
- **MaxPooling** keeps the most important value in each region (strongest feature).
- **AveragePooling** keeps the average of values in each region (overall trend).
Most CNNs use MaxPooling since it focuses on the most relevant details.


### 4. Why is normalization of image pixels important before training?
Images usually have pixel values between 0 and 255. Normalising them (e.g, scaling to 0–1) makes training stable and faster because:
- The network doesn’t have to deal with very large values.  
- Gradients flow more smoothly.  
- It helps the model converge (learn) quicker.  


### 5. How does the softmax activation function work in multi-class classification?
Softmax takes the raw output scores from the model and turns them into probabilities that sum up to 1.  
For example, if predicting clothes, the model might say:  
- Shirt: 0.70  
- Trouser: 0.20  
- Shoe: 0.10  
This means the model is 70% confident it’s a shirt.  


### 6. What strategies can help prevent overfitting in CNNs?
Overfitting happens when the model learns the training data too well but struggles on new data.  
Common fixes are: 
- **Dropout:** randomly “switch off” some neurons during training.  
- **Data Augmentation:** create new training images by rotating, flipping, or zooming existing ones.  
- **Regularisation:** methods like L2 weight decay to keep weights small.  
- **Early stopping:** stop training when validation accuracy stops improving.  


### 7. What does the confusion matrix tell you about model performance?
A confusion matrix shows where the model is getting predictions right and where it is going wrong.  
- The diagonal shows correct predictions.  
- Off-diagonal values show misclassifications.  
It’s very useful for spotting patterns, e.g. the model often confusing shirts with coats.  


### 8. If you wanted to improve the CNN, what architectural or data changes would you try?
Ways to improve include: 
- Adding more convolutional layers to capture deeper features.  
- Using pretrained models (like ResNet or VGG) for transfer learning.  
- Increasing training data or using better augmentation.  
- Trying different optimisers or tuning learning rate.  
- Using techniques like Batch Normalisation to stabilise training.  

