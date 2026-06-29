# ANN Regression Project for Power Plant Energy Prediction

This project uses an Artificial Neural Network (ANN) to predict the net hourly electrical energy output of a power plant based on several operating features.

## Overview

The model is trained on the file [powerplant_data.csv](powerplant_data.csv) and uses features such as:

- Temperature (AT)
- Vacuum (V)
- Ambient Pressure (AP)
- Relative Humidity (RH)

The target variable is:

- Electrical Energy Output (PE)

## Project Files

- [PowerPlant_Energy_predictor.ipynb](PowerPlant_Energy_predictor.ipynb) — main notebook for data loading, preprocessing, model training, evaluation, and visualization.
- [ANN_Regression.ipynb](ANN_Regression.ipynb) — additional notebook for ANN regression work.
- [powerplant_data.csv](powerplant_data.csv) — dataset used for training and testing.
- [best_ANN_model.pt](best_ANN_model.pt) — saved weights of the best-performing model.

## Requirements

Install the following Python libraries before running the notebook:

```bash
pip install pandas numpy scikit-learn torch matplotlib
```

## Workflow

1. Load the dataset from [powerplant_data.csv](powerplant_data.csv).
2. Split the data into training and testing sets.
3. Standardize the input features.
4. Build and train an ANN regression model using PyTorch.
5. Evaluate the model using loss metrics and R-squared score.
6. Save the best model weights to [best_ANN_model.pt](best_ANN_model.pt).

## Model Architecture

The ANN model uses a simple feedforward network with:

- Input layer: 4 features
- Hidden layers: 6 neurons each
- Output layer: 1 neuron for regression prediction

## How to Run

Open [PowerPlant_Energy_predictor.ipynb](PowerPlant_Energy_predictor.ipynb) in Jupyter Notebook or VS Code and run the cells in order.

## Notes

- The notebook uses a train-test split and tracks both training and validation loss during training.
- The best model is saved automatically when the validation loss improves.
- You can modify the number of epochs, batch size, or network layers to experiment with performance.

## License

This project is for educational and learning purposes.
