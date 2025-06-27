# Mobile Phone Price Prediction 📊

A regression project to predict mid-tier smartphone prices based on their technical specifications using several machine learning algorithms, with a primary focus on XGBoost.

---

## Exploratory Data Analysis (EDA)

Key insights:
- Distribution analysis of features such as **RAM**, **Battery**, **CPU Core**, and **Rear Camera**.
- Correlation heatmap to visualize relationships between numerical features.
- Features like **Weight** and **Thickness** were dropped due to low impact on pricing based on EDA results.

---

## Model Development & Evaluation

Machine learning models tested:
- **Random Forest Regressor**
- **Gradient Boosting Regressor**
- **XGBoost Regressor (default and tuned)**

### 📈 Performance Summary

| Model               | R² Score | RMSE    |
|:--------------------|:----------|:-----------|
| Random Forest        | 0.3825   | 476.80 |
| Gradient Boosting    | 0.4434   | 452.68 |
| XGBoost (Default)    | 0.6708   | 348.11 |
| **XGBoost (Tuned)**  | **0.7345** | **312.67** |

The **tuned XGBoost model** achieved the best performance.

---

## Conclusion
- The tuned XGBoost model delivered the best performance.
- The most influential features were: RAM, Battery, CPU Core, and Rear Camera.
- The model is ready to be used for predicting mid-tier smartphone prices based on technical specifications.

---

## How to Run
1. **Clone this repository**
   ```bash
      git clone https://github.com/RaymussenArthur/MobilePhonePricePrediction.git
      cd MobilePhonePricePrediction
   ```
2. **Install dependencies**
   ```bash
     pip install -r requirements.txt
   ```
3. **Run the EDA notebook**
Navigate to the Notebooks/ folder and open EDA.ipynb to explore the data and feature insights.

4. **Run the Modeling notebook**
In the same Notebooks/ folder, open and run Modeling.ipynb to train, evaluate, and tune the models.

5. **Use the trained model**
The final trained model is saved as a `.pkl` file and can be loaded using:
   ```python
    import joblib
    model = joblib.load('Results/trained_model.pkl')
    prediction = model.predict(new_data)
   ```
