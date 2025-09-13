# Titanic Survival Prediction – Machine Learning Project

## 📌 Project Overview
This project is based on the **Titanic dataset**, where the goal is to predict whether a passenger survived (1) or not (0).  
The task is formulated as a **binary classification problem** using supervised machine learning methods.

The project includes:
- Data exploration and visualization
- Feature engineering and preprocessing
- Model selection and hyperparameter tuning
- Training and evaluation on test data

---

## 📂 Dataset
The dataset contains passenger information such as:
- `Pclass` – Passenger class (1st, 2nd, 3rd)
- `Sex` – Gender (0 = female, 1 = male)
- `Age` – Passenger age
- `SibSp` – Number of siblings/spouses aboard
- `Parch` – Number of parents/children aboard
- `Fare` – Ticket fare
- `Embarked` – Port of embarkation
- `Survived` – Survival status (target variable)

---

## ⚙️ Workflow

### Part 1 – Introduction
- Defined the learning problem as binary classification.  
- Explained dataset attributes.  
- Mentioned that minimal AI-agent assistance (ChatGPT) was used only for clarification of concepts and small Python tips.

### Part 2 – Initial Preparations
- Loaded training and test datasets.  
- Basic preprocessing (handling missing values).  
- Initial visualizations:
  - Gender vs. Survival (barplot)
  - Age distribution vs. Survival (boxplot)

### Part 3 – Experiments
- Created dummy variables for categorical features.  
- Applied **MinMaxScaler** on numerical features (`Age`, `SibSp`, `Parch`, `Fare`).  
- Used **K-Nearest Neighbors (KNN)** with **GridSearchCV**.  
- Hyperparameter tuning across multiple values (`n_neighbors`, `weights`, `algorithm`, `p`, `metric`).  
- Best result achieved: **F1 score ≈ 0.73**.

### Part 4 – Training
- Trained the final model using the best hyperparameters found in experiments:
  - `KNeighborsClassifier(n_neighbors=3, algorithm='ball_tree', metric='euclidean', p=1, weights='uniform')`

### Part 5 – Evaluation
- Applied the trained model to the **test dataset**.  
- Performance results:
  - **Accuracy:** ~82%  
  - **F1 Score:** ~0.73  
- Displayed confusion matrix (both raw counts and percentages).  
- Compared first 5 predictions vs actual outcomes.

---

## 📊 Results
- **Best Model:** K-Nearest Neighbors (KNN)  
- **Cross-validation Mean F1:** ~0.734  
- **Test Set Accuracy:** ~0.82  
- **Test Set F1:** ~0.73  

The model successfully captures patterns in the Titanic dataset and demonstrates good performance on unseen data.
