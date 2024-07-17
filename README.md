# Optimized Crop Selection Using Machine Learning for Soil Analysis

This project aims to assist farmers in selecting the best crop for their fields by identifying the most critical soil measure using machine learning techniques. Due to budget constraints, the farmer can only afford to measure one out of four essential soil measures. This repository contains the code to determine which soil measure (Nitrogen, Phosphorous, Potassium, or pH value) is the best predictor for crop selection.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The goal of this project is to apply machine learning to feature selection for optimizing crop prediction based on soil measures. The analysis focuses on determining which single soil metric is most predictive of the best crop yield.

## Dataset

The dataset used in this project is `soil_measures.csv`, which contains the following columns:
- `N`: Nitrogen content ratio in the soil
- `P`: Phosphorous content ratio in the soil
- `K`: Potassium content ratio in the soil
- `ph`: pH value of the soil
- `crop`: The type of crop

## Requirements

The required libraries for this project are:
- `pandas`
- `scikit-learn`

## Installation

To install the required libraries, run:
```bash
pip install pandas scikit-learn
```

## Usage

1. Clone the repository:
```bash
git clone https://github.com/atakoutene/Optimized-Crop-Selection-Using-Machine-Learning-for-Soil-Analysis.git
cd optimized-crop-selection
```

2. Ensure the dataset `soil_measures.csv` is in the project directory.

3. Run the script:
```bash
python optimize_crops_selection.py
```

## Code Explanation

- **Data Loading and Preprocessing**: Load the dataset and check for missing values.
- **Feature and Target Split**: Split the dataset into features (X) and target (y).
- **Train-Test Split**: Split the data into training and testing sets.
- **Model Training**: Train a logistic regression model for each soil measure.
- **Performance Evaluation**: Evaluate the model using the F1-score for each feature.
- **Best Feature Selection**: Identify and store the best predictive feature based on the highest F1-score.

## Results

The script trains a logistic regression model on each soil feature individually and calculates the F1-score to determine which feature is the best predictor for crop selection. The feature with the highest F1-score is considered the most important soil measure.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue for any bugs or feature requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
