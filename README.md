# Customer Segmentation and Sales Forecasting for Bank Transactions

 ## 📊 Project Overview

This project provides an in-depth analysis of a bank transaction dataset to uncover customer behavior patterns and predict future trends. The primary goals are to segment customers based on their transaction history using RFM analysis and K-Means clustering, predict customer churn with a logistic regression model, and forecast future sales using an ARIMA time-series model.

This end-to-end data science project demonstrates key skills in data cleaning, exploratory data analysis, machine learning, and time-series forecasting.

---

## ✨ Key Features

-   **Data Cleaning & Preprocessing:**
    -   Handles missing values and removes invalid data entries (e.g., transactions with zero or negative amounts).
    -   Derives customer `Age` from their date of birth and filters for a realistic age range (18-100).
    -   Converts date columns to the correct `datetime` format for time-based analysis.

-   **RFM (Recency, Frequency, Monetary) Analysis:**
    -   Calculates **Recency**, **Frequency**, and **Monetary** values for each customer.
    -   Addresses data skewness by applying a log transformation to RFM metrics, preparing them for clustering.
    -   Visualizes the distribution of RFM values before and after transformation.


    -   **Score-Based Segmentation:** Divides customers into meaningful segments like `Best Customers`, `Loyal Customers`, `At Risk`, and `Churned Customers` using RFM scores.
    -   **K-Means Clustering:** Determines the optimal number of clusters using the Elbow Method and groups customers based on their standardized RFM values.

 
    -   Engineers a `Churn` feature based on customer recency (customers with recency > 90 days are flagged as churned).
    -   Trains a **Logistic Regression** model to predict the likelihood of a customer churning. The model achieved an accuracy of **100%** on the test set due to the direct relationship between recency and the churn definition.

-   **Sales Forecasting:**
    -   Aggregates transaction data into a monthly time series.
    -   Trains an **ARIMA (AutoRegressive Integrated Moving Average)** model to forecast total transaction amounts for the next 6 months.



## 🛠️ Technologies Used

-   **Python 3.x**
-   **Pandas:** For data manipulation and analysis.
-   **NumPy:** For numerical operations.
-   **Scikit-learn:** For machine learning (K-Means, Logistic Regression, StandardScaler).
-   **Statsmodels:** For time-series analysis (ARIMA model).
-   **Matplotlib & Seaborn:** For data visualization.
-   **Jupyter Notebook:** As the development environment.

---

## 🚀 How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Create a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You will need to create a `requirements.txt` file by running `pip freeze > requirements.txt` in your local environment.)*

4.  **Download the dataset:**
    -   Place the `bank_transactions.csv` file in the root directory of the project.

5.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook datawarehouse.ipynb
    ```

---

## 📁 File Structure
