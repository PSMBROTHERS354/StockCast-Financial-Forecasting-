# StockCast — Financial Time Series Forecasting

**A full-stack stock price forecasting platform using deep learning and machine learning.**

**Maintainer:** Sundharamoorthi P

StockCast is a financial time-series forecasting project designed to explore stock market data, train forecasting models, and visualize predicted price trends through an interactive web dashboard.

The project combines a Python backend, a React frontend, and a machine-learning pipeline to demonstrate how historical financial data can be processed and used for time-series forecasting.

> **Disclaimer:** StockCast is an educational and experimental forecasting project. Model predictions are uncertain and should not be considered financial advice or investment recommendations.

## Project Objectives

- Explore historical stock market data and identify time-series patterns.
- Investigate LSTM and GRU architectures for sequential financial data.
- Explore the integration of XGBoost with deep-learning-based forecasting.
- Build an interactive frontend for displaying forecasts and comparing stocks.
- Develop an end-to-end application integrating machine learning, APIs, and a database.

## Technology Stack

| Component | Technologies |
|---|---|
| Programming language | Python |
| Deep learning | PyTorch, LSTM, GRU |
| Machine learning | XGBoost, scikit-learn |
| Backend | FastAPI |
| Frontend | React, Vite |
| Styling | Tailwind CSS |
| Data processing | pandas, NumPy |
| Visualization | Recharts |
| Database | PostgreSQL |
| Financial data | yfinance |

*The technologies listed above are based on the original project documentation. Actual dependencies and implemented features should be verified against the codebase.*

## Key Features

- Historical financial data processing.
- Time-series forecasting using machine-learning and deep-learning approaches.
- Interactive stock prediction visualizations.
- Stock comparison and forecast analysis.
- Frontend and backend integration.
- Database-backed application architecture.

Additional features, such as authentication, watchlists, CSV/Excel export, and long-horizon forecasting, should be documented as implemented only after testing the corresponding modules.

## Project Architecture

```text
StockCast/
├── backend/
├── config/
├── data/
├── frontend/
├── general_tests/
├── models/
├── tests/
├── training/
├── check_training_stocks.py
├── evaluate_test.py
├── price_downloads.py
├── start_backend.py
├── requirements.txt
├── db_migration.sql
└── README.md
```

The backend handles application logic and forecasting APIs, while the frontend provides the user interface. The data, training, and model directories support the machine-learning workflow.

*The exact responsibilities of individual modules should be confirmed from the implementation.*

## Getting Started

### Prerequisites

Install the following tools before running the project:

- Python 3.11 or a compatible version specified by the dependencies.
- Node.js and npm.
- PostgreSQL, if required by the configured backend.
- Visual Studio Code.

### 1. Clone the repository

After creating your GitHub repository, use its URL:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd StockCast
```

Alternatively, open the extracted project folder directly in VS Code.

### 2. Set up the Python environment

From the project root, open the VS Code terminal and run:

```bash
python -m venv .venv
```

Activate the environment on Windows:

```bash
.venv\Scripts\activate
```

Install the Python dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Configure environment variables and database

Check the backend configuration and any `.env.example` files.

Configure the required database connection and application secrets using the project's documented settings. Do not commit passwords, API keys, or other credentials to GitHub.

If PostgreSQL is required, ensure the database exists and apply the appropriate migrations before starting the backend.

### 4. Start the backend

Follow the startup instructions in the backend source code and project configuration. If the application uses Uvicorn and exposes `backend/main.py` as its FastAPI entry point, the command may resemble:

```bash
uvicorn backend.main:app --reload --port 8001
```

Use this command only after confirming the module path and configuration.

### 5. Start the frontend

Open a second terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed by Vite in your browser.

**Note:** Backend configuration, database setup, and the correct startup command must be verified against the downloaded source code.

## Model Evaluation

Financial forecasting models should be evaluated using chronological train, validation, and test splits to avoid look-ahead bias.

Relevant evaluation methods include:

- Mean Absolute Error (MAE).
- Root Mean Squared Error (RMSE).
- Directional accuracy.
- Comparison against a simple baseline forecast.

Evaluation results should be added here after running the model on a held-out test set.

## Future Improvements

- Validate model performance across different market conditions.
- Compare LSTM, GRU, and XGBoost against baseline models.
- Improve forecasting evaluation and reproducibility.
- Enhance error handling and API reliability.
- Deploy the frontend and backend for public demonstration.
- Document model limitations and forecasting uncertainty.

## Learning Outcomes

This project provides an opportunity to explore:

- Financial time-series analysis.
- Deep learning for sequential data.
- REST API development with FastAPI.
- Frontend development with React.
- Database integration.
- Model evaluation and software project deployment.

## Original Project Attribution

This project is adapted from the original StockCast/ML stock forecasting project by **Gokul Sivasubramaniam**.

Original repository: https://github.com/gokulsivas/ML_stock_forecasting

This repository is maintained by **Sundharamoorthi P** for learning, development, experimentation, and portfolio demonstration. Modifications and additional contributions will be documented as they are made.

Please refer to the original repository's license and preserve the required attribution.

## Author

**Sundharamoorthi P**

GitHub: https://github.com/PSMBROTHERS354

---

*StockCast is intended for educational and research purposes. Forecasts are estimates, not guarantees of future market performance.*
