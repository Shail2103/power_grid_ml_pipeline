# Smart Power Grid Load Forecasting & Anomaly Detection Pipeline

An end-to-end Machine Learning and Time-Series pipeline designed to forecast dynamic power grid electricity consumption (MW) and automatically isolate system anomalies, faults, or severe structural disruptions.

## Architecture & Features
- **Temporal Transformations:** Encodes time cyclical variations using trigonometric sine/cosine components.
- **Historical Lags:** Implements autoregressive lag metrics ($t-1$, $t-2$, $t-24$, $t-168$) to track historical grid momentum.
- **Forecasting Module:** Deploys an optimized **XGBoost Regressor** to predict system loads.
- **Anomaly Layer:** Pairs **Isolation Forests** with model forecasting residuals ($|Actual - Predicted|$) to catch network outliers.

## Getting Started

### Prerequisites
Ensure you have Python 3.9+ installed.

### Installation & Execution
1. Clone or download the repository files.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
