
# California Housing Price Prediction

This project analyzes the **California housing dataset** and builds a **Linear Regression model** to predict house prices (`median_house_value`) based on various features.

## 📄 Dataset

The dataset is sourced from `housing.csv`, containing 20,640 entries and 10 columns, including both numerical and categorical features:

- `longitude`
- `latitude`
- `housing_median_age`
- `total_rooms`
- `total_bedrooms`
- `population`
- `households`
- `median_income`
- `median_house_value` (target)
- `ocean_proximity` (categorical)

After removing rows with missing values, the dataset contains 20,433 rows.

---

## 🛠️ Workflow

### 🔷 Data Preparation

✅ Missing values in `total_bedrooms` were dropped.  
✅ Data split into training (80%) and testing (20%) sets.  
✅ Log-transformations applied to skewed features:
- `total_rooms`, `total_bedrooms`, `population`, `households`.

✅ Created additional features:
- `bedroom_ratio = total_bedrooms / total_rooms`
- `household_rooms = total_rooms / households`

✅ One-hot encoding of the categorical feature `ocean_proximity`.

---

### 📊 Data Exploration

- Histograms of numerical features.
- Heatmaps of correlations between features.
- Scatter plot of `latitude` vs. `longitude` colored by `median_house_value`.

---

### 🤖 Model Training

- Model: **Linear Regression**
- Library: `scikit-learn`
- Trained on the training set with engineered features.

Performance on test set:
- **R² Score:** ~0.65

---

## 📈 Results

The model explains ~65% of the variance in house prices on the test set, which is reasonable given the simplicity of the linear regression model and the complexity of real estate markets.

---

## 📂 Files

- `housing.csv` — input dataset.
- `housing_analysis.ipynb` / `.py` — code file with full workflow.
- `README.md` — project documentation.

---

## 🚀 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 🔗 Notes

- Feature scaling was not explicitly done, as linear regression in `sklearn` can handle unscaled data reasonably.
- More complex models (e.g., Random Forest, Gradient Boosting) could potentially improve the R².

---

## 📬 Contact

For questions or feedback, feel free to reach out!

---
