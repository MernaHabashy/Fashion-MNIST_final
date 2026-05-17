# Fashion-MNIST_final
A Multilayer Perceptron (MLP) built using PyTorch to classify clothing items from the Fashion-MNIST dataset.  
The project explores different architectures and training strategies across multiple experiments using activation functions, learning rates, dropout, and batch normalization.

# Problem Description

The goal is to classify grayscale images of clothing items into **10 categories**.
- Each image is **28×28 pixels**
- Flattened into a **784-dimensional vector**
- Output is one of **10 classes**

This is a **multi-class classification problem**, evaluated using:
- Accuracy
- Cross-Entropy Loss

  # Dataset

- **Name:** Fashion-MNIST  
- **Source:** PyTorch / Keras  
- **Size:**
  - 60,000 training samples
  - 10,000 test samples  

- **Classes (10):**
  T-shirt/top, Trouser, Pullover, Dress, Coat,  
Sandal, Shirt, Sneaker, Bag, Ankle boot

# Preprocessing:
- Images flattened (28×28 → 784)
- StandardScaler normalization applied
- Data split into training and validation sets


# Model Architecture
A flexible **MLP (Multilayer Perceptron)** was implemented:

- Configurable hidden layers
- Adjustable neuron sizes
- Activation functions:
  - ReLU
  - Tanh
- Optional Dropout
- Optional Batch Normalization


# Experiments & Results

| # | Model | Architecture | Activation | LR | Dropout | BatchNorm | Accuracy | Loss
|--|------|-------------|------------|----|----------|------------|----------|----------|
| 1 | Baseline | [256, 128] | ReLU | 0.001 | 0.3 | Yes | 0.893 | 0.2966 |
| 2 | Deep Tanh | [256, 128, 64] | Tanh | 0.001 | 0.2 | Yes | 0.88 | 0.3944 |
| 3 | Optimized Deep | [512, 256, 128] | ReLU | 0.0001 | 0.3 | Yes | 0.894 |  0.3319 |

# Best Model
**Experiment 3** achieved the best performance:
- Deep architecture
- ReLU activation
- Batch Normalization + Dropout
- Lower learning rate
Result:
- Accuracy: ** 0.8944**


# Visualizations

The notebook includes:
- Training vs Validation Loss curves
- Training vs Validation Accuracy curves
- Comparison of all experiments



# Enhancement Techniques

| Technique | Benefit |
|----------|--------|
| Dropout (0.3) | Reduces overfitting |
| Batch Normalization | Stabilizes training |
| Lower Learning Rate | Improves convergence |


# Conclusion

The experiments show that tuning architecture depth, activation functions, and learning rate significantly impacts model performance.  
The optimized model achieved the best generalization on the Fashion-MNIST dataset.
