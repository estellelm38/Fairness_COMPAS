# Fairness Analysis on the COMPAS Dataset

Mahato Monimala
Long--Merle Estelle

## Project Structure

The project is divided into the following notebooks:

### 1. Data Preprocessing
- **Notebook**: `preprocessing.ipynb`
- **Description**: Loads the original COMPAS dataset, cleans and transforms the data, encodes categorical variables, and outputs a preprocessed CSV file (`compas-scores-two-years-preprocessed.csv`) used in some subsequent steps.

### 2. Exploratory Data Analysis (EDA)
- **Notebook**: `dataset_exploration.ipynb`
- **Description**: Provides visualizations and descriptive statistics to understand the distribution of features, correlations, and potential bias in the dataset (e.g., by race, gender, prior offenses).

### 3. Supervised Learning Classifiers
- **Notebook**: `Classifiers.ipynb`
- **Description**: Applies standard machine learning models including:
  - Logistic Regression
  - Random Forest Classifier
  - Support Vector Machines (SVM)
  Evaluation metrics include accuracy, precision, recall, and confusion matrices.

### 4. Fairness Analysis
- **Notebooks**:
  - `fairness_LR.ipynb`
  - `random_forest.ipynb` 
  - `FairML_RandomForest.ipynb`
  
- **Description**: Uses the [AIF360](https://github.com/IBM/AIF360) library to assess and mitigate algorithmic bias. Techniques include:
  - **Reweighing** (preprocessing)
  - **Reject Option Classification (ROC)** (postprocessing)
  
  Metrics evaluated:
  - Statistical Parity Difference
  - Disparate Impact
  - Equal Opportunity Difference (optional)

1. Clone the repository and set up the environment:
   ```bash
   git clone https://github.com/estellelm38/Fairness_COMPAS
   cd Fairness_COMPAS
   python3 -m venv .venv
   source .venv/bin/activate
