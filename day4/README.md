# Day 4 – Core Concept Questions: Model Optimisation Techniques

### 1. Why is hyperparameter tuning important, and what trade-offs does it involve?
Hyperparameter tuning helps you find the best combination of settings (like learning rate, batch size, or number of filters) that make the model learn effectively. If the values are too high or too low, the model may either fail to learn or overfit the training data.  
The trade-off is usually between accuracy, training time, and computing cost. A highly tuned model might perform better but could take much longer to train and require more resources.


### 2. How does model pruning or compression impact performance and resource usage?
Pruning and compression reduce the size of the model by removing unnecessary weights or simplifying layers. This usually makes the model faster and lighter, which is useful for deployment on devices with limited memory. However, if too much pruning is done, accuracy can drop as the model may lose some of its ability to capture important patterns.


### 3. Why is dropout effective in preventing overfitting?
Dropout works by randomly “switching off” a portion of neurons during training. This forces the network to not rely too heavily on specific neurons, which makes it more general and less likely to memorise training data. As a result, dropout often leads to better performance on unseen data.


### 4. What challenges arise when deploying deep learning models in production?
Deploying models in real-world environments can be tricky. Common challenges include:
- Model size being too large for mobile or edge devices  
- High latency during inference  
- Ensuring the model works reliably with live, noisy data  
- Monitoring drift when data changes over time  
- Balancing performance with hardware limits  


### 5. How does TensorFlow Lite (or ONNX, TorchScript) help in deployment optimisation?
Frameworks like TensorFlow Lite, ONNX, and TorchScript allow you to convert heavy models into lighter formats. These formats are optimised for inference on mobile, web, or edge devices. They reduce model size, improve inference speed, and ensure compatibility across platforms without needing the full training framework.


### 6. What is the balance between model accuracy and efficiency in real-world applications?
In real-world use, you often can’t just aim for maximum accuracy. A highly accurate model may be too slow or heavy to use in practice. The balance is about finding a model that is “good enough” in accuracy while also being fast, reliable, and efficient enough to run on the target hardware.


### 7. How can hardware (GPU, TPU, Edge devices) influence optimisation strategies?
Different hardware has different strengths. GPUs are great for parallel training, TPUs are even faster for large-scale deep learning, and edge devices need lightweight models. The choice of hardware will directly influence optimisation decisions — for example, you may prune or quantise more aggressively if you know the model must run on a mobile phone.


### 8. Looking ahead, how might optimisation differ for Transformer-based models compared to CNNs/RNNs?
Transformer models (like those used in NLP and vision) are usually much larger and more resource-hungry than CNNs or RNNs. Optimisation for Transformers often focuses on:
- Reducing attention complexity  
- Using distillation (training a smaller “student” model)  
- Quantisation and pruning to fit them onto edge devices  
- Specialised hardware accelerators  

As models grow in size, optimisation for Transformers will continue to be a major area of research and development.


