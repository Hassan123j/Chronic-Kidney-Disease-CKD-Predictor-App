# CKD Predictor App

This is a simple Streamlit app that predicts Chronic Kidney Disease (CKD) based on patient data. It uses a Gradient Boosting model trained on a dataset of clinical records.

## What’s inside

- A trained model (`model_gbc.pkl`) and scaler (`scaler.pkl`)
- Streamlit frontend to input patient data and get predictions
- A Jupyter notebook that walks through the full ML pipeline (data cleaning, training, evaluation)
- Dataset: `kidney_disease.csv`

## Getting started

Here’s how to run it locally:

### 1. Clone this repo

```bash
git clone https://github.com/Hassan123j/Chronic-Kidney-Disease-CKD-Predictor-App.git
cd Chronic-Kidney-Disease-CKD-Predictor-App
```

### 2. Set up a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Make sure the model files are in place

Check that `models/model_gbc.pkl` and `models/scaler.pkl` exist. If not, run the notebook to generate them:

```bash
jupyter notebook "CKD Model.ipynb"
```

### 5. Run the app

```bash
streamlit run app.py
```

## Folder layout

```
.
├── app.py                 # Streamlit app
├── CKD Model.ipynb        # Model training notebook
├── kidney_disease.csv     # Dataset
├── requirements.txt       # Python packages
└── models/
    ├── model_gbc.pkl
    └── scaler.pkl
```

## Notes

- The model expects input data to be preprocessed the same way it was during training (scaling, encoding, etc.)
- If you retrain the model, replace both `.pkl` files in the `models/` folder

## Python packages used

- streamlit
- pandas
- numpy
- scikit-learn
- joblib
