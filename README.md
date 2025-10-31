# Uber Traffic Analysis and Prediction
This project aims to analyze and predict Uber traffic volume at different junctions in a city. It utilizes historical traffic data, integrates external data sources like weather and events, and employs machine learning models for prediction.

### Project Structure
The project is organized into the following steps: 
* **Environment Setup:** Installs necessary libraries (meteostat).
* **Data Cleaning & Preprocessing:** Loads and cleans the initial traffic data, handling missing values and duplicates, and aggregates data hourly.
* **Feature Engineering & Selection:** Creates new features from the timestamp data (hour, day of week, month, weekend) and adds lagged traffic volume features. Feature importance is analyzed using a Random Forest model. 
* **Data Collection & Integration:** Fetches external weather data (OpenWeatherMap API - requires API key) and loads event data (from events.csv, with dummy data created if not present). These external data sources are merged with the traffic data. 
* **Model Development & Training:** Trains and evaluates different time series forecasting models, including Gradient Boosting Regressor, ARIMA, and LSTM. Time-based cross-validation is used for robust evaluation. 
* **Evaluation and Interpretation:** Evaluates the performance of the trained models using metrics like MAE, RMSE, and R2. Residual analysis is performed.

### Data Sources
* **Dataset_Uber Traffic.csv:** The primary dataset containing historical Uber traffic data (DateTime, Junction, Vehicles, ID).
* **OpenWeatherMap API:** Used to fetch real-time weather data. Requires an API key.
* **events.csv:** (Optional) A CSV file containing information about events that might impact traffic. If not provided, dummy data is generated.
