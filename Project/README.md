# Heart Disease Detection Using Classification Algorithms

## Project Overview
This project uses supervised machine learning classification algorithms to predict whether a patient may have heart disease based on demographic, clinical, and diagnostic information. It compares multiple models and evaluates their performance using metrics relevant to classification.

> **Important:** This project is for educational and research purposes only. It is not a medical diagnosis tool and must not be used to make clinical decisions.

## Problem Statement
Early detection of heart disease can help healthcare professionals make timely and informed decisions. The goal of this project is to build and compare machine learning models that estimate the presence of heart disease from patient data.

## Objectives
- Explore the dataset and understand the features.
- Perform exploratory data analysis (EDA).
- Prepare the data for machine learning.
- Train and compare classification models:
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - Support Vector Machine (SVM)
- Evaluate models using recall (sensitivity), precision, F1-score, ROC-AUC, specificity, and accuracy.
- Identify a suitable model based on measured results.

## Dataset
**File:** `heart_disease_dataset.csv`

The project brief describes 400 records, 13 input features, and a target column for heart disease. The dataset contains patient-related features such as age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting ECG, maximum heart rate, exercise-induced angina, ST depression, ST slope, number of major vessels, and thalassemia.

### Dataset notes
- Check the actual column names in the CSV before running the notebook. The target is described in the project brief as `heart_disease` (0 = No, 1 = Yes); the brief also contains the spelling `heart_desease`. Update the target-column setting in your code to match the CSV exactly.
- The project brief states that the data has no missing values and is already numeric. Verify these points during EDA rather than assuming they are true.
- Use an 80% training and 20% testing split, as specified in the project brief.

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook / Google Colab
- FastAPI for optional model deployment
- Docker for optional containerization

## Suggested Workflow
1. Load the CSV file and inspect its shape, columns, data types, and sample rows.
2. Check missing values, duplicate rows, and the target-class distribution.
3. Perform EDA with suitable plots and feature comparisons.
4. Separate input features (`X`) from the target (`y`).
5. Split the data into training and testing sets using an 80:20 ratio. Consider stratification to preserve class proportions.
6. Train the selected classification models using the training data.
7. Evaluate each model on the same test set.
8. Compare the results in a table and select a model based on the evaluation metrics and the project goal.
9. Document findings, limitations, and possible next steps.
10. If implemented, expose predictions through FastAPI and package the service with Docker.

## Evaluation Metrics
- **Recall (Sensitivity):** How many actual positive cases the model identifies.
- **Precision:** How many cases predicted positive are actually positive.
- **F1-score:** Harmonic mean of precision and recall.
- **ROC-AUC:** Measures how well the model ranks positive cases above negative cases.
- **Specificity:** How many actual negative cases the model identifies correctly.
- **Accuracy:** Overall fraction of correct predictions.

For a health-related classification task, do not rely on accuracy alone. Report the chosen model's test results and explain the trade-offs between recall, precision, and specificity.

## Repository Structure
A suggested GitHub folder structure is:

```text
Heart-Disease-Detection/
├── README.md
├── heart_disease_dataset.csv
├── notebooks/
│   ├── 01_Heart_Disease_EDA.ipynb
│   ├── 02_Model_Training_and_Comparison.ipynb
│   └── 03_Final_Evaluation.ipynb
├── src/
│   ├── train.py
│   └── evaluate.py
├── app/
│   └── main.py                 # FastAPI, if implemented
├── requirements.txt
└── reports/
    ├── figures/
    └── model_comparison.csv
```

This is a suggested structure. Keep only files and folders that you actually create; remove references to components you have not implemented.

## How to Run
1. Clone or download this repository.
2. Install the required packages:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
   ```

3. Open Google Colab or Jupyter Notebook.
4. Upload `heart_disease_dataset.csv` and open the notebook(s) in `notebooks/`.
5. Run the notebook cells from top to bottom.

If you later implement the FastAPI service, add `fastapi` and `uvicorn` to your dependencies. Add Docker instructions only after a working `Dockerfile` has been created.

## Results
Add your measured results here after running the notebooks. Do not enter model scores until they have been calculated on the test set.

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC | Specificity |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | TBD | TBD | TBD | TBD | TBD | TBD |
| Decision Tree | TBD | TBD | TBD | TBD | TBD | TBD |
| Random Forest | TBD | TBD | TBD | TBD | TBD | TBD |
| SVM | TBD | TBD | TBD | TBD | TBD | TBD |

## Limitations
- The dataset has 400 records according to the project brief, so findings may not generalize to other populations.
- Model results depend on data quality, the train/test split, and model settings.
- Predictions are not a substitute for advice or diagnosis from a qualified healthcare professional.
- Any real-world medical use would require suitable clinical validation, privacy safeguards, and expert oversight.

## Future Improvements
- Use cross-validation and tune model hyperparameters.
- Inspect feature importance or model explanations.
- Test calibration and choose thresholds based on the use case.
- Validate on an independent dataset.
- Add a FastAPI prediction endpoint and Docker setup if deployment is part of the completed work.

## Project Brief
The project scope and required algorithms/metrics are based on the provided *Capstone Project 2 Details – Classification* brief.

