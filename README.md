# ❤️ Heart Disease Prediction using Logistic Regression

## 📌 Project Overview

This project uses **Machine Learning** to predict whether a person is likely to have heart disease based on various medical attributes.

A **Logistic Regression** classification model is trained on a heart disease dataset and evaluated using training and testing accuracy.

## 🔄 Project Workflow

**Heart Disease Data → Data Preprocessing → Train-Test Split → Logistic Regression → Model Evaluation → Prediction**

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn
* Google Colab

## 🤖 Machine Learning Algorithm

### Logistic Regression

Logistic Regression is used as the classification algorithm to predict the target variable.

The target values are:

* `1` → Heart disease
* `0` → No heart disease

## 📊 Dataset

The dataset contains **303 records** and **14 columns**, including the target variable.

The features include:

| Feature    | Description                           |
| ---------- | ------------------------------------- |
| `age`      | Age of the person                     |
| `sex`      | Sex                                   |
| `cp`       | Chest pain type                       |
| `trestbps` | Resting blood pressure                |
| `chol`     | Serum cholesterol                     |
| `fbs`      | Fasting blood sugar                   |
| `restecg`  | Resting electrocardiographic results  |
| `thalach`  | Maximum heart rate achieved           |
| `exang`    | Exercise-induced angina               |
| `oldpeak`  | ST depression induced by exercise     |
| `slope`    | Slope of the peak exercise ST segment |
| `ca`       | Number of major vessels               |
| `thal`     | Thalassemia                           |
| `target`   | Heart disease prediction              |

## ⚙️ Project Steps

### 1. Import Dependencies

The project uses NumPy, Pandas, Scikit-learn's `train_test_split`, `LogisticRegression`, and `accuracy_score`.

### 2. Data Collection and Processing

The dataset is loaded into a Pandas DataFrame using:

```python
heart_data = pd.read_csv('/content/heart_disease_data.csv')
```

The dataset is then explored by checking:

* First and last few records
* Number of rows and columns
* Dataset information
* Missing values
* Statistical measures
* Target variable distribution

### 3. Splitting Features and Target

The `target` column is separated from the input features.

```python
X = heart_data.drop(columns='target', axis=1)
Y = heart_data['target']
```

### 4. Train-Test Split

The dataset is divided into training and testing data using an **80:20 split**.

Stratified splitting is used to maintain the distribution of the target variable.

### 5. Model Training

A **Logistic Regression** model is created and trained using the training dataset.

```python
model = LogisticRegression()
model.fit(X_train, Y_train)
```

### 6. Model Evaluation

The model's performance is evaluated using **Accuracy Score** on:

* Training data
* Testing data

### 7. Predictive System

A sample patient's medical information is provided to the trained model to predict whether the person is likely to have heart disease.

## 📈 Results

The notebook calculates and displays:

* Accuracy on Training Data
* Accuracy on Test Data

The exact accuracy values can be obtained by running the notebook.

## 📂 Project Structure

```text
heart-disease-prediction/
│
├── Heart_Diseases_Prediction.ipynb
├── heart_disease_data.csv
└── README.md
```

## ▶️ How to Run the Project

### Using Google Colab

1. Open `Heart_Diseases_Prediction.ipynb` in Google Colab.
2. Upload `heart_disease_data.csv` to the Colab session.
3. Run the notebook cells sequentially.
4. The model will train and display the training and testing accuracy.
5. The predictive system can then be used to make a sample prediction.

### Using Jupyter Notebook

1. Download or clone this repository.
2. Install the required Python libraries.
3. Make sure `heart_disease_data.csv` is available in the required location.
4. Open `Heart_Diseases_Prediction.ipynb`.
5. Run all cells.

## 📚 Key Learning Outcomes

Through this project, I practiced:

* Data loading and exploration
* Data preprocessing
* Checking missing values
* Feature and target separation
* Train-test splitting
* Logistic Regression
* Model evaluation using accuracy
* Building a simple predictive system

## ⚠️ Disclaimer

This project is created for **educational and machine learning practice purposes**. It is not intended to provide medical diagnosis or replace professional medical advice.

## 👩‍💻 Author

**Sapna**
