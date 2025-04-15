# COMPARING CLASSIFIERS

This project explores and compares the performance of four classification algorithms on a real-world dataset, applying key steps in the data science lifecycle from business understanding and preprocessing to model evaluation and conclusions.

---

## Classifiers Used

The following four classification models were selected for comparison:

1. **Logistic Regression**  
2. **Decision Tree Classifier**  
3. **K-Nearest Neighbors (KNN)**  
4. **Support Vector Machine (SVM)**

Each classifier brings different assumptions and learning strategies to the task, offering a diverse perspective on model performance.

---

## Dataset

The analysis is based on a **bank marketing dataset** containing customer and campaign-related features aimed at predicting a binary target variable:  
**Did the customer subscribe to a term deposit?** (Yes/No)

This dataset is known to be **imbalanced**, with far fewer “Yes” cases than “No” cases.

---

## Business Challenge

The core challenge is to **predict customer subscription** based on their profile and interaction history.  
This involves:
- Dealing with **imbalanced classes**
- Extracting **relevant features**
- Ensuring models generalize beyond the training data

---

## Strategy & Workflow

### Understanding the Business Problem
- Focused on the **decision-making process** of targeting customers for a bank campaign.
- Evaluated the **cost and impact** of false positives vs. false negatives in a marketing setting.

### Data Cleaning
- Removed rows with **‘unknown’** values in key categorical features.
- Checked for missing values and irrelevant features.

### Feature Engineering
- Encoded categorical variables using **LabelEncoder** and **OneHotEncoder**
- Scaled numerical features with **StandardScaler**
- Created a **pipeline** to automate transformations for each model.

### Data Transformation
- Standardized input features for better model convergence.
- Ensured all models were tested under the same preprocessed data.

### Undersampling
- Applied **undersampling** to the majority class to address class imbalance.
- Ensured fair comparison by using the same balanced dataset across all models.

---

## Code Versions

### [`Improve_and_Compare_ver1.ipynb`](./Pablo_Rivera_practical_application_III.ipynb)
- Runs baseline models with default hyperparameters.
- Includes basic preprocessing, training, testing, and metric calculation.
- Provides initial comparison to identify strong and weak models.

### [`Improve_and_Compare_ver2.ipynb`](./Pablo%20Rivera%20practical%20application_III.ipynb)
- Enhances each model using **GridSearchCV** for hyperparameter tuning.
- Includes **training time**, **cross-validation accuracy**, and **F1-score** for deeper evaluation.
- Adds performance logging and saves model reports to `.csv` and `.txt` files.

---

## Results

In the [`Results`](./Results) folder, you can find:
- **Classification Reports** for each model tested
- Summaries of performance metrics
- Files named with timestamps and model identifiers (e.g., `ClassRepoLogisticRegression_Pablo_Rivera_20250414.txt`)

---

## Conclusions (Short Summary)

- **SVM and Logistic Regression** often performed best on precision and F1-score.
- **Decision Trees** were fast and interpretable but showed signs of overfitting.
- **KNN** struggled with high-dimensionality and class imbalance.
- Using **undersampling**, **feature scaling**, and **pipelines** was critical for fair and consistent comparisons.
- The **best model** depends on business needs (e.g., higher recall vs. higher precision).

---

##  Author

**Pablo Rivera**

---

## Python Requirements

You can install the required packages using:

```bash
pip install -r requirements.txt
