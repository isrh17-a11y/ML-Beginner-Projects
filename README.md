# ML Mini-Projects 

A collection of beginner-to-intermediate machine learning projects covering classification, regression, and a rule-based chatbot. Each notebook is self-contained and demonstrates a full workflow: data loading, preprocessing, model training, evaluation, and a single-sample prediction demo.

## Projects

### 🩺 Breast Cancer Prediction
**File:** `Breast_Cancer_prediction_.ipynb`

A binary classification model that predicts whether a breast tumor is **malignant** or **benign**.

- **Dataset:** scikit-learn's built-in `load_breast_cancer` (30 numeric features per tumor — radius, texture, smoothness, etc.)
- **Model:** Logistic Regression
- **Pipeline:** train/test split → `StandardScaler` → `LogisticRegression` → accuracy evaluation
- **Demo:** predicts the diagnosis for a single sample input

**Tech stack:** `scikit-learn`, `numpy`

---

### 💉 Diabetes Progression Prediction
**File:** `Diabetes_diagnosis.ipynb`

A regression model that predicts a patient's diabetes progression score one year after baseline.

- **Dataset:** scikit-learn's built-in `load_diabetes` (10 normalized features — age, BMI, blood pressure, etc.)
- **Model:** Linear Regression
- **Pipeline:** train/test split → `StandardScaler` → `LinearRegression` → MSE / R² evaluation
- **Visualization:** Actual vs. Predicted scatter plot
- **Demo:** predicts a progression score for a single new patient

**Tech stack:** `scikit-learn`, `numpy`, `pandas`, `matplotlib`

> **Note:** This dataset's target is a continuous score, not a yes/no diabetes diagnosis. The final cell's `if prediction[0] == 1` check is left over from a classification template and doesn't reflect the regression output — worth revising if you want a true positive/negative diagnosis message.

---

### 🏠 House Sale Price Prediction
**File:** `Salesprediction.ipynb`

A regression model that predicts house sale prices from structural and zoning features.

- **Dataset:** `HousePricePrediction.xlsx` (Kaggle-style housing dataset)
- **Model:** Random Forest Regressor
- **Pipeline:** load Excel data → handle missing values (mean-fill `SalePrice`, drop remaining nulls) → label-encode categorical columns (`MSZoning`, `LotConfig`, `BldgType`, `Exterior1st`) → train/test split → `StandardScaler` → `RandomForestRegressor` → MAE / R² evaluation
- **Demo:** predicts the sale price for a single new house

**Tech stack:** `scikit-learn`, `pandas`, `numpy`, `openpyxl`

---

### 🤖 MIMI — Rule-Based Chatbot
**File:** `CHATBOT.ipynb`

A simple, fun command-line chatbot built with plain Python (no ML/NLP libraries) using keyword matching.

- Responds to greetings, "how are you", weather small talk
- Offers entertainment: riddles, tongue twisters, and rock-paper-scissors
- Runs in a loop via `input()`, exits on "bye"

**Tech stack:** Python standard library only (`random`)

> **Note:** The rock-paper-scissors logic is currently decorative rather than functional — it responds to keywords ("scissors"/"rock" → "ROCK!..oops", "paper" → "YOU WIN!") rather than tracking an actual bot move against the player's choice.

---

## Getting Started

### Prerequisites
```bash
pip install scikit-learn numpy pandas matplotlib openpyxl
```

### Running the notebooks
```bash
jupyter notebook
```
Then open any `.ipynb` file and run all cells in order.

> The House Sale Price notebook requires `HousePricePrediction.xlsx` to be present in the same directory.

## Repository Structure
```
.
├── Breast_Cancer_prediction_.ipynb
├── Diabetes_diagnosis.ipynb
├── Salesprediction.ipynb
├── CHATBOT.ipynb
└── README.md
```

## License
This project is open source and available under the [MIT License](LICENSE).

