# AlphaQuant Pro 📊

AlphaQuant Pro is an advanced stock market analysis and forecasting platform built with Python and Streamlit. It provides users with tools to fetch, visualize, and analyze stock data, including technical indicators and performance comparisons. The application also offers various forecasting models to predict future stock prices.

## Features

*   **Comprehensive Data Fetching:** Retrieves historical stock data from Yahoo Finance for a wide range of global tickers.
*   **Technical Analysis:**
    *   Simple Moving Averages (SMA: 20-day, 50-day, 200-day)
    *   Relative Strength Index (RSI)
    *   Bollinger Bands
    *   Moving Average Convergence Divergence (MACD)
*   **Interactive Visualizations:**
    *   Candlestick charts for price analysis with moving averages and volume.
    *   Dedicated charts for RSI, Bollinger Bands, and MACD.
*   **Performance Comparison:** Compare the normalized performance of a selected stock against up to four other tickers.
*   **Data Export:**
    *   Download market data as a CSV file.
    *   Download charts as PNG images.
*   **Advanced Forecasting Models:**
    *   SARIMA (Seasonal Autoregressive Integrated Moving Average)
    *   Random Forest Regressor
    *   LSTM (Long Short-Term Memory) Neural Network
    *   Prophet (by Facebook)
*   **Customizable Analysis:**
    *   Select tickers from various sectors (Technology, Finance, Consumer, Healthcare, Energy & Industrials, Emerging Markets, Crypto & Blockchain, EV & Clean Energy, Commodities & ETFs).
    *   Define custom date ranges for analysis.
    *   Choose data intervals (daily, weekly, monthly).
*   **User-Friendly Interface:**
    *   Professional dark theme for comfortable viewing.
    *   Intuitive navigation between Market Analysis and Forecasting sections.
    *   Session state management for a smooth user experience.
    *   Clear data and rerun options.

## Technologies Used

*   **Python**
*   **Streamlit:** For the web application interface.
*   **yfinance:** To fetch stock market data.
*   **Pandas:** For data manipulation and analysis.
*   **NumPy:** For numerical operations.
*   **Plotly (plotly.graph_objects, plotly.express, plotly.subplots):** For creating interactive charts.
*   **Statsmodels:** For SARIMA forecasting, seasonal decomposition, and AD Fuller test.
*   **Scikit-learn:** For Random Forest Regressor and metrics (MSE, MAE, R2).
*   **Keras (TensorFlow backend):** For LSTM neural network model (Sequential, LSTM, Dense, Dropout).
*   **Prophet (by Facebook):** For time series forecasting.
*   **TA-Lib (Technical Analysis Library, via `ta`):** For calculating technical indicators (RSI, Bollinger Bands, MACD).
*   **Requests:** For making HTTP requests with retry logic.
*   **Datetime:** For handling dates and times.

## Setup and Installation

1.  **Clone the repository (if applicable):**
    ```bash
    git clone <your-repository-url>
    cd AlphaQuant_Pro
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    # On Windows
    venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    Make sure you have a `requirements.txt` file with all the necessary packages.
    ```
    streamlit
    yfinance
    pandas
    numpy
    plotly
    requests
    statsmodels
    scikit-learn
    tensorflow # or keras if using standalone Keras
    prophet
    ta
    ```
    Then run:
    ```bash
    pip install -r requirements.txt
    ```
    *Note: Installing `prophet` can sometimes be tricky. Refer to the official [Prophet installation guide](https://facebook.github.io/prophet/docs/installation.html) if you encounter issues.*
    *For `tensorflow` (Keras backend), ensure you have compatible versions and potentially CUDA/cuDNN for GPU support if desired.*

## Usage

1.  **Navigate to the project directory:**
    ```bash
    cd path/to/AlphaQuant_Pro
    ```

2.  **Run the Streamlit application:**
    ```bash
    streamlit run app.py
    ```

3.  Open your web browser and go to the local URL provided by Streamlit (usually `http://localhost:8501`).

4.  **Using the Application:**
    *   **Sidebar Navigation:**
        *   Choose between "Market Analysis" and "Forecasting" modes.
        *   Select a sector and then a specific ticker.
        *   Set the desired date range and data interval.
        *   For "Market Analysis", you can select up to 4 tickers for comparison.
        *   For "Forecasting", select a forecasting model and adjust its parameters (forecast period, SARIMA orders, LSTM settings).
    *   **Market Analysis Page:**
        *   Click "📊 Fetch Market Data" to load and display stock information.
        *   View key metrics (current price, 52-week range, daily return, average volume).
        *   Explore tabs for:
            *   **Price Analysis:** Interactive candlestick chart with SMAs and volume.
            *   **Technical Indicators:** Charts for RSI, Bollinger Bands, and MACD.
            *   **Performance Comparison:** Normalized performance chart against selected comparison tickers.
            *   **Data Table:** View raw and calculated data, with export options.
        *   Download data as CSV or charts as PNG.
    *   **Forecasting Page:**
        *   Click "🔮 Run Forecast" to generate predictions using the selected model.
        *   View a plot of actual vs. forecasted prices (with confidence intervals for Prophet).
        *   See a table of the forecasted data.
        *   Export forecast data as CSV or the forecast chart as PNG.
    *   **Clear Data:** Use the "🔄 Clear Data" button to reset the application state.

## Author

**Muhammad Atif Latif**

*   **GitHub:** [m-Atif-Latif](https://github.com/m-Atif-Latif)
*   **Kaggle:** [matiflatif](https://www.kaggle.com/matiflatif)
*   **LinkedIn:** [Muhammad Atif Latif](https://www.linkedin.com/in/muhammad-atif-latif-13a171318)
*   **Twitter/X:** [@mianatif5867](https://x.com/mianatif5867)
*   **Instagram:** [@its_atif_ai](https://www.instagram.com/its_atif_ai/)
*   **Email:** [muhammadatiflatif67@gmail.com](mailto:muhammadatiflatif67@gmail.com)

## License

This project is open-source. This is license under Apache 2.0. If not, you can state:
"This project is for educational and demonstration purposes. Please ensure you have the rights to use any data and libraries according to their respective licenses."

---

*Data provided by Yahoo Finance. Last updated dynamically by the application.*
