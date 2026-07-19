# Medical AI: Diabetes Risk Diagnostic Neural Network

# Pima Indians Diabetes Prediction

This project uses a deep learning neural network built with Keras/TensorFlow to predict the onset of diabetes based on diagnostic measurements. 

## Dataset
The project uses the **Pima Indians Diabetes Database** (`pima-indians-diabetes.csv`). It contains data from Pima Indian women aged 21 or older. 

The dataset includes 8 medical predictor (input) variables and 1 target (output) variable:
1. **Pregnancies:** Number of times pregnant
2. **Glucose:** Plasma glucose concentration a 2 hours in an oral glucose tolerance test
3. **BloodPressure:** Diastical blood pressure (mm Hg)
4. **SkinThickness:** Triceps skin fold thickness (mm)
5. **Insulin:** 2-Hour serum insulin (mu U/ml)
6. **BMI:** Body mass index (weight in kg/(height in m)^2)
7. **DiabetesPedigreeFunction:** A function that scores the likelihood of diabetes based on family history
8. **Age:** Age in years
9. **Outcome (Target):** Class variable (0 if non-diabetic, 1 if diabetic)

## Model Architecture
The neural network is built sequentially using Keras:
* **Input Layer:** 8 nodes (matching the 8 features)
* **Hidden Layer 1:** 12 nodes with ReLU activation
* **Hidden Layer 2:** 8 nodes with ReLU activation
* **Normalization:** Batch Normalization layer to improve training stability
* **Output Layer:** 1 node with Sigmoid activation (for binary classification)

The model is optimized using the **Adam** optimizer and evaluates performance using **Binary Crossentropy** loss.

## How to Run
1. Clone this repository or open the script in Google Colab.
2. Download the `pima-indians-diabetes.csv` file.
3. Run the script. If using Colab, the code will prompt you to upload the dataset file directly.

## Saved Outputs
After training, the script automatically saves the trained model architecture and weights to disk:
* `model.json` (Neural network architecture)
* `model.weights.h5` (Trained model weights)
