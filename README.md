# Heart Disease Prediction System

A machine learning-based heart disease prediction system with a graphical user interface built using PyQt5. This project uses multiple machine learning algorithms to predict the likelihood of heart disease based on various medical parameters.

## 🏥 Project Overview

This system analyzes patient data using machine learning models to predict whether a person has heart disease or not. The prediction is based on 13 different medical features including age, sex, chest pain type, blood pressure, cholesterol levels, and other cardiovascular indicators.

## 📁 Project Structure

```
minivaish/
├── data.csv              # Heart disease dataset
├── train_models.py       # Script to train and save ML models
├── heart_disease_gui.py  # PyQt5 GUI application
├── svm_model.pkl         # Trained SVM model
├── scaler.pkl           # Data scaler for preprocessing
├── logistic_model.pkl   # Trained Logistic Regression model
├── tree_model.pkl       # Trained Decision Tree model
├── forest_model.pkl     # Trained Random Forest model
└── README.md            # Project documentation
```

## 🚀 Features

- **Multiple ML Models**: SVM, Logistic Regression, Decision Tree, and Random Forest
- **User-Friendly GUI**: Intuitive PyQt5 interface for easy data input
- **Real-time Prediction**: Instant heart disease prediction results
- **Data Preprocessing**: Automatic scaling and normalization
- **Model Persistence**: Pre-trained models saved for immediate use

## 📊 Dataset Information

The system uses a heart disease dataset with the following features:

| Feature | Description | Type |
|---------|-------------|------|
| age | Age in years | Numeric |
| sex | Gender (1 = male, 0 = female) | Binary |
| cp | Chest pain type (0-3) | Categorical |
| trestbps | Resting blood pressure | Numeric |
| chol | Serum cholesterol | Numeric |
| fbs | Fasting blood sugar > 120 mg/dl | Binary |
| restecg | Resting electrocardiographic results | Categorical |
| thalach | Maximum heart rate achieved | Numeric |
| exang | Exercise induced angina | Binary |
| oldpeak | ST depression induced by exercise | Numeric |
| slope | Slope of peak exercise ST segment | Categorical |
| ca | Number of major vessels colored by fluoroscopy | Numeric |
| thal | Thalassemia | Categorical |

## 🛠️ Installation & Setup

### Prerequisites

Make sure you have Python 3.7+ installed on your system.

### Required Packages

Install the required packages using pip:

```bash
pip install pandas numpy scikit-learn joblib PyQt5
```

### Quick Start

1. **Clone or download the project files**
2. **Train the models** (if not already done):
   ```bash
   python train_models.py
   ```
3. **Run the GUI application**:
   ```bash
   python heart_disease_gui.py
   ```

## 🎯 Usage

### Training Models

Run the training script to train and save all machine learning models:

```bash
python train_models.py
```

This will:
- Load the heart disease dataset
- Split data into training and testing sets
- Train SVM, Logistic Regression, Decision Tree, and Random Forest models
- Save the trained models as `.pkl` files
- Display accuracy and precision metrics for each model

### Using the GUI

1. Launch the application: `python heart_disease_gui.py`
2. Enter patient data in the input fields:
   - **Age**: Patient's age in years
   - **Sex**: 1 for male, 0 for female
   - **Chest Pain Type**: 0-3 (typical angina, atypical angina, non-anginal pain, asymptomatic)
   - **Resting Blood Pressure**: in mm Hg
   - **Cholesterol**: in mg/dl
   - **Fasting Blood Sugar**: 1 if > 120 mg/dl, 0 otherwise
   - **Resting ECG**: 0-2 (normal, ST-T wave abnormality, left ventricular hypertrophy)
   - **Max Heart Rate**: achieved during exercise
   - **Exercise Angina**: 1 if yes, 0 if no
   - **ST Depression**: induced by exercise relative to rest
   - **Slope**: 0-2 (upsloping, flat, downsloping)
   - **Vessels**: number of major vessels (0-3)
   - **Thalassemia**: 0-2 (normal, fixed defect, reversible defect)

3. Click "Predict" to get the result
4. The system will display whether the person has heart disease or not

## 🤖 Machine Learning Models

The system includes four different machine learning algorithms:

1. **Support Vector Machine (SVM)**: Linear kernel with C=3.0
2. **Logistic Regression**: Maximum iterations = 1000
3. **Decision Tree**: Default parameters with random state
4. **Random Forest**: Default parameters with random state

All models are trained on 80% of the data and tested on 20%, with stratified sampling to maintain class balance.

## 📈 Performance Metrics

The models are evaluated using:
- **Accuracy**: Overall prediction accuracy
- **Precision**: True positive rate for heart disease detection

## 🔧 Technical Details

- **Data Preprocessing**: StandardScaler for feature normalization
- **Model Persistence**: Joblib for saving/loading trained models
- **GUI Framework**: PyQt5 for cross-platform compatibility
- **Data Handling**: Pandas for data manipulation and analysis

