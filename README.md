# Power System Load Type Prediction

This repository contains the code and resources for predicting the "Load_Type" of a power system based on historical data. The "Load_Type" categorization includes "Light_Load", "Medium_Load", and "Maximum_Load". The project aims to develop a machine learning model capable of accurately predicting these load types.

## Table of Contents

- [Introduction](#introduction)
- [Data Description](#data-description)
- [Installation](#installation)
- [Usage](#usage)
- [Validation and Testing](#validation-and-testing)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The primary objective of this project is to develop a machine learning model capable of predicting the "Load_Type" of a power system based on historical data. This classification problem requires candidates to apply their skills in data preprocessing, exploratory data analysis (EDA), feature engineering, model selection, and model evaluation to predict the load type accurately.

## Data Description

The dataset provided for this task contains several features that are crucial for understanding and predicting the load type of a power system. These features include:

- **Date**: Continuous-time data taken on the first of the month.
- **Usage_kWh**: Industry Energy Consumption in continuous kWh.
- **Lagging Current**: Reactive power in continuous kVarh.
- **Leading Current**: Reactive power in continuous kVarh.
- **CO2**: Continuous ppm.
- **NSM**: Number of Seconds from midnight in continuous seconds.
- **Load Type**: Categorical (Light Load, Medium Load, Maximum Load).

## Installation

To run the code in this repository, you need Python 3.6 or higher and the following libraries:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

You can install these libraries using pip:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/power-system-load-type-prediction.git
```

2. Navigate to the project directory:

```bash
cd power-system-load-type-prediction
```

3. Run the main script:

```bash
python main.py
```

This script will preprocess the data, perform EDA, engineer features, train the model, and evaluate its performance.

## Validation and Testing

An appropriate validation strategy is implemented, using the last month of data as the test set to assess the model's performance. This approach evaluates the model's ability to generalize well to recent, unseen data. Metrics specific to classification problems, such as accuracy, precision, recall, and F1-score, are used for evaluation.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you find any bugs or have suggestions for improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
