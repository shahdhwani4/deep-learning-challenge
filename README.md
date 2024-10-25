# Neural Network Model for Alphabet Soup Funding Success Prediction

## Overview of the Analysis

The primary goal of this analysis was to develop a deep learning model capable of predicting the success of organizations applying for funding from Alphabet Soup. By analyzing a dataset containing over 34,000 funded organizations, the model aims to help the nonprofit foundation make data-driven decisions regarding funding allocation. The success of these applicants is defined by the effective use of the granted funds, indicated by the `IS_SUCCESSFUL` variable in the dataset.

The analysis employed a neural network to classify applicants based on various features that reflect their characteristics and operational contexts. This predictive capability is critical for optimizing funding decisions and ensuring resources are allocated to the most promising organizations.

## Results

### Data Preprocessing

**Target Variable:**

- `IS_SUCCESSFUL`: This binary variable indicates whether the funding was used effectively.

**Feature Variables:**

- `APPLICATION_TYPE`
- `AFFILIATION`
- `CLASSIFICATION`
- `USE_CASE`
- `ORGANIZATION`
- `STATUS`
- `INCOME_AMT`
- `SPECIAL_CONSIDERATIONS`
- `ASK_AMT`

**Variables to Remove:**

- `EIN` and `NAME`: These columns serve only as unique identifiers and do not contribute to the model's predictive capabilities. Therefore, they were excluded from the feature set.

### Compiling, Training, and Evaluating the Model

**Neurons, Layers, and Activation Functions:**

The architecture of the neural network model consisted of:
- **Input Layer:** 80 neurons, corresponding to the number of features in the dataset.
- **Hidden Layer 1:** 30 neurons with a ReLU activation function, chosen to allow for non-linear relationships in the data.
- **Output Layer:** 1 neuron with a sigmoid activation function to provide a binary output (successful or not).

The selection of this structure aimed to capture the complexities of the relationships between the features and the target while maintaining a manageable number of parameters to avoid overfitting.

**Target Model Performance:**

The model achieved an accuracy of 72% on the test data, which fell short of the target performance of 75%.

### Steps Taken to Increase Model Performance:

- **Architectural Adjustments:** Experimented with varying the number of hidden layers and neurons.
- **Activation Functions:** Tested different activation functions (e.g., Leaky ReLU) to enhance learning in deeper layers.
- **Dropout Regularization:** Introduced dropout layers to minimize overfitting.
- **Learning Rate and Batch Size Tuning:** Adjusted the learning rate and batch size for optimal convergence.
- **Epochs Increase:** Increased the number of epochs to allow the model more opportunities to learn from the training data.

## Summary

The deep learning model successfully established a foundational predictive framework for assessing the success of funding applicants. Despite achieving a 72% accuracy, it did not meet the desired target of 75%, indicating further optimization is needed.
