# Wine Dataset Classification Pipeline

This project focuses on solving a classification problem with 3 classes using the Wine dataset. The pipeline includes data preprocessing, model building, and performance evaluation steps.

## Dataset Description

- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/109/wine)
- **Problem:** Classification with 3 classes.
- **Preprocessing:** Min-Max scaling and replacing NaN values with the mean value of each class.

## Pipeline Steps

1. **Data Preprocessing:**
   - Min-Max scaling: Normalize the feature values.
   - Replace NaN values: Replace missing values with the mean value of each class.

2. **Data Splitting:**
   - Divide the data into 10% test and 90% train using stratified sampling.

3. **One-Hot Encoding:**
   - Encode each class using one-hot encoding:
     - Class 1: [1, 0, 0]
     - Class 2: [0, 1, 0]
     - Class 3: [0, 0, 1]

4. **Model Building:**
   - Use a Softmax activation in the last layer to train the network to recognize the one-hot encoding.
   - Employ the multi-layer perceptron (MLP) network using TensorFlow and Keras.
   - Perform parameter exploration using tenfold cross-validation design with stratified sampling:
     - Number of layers: [1, 2, 3]
     - Neurons per layer: [32, 64, 128]
     - Learning rate: [0.001, 0.01, 0.1]

5. **Performance Evaluation:**
   - Use F1 score for performance evaluation.
   - Explore the best parameters for the dataset while reducing bias towards a specific data splitting using cross-validation.

6. **Pipeline Implementation:**
   - Create a custom pipeline by passing the output of one library function to the next.
   - Add control flow to organize the tenfold cross-validation experiments.

## References
- [NOMIDL: What is the difference between Sigmoid and Softmax activation function?](https://www.nomidl.com/deep-learning/what-is-the-difference-between-sigmoid-and-softmax-activation-function/)
- [Scikit-learn: Cross-validation](https://scikit-learn.org/stable/modules/cross_validation.html)

