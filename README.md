# 🌸 Task 1: Iris Flower Classification

[![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://dvdschj8gh2frlg2ndrjjt.streamlit.app/) 

**Oasis Infobyte — SIP (Student Internship Program)**  
* **Intern Name:** Rutuja Anil Koshti
* **Track:** Data Science  
* **Offer Letter ID:** OIB/N2/IP7748 
* **Repository:** `OIBSIP`  
* **Folder Name:** `DataScience-Task1-IrisFlowerClassification`  


---

## 📌 Project Overview
The Iris Flower Classification dataset is a classic benchmark in machine learning and pattern recognition. The objective of this project is to build an end-to-end classification pipeline that predicts the species of an iris flower based on its morphological measurements:
* **Sepal Length (cm)**
* **Sepal Width (cm)**
* **Petal Length (cm)**
* **Petal Width (cm)**

Target classes:
1. `Iris-setosa` (Class 0)
2. `Iris-versicolor` (Class 1)
3. `Iris-virginica` (Class 2)

---

## 📋 Feature Checklist Compliance

| Requirement from Task Card | Status | Implementation Details |
| :--- | :---: | :--- |
| **Load Dataset** | ✅ | Loaded directly via `sklearn.datasets.load_iris()` (no manual CSV download required). |
| **Exploratory Data Analysis (EDA)** | ✅ | Inspected `.shape`, `.info()`, `.describe()`, and confirmed zero missing/null values. |
| **Pairplot / Distribution Plots** | ✅ | Seaborn pairplot generated with KDE diagonals showing pairwise feature separations. |
| **Feature Boxplots** | ✅ | Boxplots for all 4 features comparing distributions across species. |
| **Feature Correlation Heatmap** | ✅ | Pearson correlation matrix with upper triangle mask. |
| **Feature Selection Discussion** | ✅ | Evaluated discriminative power of Petal measurements vs. Sepal measurements. |
| **Train/Test Split** | ✅ | 80/20 stratified split (`stratify=y`, `random_state=42`) preserving class ratios. |
| **Train $\ge$ 2 Classifiers** | ✅ | Trained **4 classifiers**: Logistic Regression, KNN ($k=5$), Decision Tree, and Random Forest. |
| **Model Evaluation** | ✅ | Accuracy, Precision, Recall, F1-Score, and Confusion Matrix for all models. |
| **Best Model Selection** | ✅ | Logistic Regression / KNN identified as top performers ($96.67\%$ test accuracy) with full justification. |
| **Clean Jupyter Notebook** | ✅ | Commented `.ipynb` notebook ready for execution and walkthrough. |

---

## 📊 Exploratory Data Analysis & Key Findings

### 1. Discriminative Feature Analysis
* **Petal Dimensions are Supreme Predictors:** `petal length` and `petal width` show near-perfect linear separation for **Iris-setosa** ($100\%$ precision/recall).
* **Versicolor vs. Virginica:** Sepal dimensions show slight overlap between Versicolor and Virginica; however, the combination of Petal Length ($> 4.8\text{ cm}$) and Petal Width ($> 1.6\text{ cm}$) cleanly differentiates Virginica.
* **Correlation:** Strong positive linear correlation ($r = 0.96$) exists between Petal Length and Petal Width.

### 2. Visualizations
* **Pairplot:** `images/pairplot.png`
* **Boxplots:** `images/boxplots.png`
* **Correlation Heatmap:** `images/correlation_heatmap.png`
* **Confusion Matrices:** `images/confusion_matrices.png`
* **Model Accuracy Comparison:** `images/model_comparison.png`

---

## 🏆 Model Performance & Comparison

| Classifier | Accuracy | Precision (Macro) | Recall (Macro) | F1-Score (Macro) | Misclassifications (/30) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Logistic Regression** | **96.67%** | **0.97** | **0.97** | **0.97** | **1** |
| **K-Nearest Neighbors ($k=5$)** | **96.67%** | **0.97** | **0.97** | **0.97** | **1** |
| **Random Forest (100 Trees)** | **96.67%** | **0.97** | **0.97** | **0.97** | **1** |
| **Decision Tree** | 93.33% | 0.93 | 0.93 | 0.93 | 2 |

### Final Model Selection Justification:
**Logistic Regression** is chosen as the optimal production model for this dataset:
1. **Calibration:** Outputs calibrated probabilities (`predict_proba`) indicating prediction confidence.
2. **Generalization:** Highly regularized linear boundary prevents overfitting on small sample sizes ($N=150$).
3. **Simplicity:** Extremely lightweight with sub-millisecond inference time.

---

## 🛠️ Project Structure

```text
OIBSIP/
└── DataScience-Task1-IrisFlowerClassification/
    ├── README.md
    ├── iris_classification.ipynb
    └── images/
        ├── pairplot.png
        ├── boxplots.png
        ├── correlation_heatmap.png
        ├── confusion_matrices.png
        └── model_comparison.png
```

---

🚀 How to Run Locally (VS Code)
1. Prerequisites
Python 3.8 or above
Visual Studio Code
Git

2. Clone the Repository
git clone YOUR_GITHUB_REPOSITORY_URL
cd YOUR_PROJECT_FOLDER
3. Create Virtual Environment
py -m venv venv
4. Activate Virtual Environment
.\venv\Scripts\Activate.ps1
5. Install Required Libraries
py -m pip install --upgrade pip
pip install -r requirements.txt
6. Run the Iris Flower Classification Application
streamlit run app.py
7. Open in Browser
http://localhost:8501
8. Run Machine Learning Training Script (Optional)
py train_and_predict.py
The application predicts Iris flower species using:

Logistic Regression

K-Nearest Neighbors

Random Forest

The Python training script also evaluates Decision Tree classification.

---

## 📹 Video Walkthrough & Submission Checklist
* [x] **Video Title Card (First 2 Seconds):**
  * **Full Name:** Rutuja Anil Koshti
  * **Domain Track:** Data Science
  * **Task Title:** Task 1: Iris Flower Classification
* [x] **Walkthrough:** Explaining dataset inspection, visualizations, model training, evaluation metrics, and sample inference.
* [x] **Peer Review:** Reviewed and commented on 2 fellow interns' video posts.
