# Iris Flower Classification

Machine-learning classification of iris flowers (Setosa, Versicolor, Virginica) from their sepal and petal measurements.

## What the notebook covers
- Exploratory data analysis: shape, dtypes, null check, descriptive statistics
- Visualisations: pairplot and box plots by species
- Feature selection discussion (petal length and petal width are the most discriminative)
- 80/20 stratified train/test split
- Four classifiers: Logistic Regression, K-Nearest Neighbours, Decision Tree, Random Forest
- Evaluation: accuracy, confusion matrix, classification report, 5-fold cross-validation
- Best model declared with justification (Random Forest by cross-validated accuracy, about 96.7%)

## Run it
```bash
pip install -r requirements.txt
jupyter notebook iris_classification.ipynb
```
The dataset is built into scikit-learn, so nothing needs to be downloaded.

## Tech stack
Python, pandas, scikit-learn, matplotlib, seaborn, Jupyter Notebook
