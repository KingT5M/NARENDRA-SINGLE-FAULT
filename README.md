NARENDRA-SINGLE-FAULT

This is a deep reinforcement learning model used for detecting and classifying faults in Single Fault scenarios.
It implements a Convolutional Neural Network (CNN) combined with Long Short-Term Memory (LSTM) architecture.
It incorporates reinforcement learning to optimize fault detection and classification

The architecture parameters of the proposed model.
    Layer Size and Parameters,
    CNN Layer 1 Filters: 8, Kernel Size: 2, Activation: ReLU, Input Shape: [30 × 2], Output Shape: [30 × 8],
    CNN Layer 2 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8],
    CNN Layer 3 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8],
    CNN Layer 4 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8],
    CNN Layer 5 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8],
    Batch Normalization Layer 1 Output Shape: [30 × 8],
    Max Pooling Layer Pool Size: 2, Output Shape: [15 × 8],
    LSTM Layer 1 Neurons: 64, Activation: ReLU, Output Shape: [15 × 64],
    LSTM Layer 2 Neurons: 64, Activation: ReLU, Output Shape: [15 × 64],
    LSTM Layer 3 Neurons: 64, Activation: ReLU, Output Shape: [15 × 64],
    LSTM Layer 4 Neurons: 64, Activation: ReLU, Output Shape: 64,
    Batch Normalization Layer 2 Output Shape: 64,
    Flatten Layer Output Shape: 64,
    Output Layer Output Shape: 9,

It also incorporates automatic hyper parameter tuning within the following ranges
Hyper-parameter ranges and values:
    CNN Layers: 0–5,
    LSTM Layers: 0–5,
    Dense Layers: 0–5,
    Epochs: 50–900,
    Max Pooling Layer: 0–1,
    Drop Layer: 0–2,
    Batch Normalization Layer: 0–2,
    Batch Size: 64–150,
    Learning Rate: 0.001–0.0001

## Reinforcement Learning in the Code

Here's a breakdown of the key elements:

**Agent:** The agent is a script that trains and evaluates different versions of the fault detection model using various hyperparameter configurations.

**Environment:** The environment is the training process itself. The agent interacts with it by training models with different hyperparameters and receiving rewards based on their performance on the validation set.

**State:** The state of the environment consists of the current hyperparameter configuration being evaluated.

**Action:** The action taken by the agent is to sample a new set of hyperparameters based on the current state and previous rewards.

**Reward:** The reward is calculated based on the validation performance of the model trained with the current hyperparameters. A high reward is given if precision, recall, and F1-score on the validation set exceed specified thresholds.

**Reinforcement Learning Algorithm:** The code uses the REINFORCE algorithm for exploration and learning. In each episode, the agent samples new hyperparameters, trains a model, and receives a reward. This reward is used to adjust the probabilities of choosing similar hyperparameters in the future, guiding the agent towards better configurations.

**Additional Notes:**

* The code defines specific metrics (precision, recall, F1-score) and thresholds for determining rewards.
* The agent explores different hyperparameter combinations (number of layers, learning rate, etc.) within defined ranges.
* The best hyperparameters found during training are used to train a final model on the entire training data.
* Performance metrics are calculated and visualized for the final model on the validation set.

Overall, the code demonstrates how RL can be effectively used to optimize hyperparameters for a machine learning model, leading to improved performance.

The author is - Ian Mwaniki Kanyi alias King T5M. ALL HAIL T5M.
