# Gender Prediction with Random Forest

## Overview

This repository contains a simple machine learning project that uses a **Random Forest Classifier** to predict gender based on two input features: Body Mass Index (**BMI**) and walking time per kilometer (**walking_per_km**). The project is implemented in a Jupyter Notebook (`gender_predict_rfc.ipynb`).

## Features

-   **Data Generation**: Creates a small, synthetic dataset for demonstration purposes.
-   **Data Preprocessing**: Uses `LabelEncoder` from scikit-learn to convert categorical gender labels into numerical values.
-   **Model Training**: Trains a `RandomForestClassifier` on the prepared data.
-   **Prediction Function**: Includes a custom Python function (`get_pred`) to use the trained model for making new predictions.
-   **Input Validation**: The prediction function uses `assert` statements to ensure that the input `bmi` and `walk` are of the correct data type.

## How to Run the Notebook

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/gyanbdrmagar/gender_prediction_using_bmi_walking_distance.git](https://github.com/gyanbdrmagar/gender_prediction_using_bmi_walking_distance.git)
    ```

2.  **Navigate to the project directory**:
    ```bash
    cd gender_prediction_using_bmi_walking_distance
    ```

3.  **Install the required libraries**:
    ```bash
    pip install pandas scikit-learn
    ```

4.  **Open the Jupyter Notebook**:
    ```bash
    jupyter notebook gender_predict_rfc.ipynb
    ```

## Code Flowchart
graph TD
A[Start] --> B(Load Libraries);

B --> C(Create Synthetic DataFrame);

C --> D{Encode 'gender' column with LabelEncoder};

D --> E(Define Features X and Target Y);

E --> F{Split Data into Training and Test Sets};

F --> G(Initialize RandomForestClassifier Model);

G --> H(Fit Model to Training Data);

H --> I(Evaluate Model Accuracy on Test Data);

I --> J{Define get_pred Function};

J --> K{Call get_pred with New Data};

K --> L(Get Prediction Output);

L --> M[End];
