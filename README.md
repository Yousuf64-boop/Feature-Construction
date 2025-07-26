# Titanic Survival Prediction – Feature Construction and Analysis

This project focuses on feature construction, transformation, and exploratory data analysis (EDA) for the Titanic dataset. The primary goal is to prepare the dataset for machine learning by engineering meaningful features that improve prediction performance.

---

## 📌 Project Highlights

- Loaded and explored Titanic dataset.
- Performed feature extraction from complex fields (like `Name`).
- Cleaned missing values intelligently.
- Created new features like:
  - **Title** from passenger names
  - **FamilySize**
  - **IsAlone**
- Visualized survival rates across different engineered features.
- Prepared data for model training.

---

## 📊 Feature Engineering Techniques

- **Title Extraction**: Extracted titles (Mr, Miss, etc.) from the `Name` column and analyzed survival rates.
- **FamilySize**: Combined `SibSp` and `Parch` to compute total family size onboard.
- **IsAlone**: Derived from `FamilySize` to indicate passengers traveling alone.
- **Fare Binning**: Created categorical bins from continuous `Fare`.
- **Age Imputation**: Used group-based median values to fill missing ages.

---

## 📉 Example Analysis

```python
(df.groupby('Title')['Survived'].mean()).sort_values(ascending=False)
