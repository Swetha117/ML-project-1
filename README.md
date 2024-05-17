# COVID-19 Data Processing and Prediction

This project processes COVID-19 dataset to prepare it for a machine learning model which predicts the number of deaths based on various features. The dataset is cleaned, preprocessed, and used to train a decision tree regressor model.

## Project Structure

- `train_data_covid.csv`: Training dataset containing COVID-19 data.
- `test_data_covid.csv`: Test dataset containing COVID-19 data.
- `submission.csv`: Output file with predicted deaths for the test dataset.
- `script.py`: Python script containing the data processing and model training code.

## Description

This script performs the following steps:
1. **Load the Data**: Reads the training and test datasets from CSV files.
2. **Preprocess Dates**: Converts date columns to datetime objects and extracts year, month, and day components.
3. **Encode Categorical Data**: Encodes the state names into numerical values using `LabelEncoder`.
4. **Normalize Population Density**: Normalizes the population density feature using `MinMaxScaler`.
5. **Drop Unnecessary Columns**: Removes columns that are not required for the model.
6. **Train Model**: Trains a `DecisionTreeRegressor` model on the training data.
7. **Make Predictions**: Uses the trained model to predict deaths on the test dataset.
8. **Generate Submission File**: Outputs the predictions to a CSV file.

## Installation

To run the script, you'll need Python and the following libraries:
- pandas
- scikit-learn

You can install these libraries using pip:

```bash
pip install pandas scikit-learn
