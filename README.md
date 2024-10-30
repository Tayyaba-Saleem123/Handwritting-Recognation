# Handwriting Recognition Project

## Overview
This project implements a handwriting recognition model using a neural network trained on the MNIST dataset.

## Code Description

### Libraries Used
- **NumPy**: Numerical operations
- **Matplotlib**: Visualization
- **TensorFlow/Keras**: Model building and training

### Key Code Sections

1. **Import Libraries**
   ```python
   import numpy as np
   import matplotlib.pyplot as plt
   ```

2. **Set Visualization Styles**
   ```python
   plt.style.use('fivethirtyeight')
   plt.xkcd()
   ```

3. **Create Subplots**
   ```python
   fig, axes = plt.subplots(3, 3, figsize=(12, 15))
   axes = axes.flatten()
   ```

4. **Display Test Images and Predictions**
   ```python
   for i, ax in enumerate(axes):
       img = np.reshape(x_test[i], (28, 28))
       ax.imshow(img, cmap='Greys')
       pred = word_dict[np.argmax(categorical_test[i])]
       ax.set_title("Prediction: " + pred, fontsize=20, fontweight='bold', color='red')
   ```

## How to Run
1. Install the required libraries:
   ```bash
   pip install numpy matplotlib tensorflow
   ```
2. Load your model and test data, then run the script in a Python environment.

## Conclusion
This project visualizes predictions from a handwriting recognition model on the MNIST dataset.

## License
MIT License

