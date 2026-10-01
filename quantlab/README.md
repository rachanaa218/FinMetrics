# FinMetrics — Quantitative Financial Analytics Platform

![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Backend](https://img.shields.io/badge/Backend-FastAPI-009688.svg)
![Frontend](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61DAFB.svg)
![Language](https://img.shields.io/badge/Language-TypeScript%20%7C%20Python-blue.svg)

**FinMetrics** is a full-stack financial analytics platform for exploring market data, analyzing portfolio performance, evaluating investment risk, and testing quantitative trading strategies.

The project combines a React frontend with a FastAPI backend and a quantitative analysis engine to process financial time-series data and generate interactive analytics.

---

## Features

### 📊 Market Analysis

* Interactive financial charts
* Historical market data analysis
* Technical indicators including:

  * SMA
  * EMA
  * RSI
  * MACD
  * Bollinger Bands
  * ATR
* Support for multiple asset classes

### 💼 Portfolio Analysis

* Portfolio performance tracking
* Asset allocation analysis
* Return calculations
* Benchmark comparison
* Equity curve visualization

### ⚠️ Risk Analysis

* Volatility measurement
* Sharpe Ratio
* Maximum Drawdown
* Value at Risk (VaR)
* Portfolio correlation analysis
* Risk and performance comparison

### 🔬 Strategy Backtesting

* Historical strategy testing
* Configurable strategy parameters
* Equity curve generation
* Trade statistics
* Strategy performance evaluation

### 📈 Quantitative Analytics

* Return calculations
* Moving averages
* Correlation analysis
* Drawdown analysis
* Performance metrics
* Time-series data processing

### 🗄️ Data Processing

* Financial data ingestion
* Data cleaning and validation
* Normalization
* Database storage
* Automated data preparation scripts

---

## Tech Stack

### Frontend

* React
* TypeScript
* Vite
* Recharts
* Lucide Icons

### Backend

* Python
* FastAPI
* Pandas
* NumPy
* SciPy
* SQLAlchemy

### Database

* SQLite

### Data

* Historical financial market data
* Yahoo Finance data through `yfinance`

### Development

* Git & GitHub
* Docker
* REST APIs

---

## Architecture

```text
                    FinMetrics
                        │
                        ▼
              ┌──────────────────┐
              │  React Frontend  │
              │   TypeScript     │
              └────────┬─────────┘
                       │
                    REST API
                       │
                       ▼
              ┌──────────────────┐
              │  FastAPI Backend │
              └────────┬─────────┘
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
     Data Processing  Quant Engine  Database
          │            │            │
          └────────────┼────────────┘
                       ▼
              Financial Analytics
                       │
                       ▼
             Interactive Dashboard
```

---

## Project Structure

```text
quantlab/
├── frontend/          # React + TypeScript frontend
├── backend/           # FastAPI backend and quantitative engine
├── datasets/          # Financial datasets
├── scripts/           # Data ingestion and processing scripts
├── docs/              # Project documentation
├── docker-compose.yml
├── LICENSE
└── README.md
```

> The root folder is currently named `quantlab` for compatibility with the existing project structure. The application branding is **FinMetrics**.

---

## Getting Started

### Prerequisites

Make sure you have:

* Python 3.10+
* Node.js 18+
* npm
* Git

Docker is optional.

### 1. Clone the Repository

```bash
git clone https://github.com/rachanaa218/FinMetrics.git
cd FinMetrics/quantlab
```

### 2. Backend Setup

```bash
cd backend
python -m venv venv
```

#### Windows

```bash
.\venv\Scripts\activate
```

#### Linux/macOS

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the backend:

```bash
python -m uvicorn app.main:app --reload --port 8000
```

Backend API:

```text
http://localhost:8000
```

Swagger API documentation:

```text
http://localhost:8000/docs
```

### 3. Frontend Setup

Open another terminal:

```bash
cd quantlab/frontend
npm install
npm run dev
```

The frontend will normally be available at:

```text
http://localhost:5173
```

---

## Data Processing

The project includes scripts for preparing financial market data:

```bash
cd quantlab/scripts

python download_data.py
python clean_data.py
python normalize_data.py
python seed_database.py
```

---

## Current Assets

The project currently works with financial market data including:

* Gold
* Bitcoin
* NVIDIA

Additional assets can be integrated through the data layer.

---

## Project Goals

FinMetrics is being developed as a personal full-stack project to explore:

* Financial data engineering
* Quantitative analysis
* Portfolio analytics
* Risk measurement
* Algorithmic strategy evaluation
* REST API development
* Full-stack application architecture

---

## Future Improvements

Planned improvements include:

* [ ] Portfolio creation and management
* [ ] Paper trading simulation
* [ ] Watchlists
* [ ] Real-time market data integration
* [ ] Advanced portfolio optimization
* [ ] Strategy comparison
* [ ] Improved backtesting engine
* [ ] User authentication
* [ ] PostgreSQL support
* [ ] Cloud deployment
* [ ] Automated financial reports

---

## Disclaimer

FinMetrics is an educational and software-development project. The analytics and simulations provided by the application are for research and learning purposes and should not be considered financial advice.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
