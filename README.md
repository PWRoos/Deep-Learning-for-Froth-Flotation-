# Deep Learning for Iron Concentration Prediction in Froth Flotation: A Data-Driven Approach. 

This project applies deep learning techniques, including LSTM and Autoencoder models, to predict iron concentration in a froth flotation plant. The study aims to improve prediction accuracy by leveraging time-series data and advanced feature engineering, such as rolling statistics and lag features.

## Table of Contents
1. Project Overview
2. Features
3. Installation
4. Usage
5. Project Structure
6. Model Architectures
7. License

---

## 1. Project Overview

Flotation processes are widely used in the metallurgical industry for material separation. Predicting the purity of iron concentration is a challenging problem due to the complex, non-linear behavior of the system. This project expands on the work of Pu et al. (2020) by developing deep learning models to predict iron concentration using LSTM, Autoencoder, and LSTM Autoencoder architectures.

---

## 2. Features

- **LSTM Model**: Handles sequential time-series data for iron concentration prediction.
- **Autoencoder**: Reduces dimensionality and extracts key features.
- **LSTM Autoencoder**: Combines encoding and sequential learning for noise reduction and improved robustness.
- **Feature Engineering**: Includes lag features, rolling statistics, and mean, median, and standard deviation calculations.
- **Hyperparameter Optimization**: Uses `KerasTuner` to tune important model parameters.

---

## 3. Installation

**Prerequisites**:
- Python 3.12
- Anaconda/Miniconda (recommended)
- Git

To clone the repository and install the required packages:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/flotation-prediction.git
   cd flotation-prediction
   
2. Create and activate a cirtual environment:
   ```bash
   conda create --name flotation_env python=3.12
   conda activate flotation_env

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   
## 4. Usage
To run the models execute the src/main.ipynb script. This script trains and evaluated the LSTM, Autoencoder, and LSTM-Autoencoder models on the froth flotation dataset.

## 5. Project Structure

    /flotation-prediction
    │
    ├── /src                         # Source code and models
    │    ├── main.ipynb              # Main script to run models
    │    ├── flotation_dataset.csv   # Froth flotation dataset to be used
    │
    ├── /docs                        # Documentation for the project
    │    └── user_guide.md           # Detailed user guide
    │
    ├── README.md                    # Project overview and instructions
    ├── LICENSE.txt                  # License for your project
    ├── requirements.txt             # List of dependencies
    └── .gitignore                   # Ignore unnecessary files for Git

## 6. Model Architectures

1. LSTM Model:
- Architecture: Sequential model with two LSTM layers and a Dense layer for prediction.
- Optimizer: Adam
- Loss function: Huber Loss

2. Autoencoder Model:
- Architecture: Time-distributed Dense layers for encoding and decoding.
- Optimizer: Adam
- Loss function: Mean Squared Error (MSE)

3. LSTM Autoencoder
- Architecture: Encoder with LSTM layers and Decoder with LSTM layers.
- Optimizer: Adam
- Loss function: Mean Squared Error (MSE)

## 7. License

This project is licensed under the GNU General Public License v3.0. Please see LICENSE.txt for details.
