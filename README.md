# part-1-neural-network-analysis

## Task 6: Final Reflection Report

### 1. What role do weights and biases play in the model?
* **Weights:** Weights are the learnable parameters in a neural network that control the signal strength or relative importance of each input feature. Mathematically, they scale the incoming data. A larger weight value indicates that a specific feature (such as contract type or monthly charges) has a stronger influence on predicting whether a customer will churn.
* **Biases:** The bias is an additional learnable parameter added to the weighted sum of inputs before it passes through the activation function. It acts as an offset shift, allowing the activation function's curve to move left or right on the graph. This ensures that neurons can activate and make meaningful decisions even if all the input feature values happen to be zero.

### 2. Why is an activation function required?
* **Non-Linearity:** Without an activation function, a neural network is just a series of matrix multiplications and additions. Mathematically, stacking multiple layers without activation functions would simply collapse back into a single, basic linear regression model.
* **Complex Patterns:** Activation functions (like **ReLU** in the hidden layer and **Sigmoid** in the output layer) introduce non-linearity into the network. This enables the model to learn complex, multi-dimensional decision boundaries, which is absolutely critical for solving real-world classification problems like customer churn where features interact non-linearly.

### 3. What happens when the learning rate is too high or too low?
* **Too High (e.g., Learning Rate = 0.5):** The optimization algorithm updates the network's weights too aggressively. It overshoots the minimum point of the loss function violently, causing the training loss to oscillate erratically or completely diverge. This leaves the model unstable and unable to learn, resulting in poor accuracy.
* **Too Low (e.g., Learning Rate = 0.001):** The model takes microscopic steps toward the optimal weights. While this makes the training stable, the convergence process becomes extremely slow. The model might require an impractical number of epochs to achieve good performance, or it might get prematurely trapped in a poor local minimum.

### 4. Did your model show signs of underfitting or overfitting? Explain.
* **Observation:** The baseline model trained in Task 4 showed **no significant signs of overfitting or underfitting**. 
* **Explanation:** Both the final training accuracy and testing accuracy values remained closely aligned (within a 1-2% margin of each other). This minimal gap proves that the model did not simply memorize the training data (overfitting), nor did it fail to capture the underlying data structure (underfitting). Instead, it demonstrated strong generalization capabilities on entirely unseen customer dataset validation splits due to proper feature scaling and a balanced network capacity.
