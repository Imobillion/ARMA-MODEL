This project demonstrates time series modeling and forecasting using the Autoregressive (AR), Moving Average (MA), and Autoregressive Moving Average (ARMA) models.

The dataset represents event counts collected over time (daily frequency). The goal is to:

Analyze long-term patterns and seasonality.

Fit and evaluate AR, MA, and ARMA models.

Compare model performance using statistical error metrics.

Save the trained models for future forecasting.

📂 Dataset

Name: Event Time Series Dataset

Source: Collected from logs of events (e.g., system events, locale activity, etc.)

Structure:

Column	Description
date	Timestamp of the event (daily granularity).
locale_name	Event category or locale identifier.
count	Number of events recorded on that date.

Frequency: Daily (missing values filled with zeros).

Total Size: ~7,000+ records (depending on aggregation).

🧮 Methodology

Data Preparation

Converted date column to datetime.

Aggregated data by day and filled missing values.

Train-test split (80% train, 20% test).

Exploratory Analysis

Time series decomposition into Trend, Seasonality, Residual.

Visualization of event frequency across time and locales.

Modeling

AR(p): Autoregressive model depending on past values.

MA(q): Moving Average model depending on past error terms.

ARMA(p,q): Combined model capturing both dependencies.

Evaluation Metrics

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Model Saving

Trained models saved using joblib for reuse.

📈 Results & Insights

AR model: Captured autocorrelation structure of the data.

MA model: Modeled short-term randomness and shocks.

ARMA model: Balanced both memory (AR) and shocks (MA), leading to better forecasts in most cases.

Key Insight:

If AR performed better → events are driven by past values.

If MA performed better → events are driven by past shocks/noise.

ARMA typically provided the best trade-off between the two.

💻 Installation & Usage
Requirements

Python 3.9+

pandas

numpy

matplotlib

statsmodels

scikit-learn

joblib


Author

Imo Bassey

Data Science & Machine Learning Enthusiast

Passionate about time series analysis and forecasting applications.
