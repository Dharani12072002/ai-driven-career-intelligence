# AI-Driven Career Transition Intelligence

This project predicts **Career Transition Difficulty** using **Neural Network models**.  
It includes **both Classification and Regression approaches** to analyze how difficult a career transition may be for an individual based on professional and personal factors.

---

## Project Objectives

- Calculate a **Career Transition Difficulty Index**
- Predict difficulty using:
  - **Regression** (continuous difficulty score)
  - **Classification** (Low / High difficulty)
- Evaluate models using standard machine learning metrics

---

## Dataset Description

The dataset contains the following features:

- Years of Experience  
- Job Satisfaction  
- Work-Life Balance  
- Technology Adoption  

Missing values are removed during preprocessing.

---

## Career Transition Difficulty Index

The difficulty index is computed using the formula:

Difficulty Index = 0.4 × Years of Experience

- 0.3 × (100 − Job Satisfaction)
- 0.2 × (100 − Work-Life Balance)
- 0.1 × Technology Adoption


- Used directly as the target for the **regression model**
- Converted into binary labels for the **classification model**

---

## Model Architecture

### Input Layer
- 4 neurons (one for each feature)
- Features are standardized using `StandardScaler`

### Hidden Layers
- Dense layer (128 neurons, ReLU)
- Dense layer (64 neurons, ReLU)
- Dense layer (32 neurons, ReLU)
- Dropout layers to prevent overfitting

### Output Layer
- **Regression**: 1 neuron with Linear activation  
- **Classification**: 1 neuron with Sigmoid activation  

---

## Training Configuration

- Optimizer: Adam  
- Loss Function:
  - Regression: Mean Squared Error (MSE)
  - Classification: Binary Crossentropy
- Epochs: Up to 200
- Batch Size: 32
- Early Stopping enabled (patience = 20)

Training stops automatically when validation performance converges.

---

## Evaluation Metrics

### Regression
- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
- R² Score
- Error Distribution Plot
- Actual vs Predicted Plot

### Classification
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---


---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ai-driven-career-intelligence.git

2. Install dependencies:
   pip install pandas numpy matplotlib scikit-learn tensorflow

3. Run the models:
   python regression_model.py
   python classification_model.py




