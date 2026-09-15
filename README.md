# 🏡 NYC Airbnb Room Type Predictor

An **End-to-End Machine Learning Web Application** that predicts the **room type** of an Airbnb listing using a dataset of **48,895 NYC Airbnb listings**.

The project covers the complete Machine Learning workflow — from **data preprocessing and exploratory data analysis to model training, evaluation, FastAPI backend integration, and frontend development**.

---

## 🚀 Project Overview

The goal of this project is to build a Machine Learning system capable of predicting the room type of an Airbnb listing based on its available features.

The application provides a user-friendly frontend where users can enter listing information. The data is then sent to a **FastAPI backend**, processed through the trained preprocessing pipeline, and passed to the Machine Learning model to generate a prediction.

### 🔄 End-to-End Workflow

```text
User Input
    ↓
HTML / CSS / JavaScript Frontend
    ↓
FastAPI Backend
    ↓
Data Preprocessing Pipeline
    ↓
Trained ML Model
    ↓
Room Type Prediction
    ↓
Prediction displayed on Frontend
```

---

## 📊 Dataset

The project uses the **NYC Airbnb Open Data** dataset containing **48,895 Airbnb listings**.

The dataset contains information related to:

* Location
* Neighborhood
* Room type
* Price
* Minimum nights
* Number of reviews
* Reviews per month
* Availability
* Host information
* And other listing-related features

### 🎯 Target Variable

The target variable is:

```text
room_type
```

Possible room types include:

* Entire home/apt
* Private room
* Shared room

One of the challenges was **class imbalance**, particularly because Shared Room listings represent a much smaller class compared with the other room types.

---

# 🧹 Data Preprocessing & EDA

The dataset was explored and prepared before training the Machine Learning models.

### Data Preparation

* Loaded and inspected the dataset
* Checked dataset dimensions
* Identified missing values
* Examined data types
* Analyzed categorical and numerical features
* Identified potential outliers
* Performed Exploratory Data Analysis
* Investigated the target-class distribution
* Prepared features for Machine Learning

### Preprocessing Pipeline

A Scikit-Learn preprocessing pipeline was implemented to ensure that the same transformations are applied consistently during training and prediction.

The pipeline includes:

* Missing-value imputation
* Numerical feature scaling
* Categorical feature encoding
* One-Hot Encoding

This approach helps prevent inconsistent preprocessing between the training environment and the deployed application.

---

# 🤖 Machine Learning

Multiple Machine Learning models were trained and compared to identify a suitable model for the prediction task.

### Models Explored

* Random Forest
* Gradient Boosting
* Other classification models

The models were evaluated using appropriate classification metrics and validation techniques.

### Model Evaluation

The project includes:

* Train/Test Split
* Cross-Validation
* Confusion Matrix
* Classification Performance Evaluation
* Model Comparison
* Hyperparameter Tuning

After evaluation, the best-performing model was selected and saved for integration with the application.

---

# ⚙️ FastAPI Backend

The trained Machine Learning model was integrated into a **FastAPI backend**.

FastAPI provides an API endpoint that receives listing information from the frontend and returns the predicted room type.

### Prediction Flow

```text
Frontend Form
      ↓
HTTP Request
      ↓
FastAPI API
      ↓
Preprocessing Pipeline
      ↓
ML Model
      ↓
Prediction
      ↓
JSON Response
      ↓
Frontend
```

This allows the Machine Learning model to operate as part of a real application rather than only inside a notebook.

---

# 💻 Frontend

A custom frontend was developed for interacting with the Machine Learning model.

### Technologies Used

* HTML
* CSS
* JavaScript

The frontend allows users to:

1. Enter the required Airbnb listing information.
2. Submit the information.
3. Send the data to the FastAPI backend.
4. Receive the model prediction.
5. Display the predicted room type.

---

# 🛠️ Technologies Used

| Technology   | Purpose                              |
| ------------ | ------------------------------------ |
| Python       | Core programming language            |
| Pandas       | Data manipulation                    |
| NumPy        | Numerical operations                 |
| Matplotlib   | Data visualization                   |
| Seaborn      | Exploratory data analysis            |
| Scikit-Learn | Machine Learning & preprocessing     |
| FastAPI      | Backend API                          |
| HTML         | Frontend structure                   |
| CSS          | Frontend styling                     |
| JavaScript   | Frontend interaction                 |
| Git & GitHub | Version control & project management |

---

# 📁 Project Structure

```text
NYC-Airbnb-Room-Type-Predictor/
│
├── data/
│   └── AB_NYC_2019.csv
│
├── notebooks/
│   └── analysis_and_modeling.ipynb
│
├── model/
│   └── trained_model.pkl
│
├── static/
│   ├── style.css
│   └── script.js
│
├── templates/
│   └── index.html
│
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
```

> The exact file structure may vary depending on the final version of the project.

---

# ▶️ How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/sabirullah514-ops/NYC-Airbnb-Room-Type-Predictor.git
```

## 2. Navigate to the Project

```bash
cd NYC-Airbnb-Room-Type-Predictor
```

## 3. Create a Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
source venv/bin/activate
```

## 4. Install Dependencies

```bash
pip install -r requirements.txt
```

## 5. Start the FastAPI Application

If your application entry point is `app.py`:

```bash
uvicorn app:app --reload
```

The application will then be available locally through the FastAPI server.

---

# 🔌 API

The application exposes a prediction endpoint through FastAPI.

### Example Request

```text
POST /predict
```

The endpoint receives the required Airbnb listing features and sends them through the preprocessing pipeline and trained model.

### Example Response

```json
{
    "prediction": "Private room"
}
```

> The exact endpoint name and request/response format depend on the implementation in the current version of the project.

---

# 📈 Key Challenges

### 1. Class Imbalance

The dataset contains significantly fewer Shared Room listings than other room types.

This required careful evaluation because overall accuracy alone may not fully represent model performance across all classes.

### 2. Categorical Features

The dataset contains several categorical variables that cannot be directly provided to most Machine Learning algorithms.

These were handled using **One-Hot Encoding**.

### 3. Missing Values

Missing values were identified and handled through the preprocessing pipeline.

### 4. ML-to-Application Integration

A major part of the project was connecting the trained Machine Learning model with a real web application using **FastAPI, HTML, CSS, and JavaScript**.

---

# 🎯 Learning Outcomes

Through this project, I gained practical experience in:

* Data Cleaning
* Exploratory Data Analysis
* Feature Preprocessing
* Machine Learning Classification
* Scikit-Learn Pipelines
* Handling Imbalanced Classes
* Model Evaluation
* Cross-Validation
* Hyperparameter Tuning
* Model Serialization
* FastAPI
* REST API Integration
* Frontend Development
* Connecting ML models with web applications

---

# 🌟 Key Takeaway

This project helped demonstrate that building a Machine Learning solution is not only about training a model.

A practical ML system requires a complete workflow:

```text
Data
 ↓
Preprocessing
 ↓
Model Training
 ↓
Evaluation
 ↓
Model Saving
 ↓
Backend API
 ↓
Frontend
 ↓
Prediction
```

The project therefore represents my hands-on experience in building an **end-to-end Machine Learning application**.

---

# 🔗 Repository

**GitHub:**
https://github.com/sabirullah514-ops/NYC-Airbnb-Room-Type-Predictor

---

# 👨‍💻 Author

**Sabir Ullah**

Computer Science | Data Science | Artificial Intelligence | Machine Learning

---

## 📌 Future Improvements

Potential improvements for future versions include:

* Deploying the application to a cloud platform
* Improving model performance on minority classes
* Adding more advanced feature engineering
* Experimenting with additional classification algorithms
* Adding automated model monitoring
* Improving frontend UX/UI
* Containerizing the application with Docker
* Adding automated testing and CI/CD
