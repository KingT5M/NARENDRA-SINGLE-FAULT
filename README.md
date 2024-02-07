# NARENDRA-SINGLE-FAULT
This is a deep learning model used for detecting and classifying faults in Single Fault scenarios.
It implements a Convolutional Neural Network (CNN) combined with Long Short-Term Memory (LSTM) architecture.
The architecture parameters of the proposed model.
    Layer Size and Parameters 
    CNN Layer 1 Filters: 8, Kernel Size: 2, Activation: ReLU, Input Shape: [30 × 5], Output Shape: [30 × 8] 
    CNN Layer 2 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8] 
    CNN Layer 3 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8] 
    CNN Layer 4 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8] 
    CNN Layer 5 Filters: 8, Kernel Size: 2, Activation: ReLU, Output Shape: [30 × 8] 
    Batch Normalization Layer 1 Output Shape: [30 × 8] 
    Max Pooling Layer Pool Size: 2, Output Shape: [15 × 8] 
    LSTM Layer 1 Neurons: 64, Activation: ReLU, Output Shape: [15 × 64] 
    LSTM Layer 2 Neurons: 64, Activation: ReLU, Output Shape: [15 × 64] 
    LSTM Layer 3 Neurons: 64, Activation: ReLU, Output Shape: [15 × 64] 
    LSTM Layer 4 Neurons: 64, Activation: ReLU, Output Shape: 64 
    Batch Normalization Layer 2 Output Shape: 64 
    Flatten Layer Output Shape: 64 
    Output Layer Output Shape: 9 

The author is - Ian Mwaniki Kanyi alias King T5M. ALL HAIL T5M.
