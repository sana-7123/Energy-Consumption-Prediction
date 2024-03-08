# Energy-Consumption-Prediction
Certainly! Below is an enhanced explanation section that provides a more detailed overview of each step in the code.

```markdown
# Energy Consumption Prediction

This Python script predicts energy consumption load types using a Random Forest Classifier. The script encompasses several stages, including data preprocessing, feature scaling, label encoding, lagged feature creation, and model training, to facilitate accurate predictions.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Dependencies](#dependencies)
- [Explanation](#explanation)
- [License](#license)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/sana-7123/energy-consumption-prediction.git
   ```

2. Navigate to the project directory:

   ```
   cd energy-consumption-prediction
   ```

3. Install the required dependencies:

   ```
   pip install -r requirements.txt
   ```

## Usage

Run the main script to perform energy consumption load type prediction.

```
python energy_prediction.py
```

Make sure to customize the script with your dataset path if needed.

## Dataset

The script operates on a CSV dataset (`load_data.csv`) containing a wealth of information pertaining to energy consumption. The dataset comprises the following key columns:

- `Date_Time`: Timestamps indicating when the data was recorded.
- `Usage_kWh`: Energy consumption measured in kilowatt-hours.
- `Lagging_Current_Reactive_Power_kVarh`: Lagging reactive power consumption.
- `Leading_Current_Reactive_Power_kVarh`: Leading reactive power consumption.
- `CO2(tCO2)`: Carbon dioxide emissions measured in tons of CO2.
- `Load_Type`: The target variable representing the type of energy consumption load.

## Dependencies

- pandas
- scikit-learn

## Explanation

### 1. Loading the Dataset

The initial step involves loading the dataset using the pandas library. The `Date_Time` column is parsed to datetime format to facilitate temporal analysis.

### 2. Data Preprocessing

Data preprocessing is crucial for ensuring the quality of the dataset. In this stage, the numeric features (`Usage_kWh`, `Lagging_Current_Reactive_Power_kVarh`, `Leading_Current_Reactive_Power_kVarh`, `CO2(tCO2)`) are standardized using the StandardScaler from scikit-learn. This process involves centering and scaling the features to achieve zero mean and unit variance.

### 3. Label Encoding

Label encoding is applied to the `Load_Type` column using scikit-learn's LabelEncoder. This transformation converts categorical labels into numerical representations, facilitating the model training process.

### 4. Lagged Feature Creation

To incorporate temporal patterns, lagged features are created. The `Usage_kWh_Lag1` feature is introduced by shifting the `Usage_kWh` column by one time step. This accounts for the historical consumption patterns.

### 5. Model Training

The Random Forest Classifier is chosen as the predictive model. This ensemble learning algorithm is effective for classification tasks. The script uses scikit-learn's RandomForestClassifier, with 100 decision trees, to train on the preprocessed dataset.

### 6. Prediction and Evaluation

The dataset is split into training and testing sets using scikit-learn's `train_test_split`. The trained model is then employed to make predictions on the testing set. Evaluation metrics such as classification report and confusion matrix are computed to assess the model's performance.

