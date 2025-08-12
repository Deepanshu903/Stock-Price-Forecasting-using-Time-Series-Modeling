# Stock Price Prediction using Time-Series Modeling

A deep learning project that uses Long Short-Term Memory (LSTM) neural networks to predict Microsoft stock prices. This project implements a sequential LSTM model using TensorFlow/Keras to forecast stock closing prices based on historical data.

## Features

- **Data Preprocessing**: Comprehensive data cleaning and preprocessing pipeline
- **Exploratory Data Analysis**: Visualizations for price trends, volume analysis, and feature correlations
- **LSTM Model**: Multi-layer LSTM architecture for time series prediction
- **Model Evaluation**: Performance metrics including RMSE and MAE
- **Visualization**: Interactive plots comparing actual vs predicted stock prices


## Requirements

### Dependencies
```
tensorflow>=2.8.0
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.5.0
seaborn>=0.11.0
```

### Python Version
- Python 3.7 or higher

## Installation

1. Clone this repository:
```bash
git clone https://github.com/your-username/microsoft-stock-prediction.git
cd microsoft-stock-prediction
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Data Requirements

The project expects a CSV file named `MicrosoftStock.csv` with the following columns:
- `date`: Date in YYYY-MM-DD format
- `open`: Opening price
- `close`: Closing price
- `volume`: Trading volume

### Sample Data Format:
```csv
date,open,close,volume
2010-01-01,100.50,101.25,1000000
2010-01-02,101.25,102.00,1100000
```

## Usage

1. Ensure your Microsoft stock data CSV file is in the project directory
2. Run the main script:
```bash
python stock_prediction.py
```

The script will load data, train the LSTM model, generate predictions, and display evaluation metrics with comparison plots.


## Visualizations

The project generates several visualizations:

1. **Price Trends**: Open and close prices over time
2. **Volume Analysis**: Trading volume patterns
3. **Correlation Heatmap**: Feature correlation matrix
4. **Prediction Comparison**: Actual vs predicted prices

## Model Architecture

The LSTM model consists of:
1. **First LSTM Layer**: 64 units with return_sequences=True
2. **Second LSTM Layer**: 64 units with return_sequences=False
3. **Dense Layer**: 128 units with ReLU activation
4. **Dropout Layer**: 50% dropout rate for regularization
5. **Output Layer**: Single unit for price prediction

### Model Configuration:
- **Optimizer**: Adam
- **Loss Function**: Mean Absolute Error (MAE)
- **Training Split**: 95% training, 5% testing
- **Sequence Length**: 60 days sliding window

## Model Performance

The model performance is evaluated using:
- **RMSE (Root Mean Squared Error)**: Measures prediction accuracy
- **MAE (Mean Absolute Error)**: Average absolute difference between predicted and actual prices

## Configuration

You can modify the following parameters in the script:

- **Sequence Length**: Change the sliding window size (default: 60 days)
- **Training Split**: Adjust the train/test split ratio (default: 95/5)
- **Model Architecture**: Modify LSTM layers, units, or add more layers
- **Training Parameters**: Epochs, batch size, optimizer settings

## Project Structure

```
microsoft-stock-prediction/
â”œâ”€â”€ stock_prediction.py          # Main script
â”œâ”€â”€ MicrosoftStock.csv           # Stock data
â”œâ”€â”€ README.md                    # Documentation
â””â”€â”€ requirements.txt             # Dependencies

```

## Notes

- The model uses standardized data for better training performance
- Predictions are inverse-transformed to original scale for interpretation
- The date filter in the code (2013-2018) can be adjusted based on your data range](https://www.perplexity.ai/search/a503de4a-0345-4cac-bd51-f9d1a41200a7?0=c)](https://www.perplexity.ai/search/a503de4a-0345-4cac-bd51-f9d1a41200a7?0=c)
