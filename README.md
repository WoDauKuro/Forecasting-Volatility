# NVDA Volatility Forecasting Project

## Project Overview

This project implements a GARCH (Generalized Autoregressive Conditional Heteroskedasticity) model to forecast the volatility of NVIDIA Corporation (NVDA) stock. It includes data retrieval from the AlphaVantage API, data storage in a SQLite database, model training, model prediction and model deployment using FastAPI.

## Features

- Data retrieval from AlphaVantage API
- SQLite database for storing stock data
- GARCH model implementation for volatility forecasting
- FastAPI for model deployment
- Jupyter Notebook for data analysis and visualization

## Project Structure

- `config.py`: Configuration settings and environment variable management
- `data.py`: Classes for interacting with AlphaVantage API and SQLite database
- `model.py`: GARCH model implementation
- `main.py`: FastAPI web service implementation
- `NVDA Volatility Forecasting.ipynb`: Jupyter Notebook for data analysis and visualization

## Installation

1. Clone the repository:
   ```
   git clone  https://github.com/WoDauKuro/Forecasting-Volatility.git
   cd nvda-volatility-forecasting
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

3. Set up the `.env` file with the following variables:
   ```
   ALPHA_API_KEY=your_alphavantage_api_key
   DB_NAME=your_database_name.db
   MOD_DIR=path_to_model_directory
   ```

## Usage

### Running the FastAPI Server

1. Start the FastAPI server:
   ```
   uvicorn main:app --reload --workers 1 --host localhost --port 8008
   ```

2. Access the API documentation at `http://localhost:8008/docs`

### API Endpoints

- `/hello`: GET request to test the API
- `/fit`: POST request to fit the GARCH model
- `/predict`: POST request to get volatility predictions

### Jupyter Notebook

Open and run the `NVDA Volatility Forecasting.ipynb` notebook for data analysis, visualization, and example usage of the API endpoints.

## Model Details

The project uses a GARCH(1,1) model to forecast volatility. The model is trained on historical NVDA stock data and can be updated with new data as needed.

## Contributing

Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes.


## Contact

Wodakuro K.L - kurolegz7@gmail.com

Project Link: https://github.com/WoDauKuro/Forecasting-Volatility