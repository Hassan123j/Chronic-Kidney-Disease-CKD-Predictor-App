# CKD Predictor – Chronic Kidney Disease Prediction App

This is a small Streamlit app I built that predicts whether someone might have Chronic Kidney Disease (CKD) based on basic clinical info. It uses a machine learning model trained on real-world patient data.

## Demo

Here’s a quick demo and explanation of how the app works:  
[View the project on LinkedIn](https://www.linkedin.com/posts/hassan-ahmed-ai_sharing-a-recent-project-a-ckd-predictor-activity-7343216366063120385-Um6M?utm_source=share&utm_medium=member_desktop&rcm=ACoAADcMskUBCV1EYOEZsfJd6ub2yVedI94Bhuc)

## What's in this repo

- `app.py` - the main Streamlit app
- `CKD Model.ipynb` - a Jupyter notebook that walks through data cleaning, model training, and evaluation
- `kidney_disease.csv` - the dataset I used
- `models/` folder:
  - `model_gbc.pkl`: the trained Gradient Boosting model
  - `scaler.pkl`: the fitted scaler used for preprocessing
- `requirements.txt` - list of Python packages used

## How to run it locally

If you want to test this on your machine:

### 1. Clone the repo

```bash
git clone https://github.com/Hassan123j/Chronic-Kidney-Disease-CKD-Predictor-App.git
cd Chronic-Kidney-Disease-CKD-Predictor-App
````

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
```

### 3. Install the dependencies

```bash
pip install -r requirements.txt
```

### 4. Check if the model files are there

Make sure you have these two files in the `models/` folder:

* `model_gbc.pkl`
* `scaler.pkl`

If they’re missing, open `CKD Model.ipynb` and run the notebook to train the model and save the files.

### 5. Run the app

```bash
streamlit run app.py
```

## Features used in the prediction

The model uses a number of clinical features like:

* Age
* Blood Pressure
* Specific Gravity
* Albumin
* Sugar
* Hemoglobin
* Serum Creatinine
* Packed Cell Volume
* and more...

(You’ll see the full list in the app UI.)

## Notes

* Input data is scaled and encoded before feeding it to the model. This is the same preprocessing used during training.
* If you retrain the model, be sure to replace both `.pkl` files in the `models/` folder with your updated ones.

## Built With

* Python
* Streamlit
* scikit-learn
* pandas and numpy
* Jupyter Notebook

## License

This project is MIT licensed.

---

If you find this useful or interesting, feel free to fork the repo or open an issue. Thanks for checking it out!

