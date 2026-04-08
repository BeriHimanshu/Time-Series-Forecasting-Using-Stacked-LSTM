#  Microsoft Stock Price Forecasting using Stacked LSTM

##  Project Overview

This project focuses on forecasting **Microsoft (MSFT) stock closing prices** using a **Stacked Long Short-Term Memory (LSTM)** deep learning model.

Historical stock data is collected using the `yfinance` API, preprocessed, and used to train a multi-layer LSTM model to capture temporal dependencies and predict future stock prices.

---

## Dataset

* Source: Yahoo Finance (via `yfinance`)
* Stock: Microsoft (MSFT)
* Time Period: Last 15 years
* Feature Used: Closing Price

---

## Workflow

### 1. Data Collection

* Extracted stock data using `yfinance`
* Saved dataset as CSV for further use

### 2. Data Preprocessing

* Selected **Close price**
* Applied **MinMaxScaler** for normalization
* Split dataset:

  * Training: 65%
  * Testing: 35%

### 3. Sequence Creation

* Created time-series sequences using a sliding window
* Time step: **100 days**

### 4. Model Architecture

* Stacked LSTM model with 3 layers:

  * LSTM (50 units, return_sequences=True)
  * LSTM (50 units, return_sequences=True)
  * LSTM (50 units)
* Dense output layer
* Loss: Mean Squared Error
* Optimizer: Adam

### 5. Model Training

* Epochs: 100
* Batch size: 64

### 6. Evaluation

* Performance metric: **Root Mean Squared Error (RMSE)**
* Predictions compared with actual values

### 7. Forecasting

* Predicted future stock prices for the next **30 days**

---

## Tech Stack

* Python 
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* TensorFlow / Keras
* yfinance

---

## Results

* Model successfully captures stock price trends
* Reasonable prediction accuracy on test data
* Visualization shows alignment between predicted and actual values
* Future forecasting demonstrates model capability for time-series prediction

---

## Project Structure

```
├── finance_Project.ipynb   # Main notebook
├── README.md
├── PPT 
```

---

## How to Run

1. Clone the repository:

```
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. Install dependencies:

```
pip install numpy pandas matplotlib scikit-learn tensorflow yfinance
```

3. Run the notebook:

```
jupyter notebook finance_Project.ipynb
```

---

## Future Improvements

* Hyperparameter tuning for better accuracy
* Use of GRU / Transformer models
* Add multiple features (Open, High, Volume)
* Deploy model using Flask/Streamlit
* Real-time stock prediction

---

## Contribution

Contributions are welcome! Feel free to fork and improve the project.

---

## Contact Information 

Himanshu Beri
Himanshuberi1606@gmail.com
GitHub: https://github.com/BeriHimanshu
Linkedin: www.linkedin.com/in/himanshu-beri

---

