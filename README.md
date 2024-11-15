# Sales Forecasting Project

This repository contains Python code for building and analyzing a sales forecasting model using historical data. The project is designed to support both batch and real-time sales forecasting using the ARIMA model.

## Features
- **Data Preprocessing**: Handles missing values, removes duplicates, cleans outliers, and prepares the dataset for analysis.
- **Pattern Analysis**:
  - Identifies seasonal patterns, trends, and cyclical components.
  - Visualizes sales over time.
- **Forecasting with ARIMA**:
  - Supports batch processing for historical data.
  - Enables real-time forecasting with dynamic data updates.
- **Evaluation**: Uses Mean Absolute Error (MAE) to evaluate model performance.

## Requirements
The following Python libraries are used:
- `pandas`
- `numpy`
- `matplotlib`
- `sqlite3`
- `scikit-learn`
- `statsmodels`
- `pmdarima`

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project folder:
   ```bash
   cd sales_forecast
   ```

## Usage
1. **Generate Example Data**: Run the script to generate synthetic sales data and save it to a CSV file.
2. **Preprocess Data**: Clean and preprocess the data for analysis.
3. **Pattern Analysis**: Use the provided functions to visualize trends, seasonality, and other patterns in the data.
4. **Run Forecasting**:
   - Perform batch forecasting on historical data.
   - Append new sales data and run real-time forecasting.

## Key Functions
- `generate_sales_data(file_path)`: Generates synthetic sales data.
- `preprocess_data(data)`: Cleans and preprocesses the dataset.
- `pattern_analysis(data)`: Analyzes seasonal and cyclical patterns.
- `arima_real_time_forecasting(data, new_data=None)`: Builds and updates an ARIMA model for real-time forecasting.

## Example
To forecast sales using real-time data:
```python
new_sales_data = pd.DataFrame({"date": ["2023-01-01", "2023-01-02"], "sales": [450, 470]})
model, forecast = arima_real_time_forecasting(existing_data, new_sales_data)
```