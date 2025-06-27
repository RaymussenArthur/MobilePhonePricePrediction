# Model Evaluation Summary

## 📄 Dataset
- Cleaned dataset: `Data/Clean/clean_cellphone.csv`
- Total records: XX (isi sesuai data kamu)
- Features: Sale, Resolution, PPI, CPU Core, CPU Freq, Internal Mem, RAM, Rear Cam, Front Cam, Battery
- Target: Price (Regression)

---

## Models Evaluation

| Model               | R² Score | RMSE    |
|:--------------------|:----------|:-----------|
| Random Forest        | 0.3825   | 476.80 |
| Gradient Boosting    | 0.4434   | 452.68 |
| XGBoost (Default)    | 0.6708   | 348.11 |
| **XGBoost (Tuned)**  | **0.7345** | **312.67** |

---

## Final Model
- **Model**: Tuned XGBoost Regressor
- **Parameter**:
  - n_estimators: 200
  - max_depth: 6
  - learning_rate: 0.05
  - subsample: 0.8
  - colsample_bytree: 0.8
  - random_state: 42
- Disimpan dalam: `Results/trained_model.pkl`

---

## Visualization Prediction

![XGBoost Prediction Result](Results/xgb_prediction_vs_actual.png)

---

## Conclusion
- Tuned XGBoost memberi performa terbaik.
- Fitur paling berpengaruh: RAM, Battery, CPU Core, Rear Cam.
- Model siap digunakan untuk prediksi harga handphone mid-tier berdasarkan spesifikasi.

