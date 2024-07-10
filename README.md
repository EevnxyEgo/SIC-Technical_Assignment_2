# Tool Wear Prediction

This project aims to develop a machine learning model to predict tool wear failures in a milling machine based on sensor data. Early prediction of tool wear can significantly reduce production downtime and maintenance costs.

## Dataset

The dataset used is the AI4I 2020 Predictive Maintenance Dataset, available from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset).

### Dataset Details

- **UID**: Unique identifier for each record.
- **Product ID**: Categorical identifier for the product.
- **Type**: Categorical feature indicating the type of machine.
- **Air temperature [K]**: Continuous feature representing the air temperature in Kelvin.
- **Process temperature [K]**: Continuous feature representing the process temperature in Kelvin.
- **Rotational speed [rpm]**: Integer feature representing the rotational speed in RPM.
- **Torque [Nm]**: Continuous feature representing the torque in Nm.
- **Tool wear [min]**: Integer feature representing the tool wear in minutes.
- **Machine failure**: Target variable indicating if the machine failed.
- **TWF, HDF, PWF, OSF, RNF**: Target variables indicating different failure modes.

## Project Steps

1. **Loading and Preprocessing the Dataset**
   - Load the dataset and handle missing values.
   - Encode categorical features.
   - Scale numerical features.
   - Bin the `Tool wear [min]` into categories for classification.

2. **Splitting the Dataset**
   - Split the data into training and testing sets.

3. **Handling Class Imbalance**
   - Apply SMOTE (Synthetic Minority Over-sampling Technique) to balance the classes.

4. **Training the Model**
   - Train a Random Forest classifier on the resampled dataset.

5. **Evaluating the Model**
   - Evaluate the model using a classification report and confusion matrix.

## How to Run the Code

### Prerequisites

- Python 3.10
- Required Python packages:
  - pandas
  - scikit-learn
  - imbalanced-learn
  - matplotlib
  - seaborn

### Installation

Install the required packages using pip:

```bash
pip install pandas scikit-learn imbalanced-learn matplotlib seaborn
```

### Results
After applying SMOTE and training a Random Forest classifier, the model achieved improved precision, recall, and F1-scores, especially for the minority class. The confusion matrix provided a clear view of the model's performance in correctly predicting each class.
