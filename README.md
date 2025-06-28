# Modeling COVID-19 Spread: A Comparative Study of Forecasting Techniques

# Project Overview

This project explores and compares various data science and time series forecasting techniques to analyze and predict the spread of infectious diseases, using real-world COVID-19 confirmed cases data as a case study. The goal is to demonstrate a comprehensive data science workflow, from data acquisition and exploratory analysis to implementing and evaluating different modeling approaches.

# Project Goals

*   Load, clean, and prepare a real-world time-series dataset of infectious disease spread.
*   Perform exploratory data analysis (EDA) to understand trends and patterns.
*   Engineer relevant features for time-series forecasting.
*   Implement and compare the performance of multiple modeling techniques.
*   Visualize actual vs. predicted values to assess model performance.
*   Attempt regional forecasting and understand associated data challenges.
*   Interpret model results, discuss strengths, weaknesses, and insights.

# Data

The project utilizes publicly available time-series data for COVID-19 confirmed cases. The dataset includes daily counts of confirmed cases globally, broken down by country and province/state.


# Methodology

The project followed a structured data science workflow:

1.  **Data Acquisition and Preparation**: Loading data from a public source and initial cleaning.
2.  **Exploratory Data Analysis (EDA)**: Visualizing global cumulative and daily new cases.
3.  **Feature Engineering**: Creating features such as rolling averages, lag values, and time-based indicators (day of week, month, etc.).
4.  **Model Implementation and Comparison**: Implemented and evaluated the following forecasting models:
    *   **Linear Regression**: Served as a baseline model with engineered features.
    *   **Prophet**: A time series model designed to handle seasonality and trends.
    *   **Long Short-Term Memory (LSTM)**: A type of recurrent neural network suitable for sequential data.
    *   **LightGBM**: A gradient boosting machine learning model applied with engineered features.
5.  **Regional Forecasting**: Attempted to apply modeling to a specific region (United States) to explore regional prediction challenges.
6.  **Interpretation and Analysis**: Compared model performance based on metrics (MSE, RMSE, R-squared) and visualizations, discussing the strengths and weaknesses of each approach. Insights from regional forecasting data anomalies were also analyzed.

# Key Findings

*   Different modeling approaches captured the patterns in COVID-19 spread with varying effectiveness.
*   The LSTM model generally showed improved quantitative performance on global data compared to Linear Regression and LightGBM.
*   Prophet was effective at capturing visual trends and seasonality.
*   Implementing regional forecasting highlighted the importance of understanding data characteristics and limitations in specific geographical subsets.

# Repository Structure


*   `README.md`: This file.
*   `Comparative-Study-of-Forecasting-Models-for-Infectious-Disease-Spread.ipynb`: The Jupyter Notebook containing all the code and analysis steps.

# How to Run the Code

1.  Clone this repository:
    ```bash
    git clone https://github.com/AnirbanRoy-cloud/Comparative-Study-of-Forecasting-Models-for-Infectious-Disease-Spread
    ```
2.  Navigate to the project directory.
3.  (Recommended) Create a virtual environment:
    ```bash
    python -m venv venv
    ```
4.  Activate the virtual environment:
    *   On Windows:
        ```bash
        .\venv\Scripts\activate
        ```
    *   On macOS/Linux:
        ```bash
        source venv/bin/activate
        ```
5.  Install the required libraries:
    ```bash
    pip install pandas matplotlib seaborn scikit-learn prophet tensorflow keras lightgbm
    # If you encountered specific issues with numpy/pmdarima, you might note that here
    # or provide a requirements.txt
    ```
6.  Open the Jupyter Notebook (`Comparative-Study-of-Forecasting-Models-for-Infectious-Disease-Spread.ipynb`) in your preferred environment (e.g., JupyterLab, VS Code, Google Colab).
7.  Run the cells sequentially to execute the analysis and models.

# Potential Future Work

*   Hyperparameter tuning and more rigorous cross-validation for all models.
*   Incorporating external data (e.g., mobility, vaccination rates, policy changes).
*   Exploring spatial-temporal modeling techniques.
*   Developing more robust strategies for regional forecasting across diverse areas.
*   Building a system for near real-time forecasting.

# License

MIT
