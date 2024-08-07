# Exoplanet Detection Methods Classification

## Overview

This project involves a detailed comparison of Fully Connected Neural Networks (FCNN) and Recurrent Neural Networks (RNN) for classifying exoplanet detection methods. We evaluate the efficacy of these two neural network architectures in accurately classifying various methods of exoplanet detection.

## Dataset

The dataset includes multiple detection techniques such as:
- Astrometry
- Eclipse Timing Variations
- Imaging
- Microlensing
- Orbital Brightness Modulation
- Pulsar Timing
- Pulsation Timing Variations
- Radial Velocity
- Transit
- Transit Timing Variations

## Models

### Fully Connected Neural Network (FCNN)

- **Definition**: A deep learning model where each neuron in one layer is connected to every neuron in the next layer, suitable for fixed-size vector inputs.
- **Architecture**:
  - **Input Layer**: Receives features related to exoplanets and their host stars.
  - **Hidden Layers**: Two layers with 128 neurons each, using ReLU activation and dropout regularization.
  - **Output Layer**: Neurons equal to the number of classes, with a linear activation function.

### Recurrent Neural Network (RNN)

- **Definition**: Designed to recognize patterns in sequential data, though this dataset lacks a natural sequential structure.
- **Architecture**:
  - **Input Layer**: Processes feature vectors of the dataset.
  - **Recurrent Layers**: Two layers with 128 hidden units each, using ReLU activation and dropout regularization.
  - **Output Layer**: Maps the final hidden state to the output classes.

## Performance

### Fully Connected Neural Network (FCNN)

- **Accuracy**: 98.37% on the test set.
- **Confusion Matrix**: Effective classification across different discovery methods.
- **Classification Report**: High precision, recall, and F1-scores for most classes, with lower performance for less frequent classes.

### Recurrent Neural Network (RNN)

- **Accuracy**: 98.52% on the test set.
- **Confusion Matrix**: Effective classification across various discovery methods.
- **Classification Report**: Robust performance for most classes, benefiting from capturing temporal patterns.

### Comparison

Both models exhibit high performance, with RNN slightly outperforming FCNN. FCNN struggles with certain classes like Eclipse Timing Variations, while RNN performs better, achieving a perfect AUC for that class. Both models show `nan` AUC values for classes with insufficient data, indicating the need for a more balanced dataset.

## Conclusion

Both FCNN and RNN models perform exceptionally well for most classes. The RNN shows superior performance for challenging classes and better handling of specific tasks. The confusion matrices and classification reports provide valuable insights into each model's capabilities and limitations.

## Keywords

Exoplanet discovery, Deep learning, Fully Connected Neural Networks, Recurrent Neural Networks, Hyperparameter tuning, Kepler mission, Machine learning

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
