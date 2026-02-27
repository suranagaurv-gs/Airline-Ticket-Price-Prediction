# Airlines Ticket Price Prediction


## Project Description
This project predicts airline ticket prices using various machine learning regression techniques.  
The dataset is cleaned, preprocessed, and transformed to extract key features such as journey date, departure and arrival times, duration in minutes, and total stops.  
The best performing model (Random Forest with hyperparameter tuning) is saved for deployment.

---

## Dataset
- Historical flight ticket data.
- Columns include:
  - Airline
  - Source
  - Destination
  - Date_of_Journey
  - Dep_Time
  - Arrival_Time
  - Total_Stops
  - Duration
  - Price
- Cleaned dataset is saved in `data/processed/cleaned_airlines.csv`.

---

## Project Structure

airlines-ticket-price-prediction/
│
├── notebooks/ 
├── data/ 
      ├── raw/
      └── processed/cleaned_airlines.csv
├── models/
      ├── linear_regression.pkl
      ├── xgboost.pkl
      ├── catboost.pkl
      ├─scaler.pkl
      └── airline_rf_model.pkl
       
├── README.md 
└── requirements.txt 


---



## Models Used
1. Linear Regression
2. Random Forest (Hyperparameter Tuned – Best Model)
3. XGBoost
4. CatBoost

---



## How to Run

1. Clone the repository:

```bash
git clone https://github.com/suranagaurv-gs/Airlines-Ticket-Price-Prediction.git


2. Install required libraries:

pip install -r requirements.txt





## Model Performance


| Model                 | RMSE    | R²    |
| --------------------- | ----    | ----  |
| Random Forest (Tuned) | 2784.77 | 0.984 |
| Linear Regression     | 6761.94 | 0.911 |
| XGBoost               | 3788.62 | 0.972 |
| CatBoost              | 4281.28 | 0.964 |


## Final Tuned Model

The final Random Forest model was trained using hyperparameter tuning.
Due to GitHub file size limitations, the trained model file is not uploaded.

To regenerate the model:
Run the notebook: notebooks/model_training.ipynb


## Acknowledgements
- Kaggle Airline Price Prediction dataset
- Scikit-learn documentation
- XGBoost and CatBoost official documentation



## Notes
- Preprocessing and feature extraction are crucial to reduce high-dimensional data and prevent memory overload.
- The `models/` folder contains serialized `.pkl` files ready for deployment.
- The `data/processed/` folder contains the cleaned dataset used for model training.
- The Random Forest (Tuned) model is recommended for deployment as it performed best on evaluation metrics.
