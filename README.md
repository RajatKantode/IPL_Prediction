Here is a complete `README.md` file for your project based on the contents of the uploaded notebook **`IPL_score_prediction.ipynb`**:

---

# 🏏 IPL Score Prediction

This project builds a machine learning model to predict the **final score of a batting team** during an Indian Premier League (IPL) T20 match based on various match conditions such as the number of overs played, current runs, wickets fallen, and recent performance.

---

## 📌 Objective

To predict the **final inning score** in an IPL match using a regression-based machine learning model, given real-time match data up to a certain over.

---

## 📁 Project Structure

```
IPL_score_prediction/
├── IPL_score_prediction.ipynb
├── README.md
└── dataset.csv
```

---

## 📊 Features Used

* **Batting Team**
* **Bowling Team**
* **Overs** – Number of overs completed so far
* **Runs** – Current score
* **Wickets** – Wickets lost so far
* **Runs in last 5 overs**
* **Wickets in last 5 overs**

---

## 🧠 Model Pipeline

1. **Data Preprocessing**

   * Dropping irrelevant columns
   * Filtering teams for consistency
   * Encoding categorical features using `OneHotEncoder`
   * Train-test split

2. **Model Building**

   * Regression model using **Linear Regression** (or alternative)
   * Model trained on preprocessed data

3. **Prediction Example**

   * Inputs current match state (e.g., `overs=12.3`, `runs=113`, etc.)
   * Outputs predicted final score

---

## ✅ Model Performance

* Evaluated using `r2_score` and residual analysis.
* Performs reasonably well with standard features and IPL data.

---

## 🧪 Sample Usage

```python
predict_score(
    batting_team='Mumbai Indians',
    bowling_team='Kings XI Punjab',
    overs=12.3,
    runs=113,
    wickets=2,
    runs_last_5=55,
    wickets_last_5=0
)
# Output: Predicted Score: ~176
```

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* Seaborn, Matplotlib
* Jupyter Notebook

---

## ▶️ How to Run

1. Clone or download the repository.
2. Ensure required libraries are installed:

   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
   ```
3. Run the notebook:

   ```bash
   jupyter notebook IPL_score_prediction.ipynb
   ```
4. Follow the steps and use the `predict_score` function to make predictions.

---

## 🚀 Future Improvements

* Use more sophisticated models like XGBoost or LSTM for time-series prediction.
* Deploy as a web app using Streamlit for real-time predictions.
* Integrate live match data feeds.
