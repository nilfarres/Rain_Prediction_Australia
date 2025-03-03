# Rain Prediction in Australia

## Overview
This project explores the **application of machine learning to predict daily rainfall in Australia, using 10 years of meteorological observations (2007-2017)**. The dataset, sourced from Kaggle, includes various weather parameters, and the model employs the XGBClassifier, **achieving an accuracy of 86%**. The results highlight the significance of wind direction, evaporation, humidity, and sunlight in rainfall prediction.

## Dataset
- **Source:** The dataset is obtained from Kaggle and contains weather records from different locations across Australia.
- **Features:**
  - Date and location
  - Minimum and maximum temperature
  - Rainfall amount
  - Evaporation and sunshine hours
  - Wind gust speed and direction
  - Humidity levels
  - Atmospheric pressure
  - Cloud cover (in oktas)
  - Temperature at 9 AM and 3 PM
  - Target variable: `RainTomorrow` (Yes/No)

## Methodology
1. **Data Preprocessing**
   - Handling missing values with KNNImputer
   - Encoding categorical variables using Target Encoding
   - Feature scaling using Standard Scaler
   - Creation of additional features: monthly and weekly rainfall averages, last three days' rainfall
2. **Exploratory Data Analysis (EDA)**
   - Data visualization to identify patterns
   - Analysis of weather conditions influencing rainfall
3. **Model Training**
   - Comparison of models: Random Forest, XGBClassifier, LGBMClassifier, AdaBoostClassifier, KNeighborsClassifier
   - XGBClassifier selected as the best-performing model
   - Hyperparameter tuning for optimal results
4. **Prediction & Performance Metrics**
   - Accuracy: 86%
   - Precision-Recall (PR) Curve AUPRC: 0.75
   - Performance breakdown:
     - Non-rainy days: Precision 88%, Recall 95%
     - Rainy days: Precision 75%, Recall 56%

## Files in the Repository
- `Cas_Kaggle_vf.ipynb`: Jupyter Notebook with data analysis and model training.
- `weatherAUS.csv`: The dataset containing weather records.
- `Informe_Cas_Kaggle.pdf`: Report explaining the project.
- Preprocessed datasets (`.joblib` files): Used for training and testing models.

## Requirements
To run this project, you need the following dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib xgboost
```

## Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Rain-Prediction-Australia.git
   ```
2. Navigate to the project folder and open the Jupyter Notebook:
   ```bash
   jupyter notebook Cas_Kaggle_vf.ipynb
   ```
3. Run the notebook cells to preprocess data, train models, and evaluate performance.

## Results
The best-performing model (XGBClassifier) achieves an accuracy of **86%** in predicting rainfall, with a Precision-Recall AUPRC of **0.75**. The wind direction at 3 PM (especially SW and WNW) is the most influential predictor, showing a strong correlation with increased humidity and decreased atmospheric pressure, key indicators of rainfall the next day.

## License
This project is open-source and available under the MIT License.

---
**Author:** Nil Farrés Soler



