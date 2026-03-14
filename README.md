# 🍊 Orange Quality Classification (Machine Learning)

This project demonstrates a simple **Machine Learning classification system** to predict the **quality of oranges** based on their physical and environmental characteristics.

The project consists of two main components:

1. **Model Training Script** – builds and trains a Logistic Regression model using Scikit-learn.
2. **Streamlit Web Application** – provides an interactive UI to predict orange quality.

---

# 📊 Project Overview

The model predicts orange quality based on the following features:

| Feature | Description |
|------|------|
| diameter | Diameter of the orange |
| berat | Weight of the orange |
| tebal_kulit | Thickness of the peel |
| kadar_gula | Sugar content |
| asal_daerah | Region where the orange was grown |
| warna | Color of the orange |
| musim_panen | Harvest season |

The machine learning model learns patterns from the training dataset and classifies the orange quality accordingly.

---

# 🧠 Machine Learning Model

The model used in this project is:

**Logistic Regression**

The training pipeline includes:

- Standard Scaling for numeric features
- One Hot Encoding for categorical features
- Ordinal Encoding for ordered categories
- Scikit-learn Pipeline for clean preprocessing + model integration

---

# ⚙️ Model Training Pipeline

The preprocessing pipeline is implemented using:

- `StandardScaler`
- `OneHotEncoder`
- `OrdinalEncoder`
- `ColumnTransformer`
- `Pipeline`

Workflow:


Raw Data
↓
Preprocessing
↓
Feature Scaling / Encoding
↓
Logistic Regression Model
↓
Prediction


The trained model is saved using:


joblib.dump(model, "model_klasifikasi_jeruk.joblib")


---

# 📁 Project Structure


orange-classification
│
├── train_model.py
├── app.py
├── model_klasifikasi_jeruk.joblib
├── dataset.csv
└── README.md


| File | Description |
|-----|-----|
| train_model.py | Script used to train the machine learning model |
| app.py | Streamlit application |
| model_klasifikasi_jeruk.joblib | Saved trained model |
| dataset.csv | Training dataset |
| README.md | Project documentation |

---

# 🚀 Running the Project

## 1️⃣ Install Dependencies

```bash
pip install pandas scikit-learn streamlit joblib

2️⃣ Train The Model

Run the training script:

python train_model.py

This will generate:

model_klasifikasi_jeruk.joblib
3️⃣ Run the Web App

Start the Streamlit application:

streamlit run app.py
🖥️ Streamlit Web Application

The Streamlit app allows users to interactively input orange characteristics and receive predictions.

Users can adjust parameters using sliders and selection buttons:

Diameter

Weight

Peel Thickness

Sugar Content

Origin Region

Orange Color

Harvest Season

The model will then output:

Predicted Orange Quality
Prediction Confidence
📦 Technologies Used

Python

Pandas

Scikit-learn

Streamlit

Joblib

🎯 Purpose of the Project

This project was built as a learning exercise in machine learning deployment, covering:

Data preprocessing

Model training

Pipeline design

Model persistence

Interactive web deployment

👨‍💻 Author

Adi Setiawan

Built using Python, Scikit-learn, and Streamlit.
