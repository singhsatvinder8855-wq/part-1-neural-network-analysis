# part-1-neural-network-analysis

# Neural Network Fundamentals and Training Behavior Analysis

### Dataset Source & Path
* **Original Link:** https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJV-wBvUYs?usp=sharing
* **Project Folder Path:** `ai_project_synthetic_datasets/part_1_neural_network_analysis/customer_churn_nn.csv`

---

### 1. Approach & Steps
* **Dataset Exploration:** Checked shape, types, missing values, and target distribution.
* **Preprocessing:** Handled features with dummy variables and standardized numerical inputs using `StandardScaler`.
* **Model Architecture:** Built a feed-forward neural network with an explicit `Input` layer, one `Dense` hidden layer (ReLU), and a final `Dense` output layer (Sigmoid).
* **Experiments:** Tested three different configurations changing layers, learning rates, activation functions, and batch sizes.

---

### 2. Task 6: Final Reflection Report

#### A. What role do weights and biases play in the model?
* **Weights:** These are learnable parameters that control the signaling strength of each input feature, scaling their importance toward the churn prediction.
* **Biases:** This is an offset value added to the weighted sum, allowing the activation function to shift on the graph so neurons can activate even if all input features are zero.

#### B. Why is an activation function required?
* Without them, the entire network collapses mathematically into a single linear regression calculation. Activation functions like ReLU and Sigmoid introduce non-linearity, allowing the model to learn complex structures like customer churn.

#### C. What happens when the learning rate is too high or too low?
* **Too High (e.g., LR = 0.5):** The updates overshoot the minimum loss violently, causing the loss to oscillate or completely diverge, resulting in random-chance accuracy.
* **Too Low (e.g., LR = 0.001):** The steps are so small that training becomes extremely slow, risking getting trapped in a sub-optimal local minimum.

#### D. Did your model show signs of underfitting or overfitting? Explain.
* **Observation:** The baseline model trained in Task 4 showed **no significant signs of overfitting or underfitting**.
* **Explanation:** Both the final training accuracy and testing accuracy values remained closely aligned within a minimal 1-2% margin. This proves that the model did not simply memorize the training data (overfitting), nor did it fail to capture the underlying data structure (underfitting). Instead, it demonstrated strong generalization capabilities on unseen data due to proper feature scaling and a balanced network capacity.
