# Personalized Nutrition Predictor

A **machine learning-powered application** to predict personalized nutritional requirements based on user health data. 
This project uses **Ridge Regression**, **Feedforward Neural Networks (FFNN)**, and **Random Forest Regressor (RFR)** 
to deliver accurate predictions. It features a user-friendly **Tkinter GUI** for seamless interaction, enabling data 
upload, model training, and predictions.

---

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Future Enhancements](#future-enhancements)
7. [Contributing](#contributing)
8. [License](#license)

---

## Overview

The **Personalized Nutrition Predictor** addresses the limitations of generalized nutritional recommendations by using 
**machine learning and deep learning models**. It provides personalized caloric recommendations based on health metrics, 
activity levels, and dietary patterns. The GUI allows non-technical users to interact with the system effortlessly.

---

## Features

- **Data Preprocessing**: Handles missing values, encodes categorical data, and visualizes feature correlations.
- **Ridge Regression**: Provides a baseline model for predictions.
- **FFNN + Random Forest Regressor**: Captures complex, non-linear relationships for more accurate results.
- **Performance Metrics**: Displays MAE, MSE, RMSE, and R² for model evaluation.
- **Interactive GUI**: Built with Tkinter for easy data upload, preprocessing, and prediction.

---

## Technologies Used

- **Languages**: Python
- **Libraries**:
  - **Data Handling**: `pandas`, `numpy`
  - **Visualization**: `matplotlib`, `seaborn`
  - **Machine Learning**: `scikit-learn`, `tensorflow`
  - **GUI**: `Tkinter`
- **Modeling Techniques**:
  - Ridge Regression
  - Feedforward Neural Networks (FFNN)
  - Random Forest Regressor (RFR)



---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/personalized-nutrition-predictor.git
   cd personalized-nutrition-predictor
python main.py

---

## Usage

**Upload Dataset**: Load a .csv file with user health data via the GUI.

**Preprocess Data**: Clean and transform the data for modeling.

**Train Models**: Select between Ridge Regression or FFNN + RFR.

**Evaluate Performance**: View model accuracy metrics and predictions.

**Predict Nutrition**: Use test data to predict caloric needs.

---
## Future Enhancements
1. Integrate FastAPI for web-based predictions.
2. Add real-time data processing from wearable devices (e.g., Fitbit, smartwatches).
3. Improve explainability using SHAP or LIME for model interpretability.

---
## Contributing
**We welcome contributions to improve this project! Follow these steps to contribute**:

Fork the repository.

**Create a feature branch:**


git checkout -b feature-name

**Commit changes and push the branch:**

git commit -m "Added new feature"

git push origin feature-name

Open a pull request.

---
## License
This project is licensed under the MIT License.




