# Personality and Interest Patterns Analysis

## 🎯 Objective
This project analyzes a dataset of personality traits and demographic attributes to predict personality types. The goal is to explore the data, preprocess it, and build a machine learning model for classification.

---

## Dataset
The dataset includes:
- **Demographics**: Age, Gender, Education
- **Personality Scores**: Introversion, Sensing, Thinking, Judging
- **Interest Category**: Type of interest (e.g., Sports, Arts, Technology)
- **Personality Type**: Personality category to be predicted (e.g., ENFP, INTP)

---

## Tasks Performed
1. **Data Preprocessing**:
   - Handled missing values and encoded categorical variables.
   - Normalized continuous personality scores.
2. **Exploratory Data Analysis (EDA)**:
   - Visualized distributions and correlations.
   - Created pair plots and heatmaps.
3. **Feature Engineering**:
   - Created new features (e.g., combined scores, age groups).
4. **Model Building**:
   - Trained and evaluated multiple models (e.g., Random Forest, Decision Trees).
   - Used cross-validation for hyperparameter tuning.
5. **Model Evaluation**:
   - Compared models using accuracy, F1 score, and confusion matrix.
   - Analyzed feature importances.

---

## Results

### Classification Report
The Random Forest model achieved the following performance:

| Personality Type | Precision | Recall | F1-Score | Support |
|------------------|-----------|--------|----------|---------|
| ENFJ             | 0.90      | 0.92   | 0.91     | 518     |
| ENFP             | 0.92      | 0.92   | 0.92     | 4191    |
| ENTJ             | 0.91      | 0.92   | 0.92     | 399     |
| ENTP             | 0.92      | 0.92   | 0.92     | 3113    |
| ESFJ             | 0.84      | 0.80   | 0.82     | 79      |
| ESFP             | 0.85      | 0.81   | 0.83     | 585     |
| ESTJ             | 0.86      | 0.80   | 0.83     | 54      |
| ESTP             | 0.84      | 0.83   | 0.84     | 411     |
| INFJ             | 0.90      | 0.86   | 0.88     | 397     |
| INFP             | 0.89      | 0.90   | 0.89     | 2929    |
| INTJ             | 0.89      | 0.89   | 0.89     | 267     |
| INTP             | 0.89      | 0.89   | 0.89     | 2107    |
| ISFJ             | 0.70      | 0.78   | 0.74     | 49      |
| ISFP             | 0.81      | 0.81   | 0.81     | 416     |
| ISTJ             | 0.81      | 0.73   | 0.77     | 30      |
| ISTP             | 0.83      | 0.78   | 0.80     | 301     |

- **Accuracy**: 0.90
- **Macro Avg**: Precision = 0.86, Recall = 0.85, F1-Score = 0.85
- **Weighted Avg**: Precision = 0.90, Recall = 0.90, F1-Score = 0.90

---

### Key Findings
1. **Most Predictive Features**:
   - **Introversion Score** and **Thinking Score** were the most influential features (both around 0.30 importance).
   - **Sensing Score** and **Judging Score** showed moderate importance (around 0.12-0.15).
   - Demographic features (Age, Gender, Education) had relatively low importance (below 0.05).
   - Interest categories (Sports, Technology, Others) showed minimal predictive power.

2. **Age Distribution**:
   - The dataset shows a **right-skewed age distribution**.
   - Majority of users are between **20-35 years old**.
   - Peak concentration around **25 years old**.
   - Fewer representations of users above **40 years old**.

3. **Personality Score Correlations**:
   - The correlation heatmap shows **very weak correlations** between different personality scores (all correlations < 0.01).
   - Each personality dimension appears to be **relatively independent** of others.

---

## Limitations
1. **Dataset Biases**:
   - **Age bias**: Strong representation of younger adults but limited data for older age groups.
   - Possible **sampling bias** due to uneven age distribution.

2. **Model Limitations**:
   - Heavy reliance on personality scores while demographic and interest features contribute minimally.
   - The weak correlations between personality scores might indicate potential **measurement issues** or **noise in the data**.

3. **Potential Challenges**:
   - The model might not perform well for **outlier age groups**.
   - Limited predictive power from interest categories suggests possible **missing important features**.
   - May not capture **complex interactions** between personality traits due to their independence.

4. **Generalizability Concerns**:
   - Results might not be representative of **all age groups**.
   - The model might be less effective for users with **non-typical personality patterns**.

---

## For Clone the repository:
   ```bash
   git clone https://github.com/Pranali-DA/Personality-and-Interest-Patterns-Analysis.git
