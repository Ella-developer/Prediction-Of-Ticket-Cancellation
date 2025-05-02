# 🎫 Ticket Cancellation Prediction (98% Accuracy) with XGBoost

This project focuses on predicting whether a ticket (e.g., for travel or events) will be canceled or not, using a carefully engineered dataset and a finely tuned **XGBoost classifier**, achieving up to **98% accuracy**.

## 📌 Project Highlights

- ✅ Achieved 98% accuracy using XGBoost (with tuned hyperparameters)
- ⚙️ Designed as an end-to-end pipeline
- 📈 Includes full preprocessing, training, evaluation, and model export
- 🧠 Feature importance and interpretability via SHAP (optional extension)
- 🗃️ Exported model (`xgb_ticket.json`) available for deployment
- 🔍 Ideal for integration with APIs for real-time prediction

---

## 🧠 Model Details

- **Model type**: XGBoost Classifier
- **Objective**: `binary:logistic`
- **Features**: 14 selected features (e.g., ticket age, route distance, time to departure)
- **Hyperparameters**:
  - `max_depth=5`
  - `n_estimators=150`
  - `colsample_bytree=0.5`
  - `learning_rate=0.1`
  - `objective="binary:logistic"`
- **Classes**: 0 (Not Canceled), 1 (Canceled)

---

## 📁 Files

| File | Description |
|------|-------------|
| `prediction-of-ticket-cancellation-acc-98.ipynb` | Jupyter notebook with preprocessing, training, evaluation |
| `xgb_ticket.json` | Exported XGBoost model in JSON format |
| `README.md` | Project documentation (you are reading it) |

---

## 📊 Results

- **Training Accuracy**: ~99%
- **Test Accuracy**: ~98%
- **Confusion Matrix**: High precision and recall for both classes

---

## ▶️ How to Use

```bash
# Install required packages
pip install xgboost pandas scikit-learn matplotlib
```

```python
import xgboost as xgb
model = xgb.XGBClassifier()
model.load_model("xgb_ticket.json")
```

Make sure your input data matches the training structure used in the notebook.

---

## 📌 Next Steps

- Deploy model in a REST API (FastAPI)
- Add SHAP for interpretability
- Extend to multiclass cancellation types (e.g., user-initiated vs. system-initiated)

---

## 📜 Citation

If you use this model or dataset in your work, please consider citing the author or referencing the [GitHub project](https://github.com/Ella-developer/Prediction-Of-Ticket-Cancellation).
