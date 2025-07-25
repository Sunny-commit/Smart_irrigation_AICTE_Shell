# Smart_irrigation_AICTE_Shell
This is an AICTE internship Cycle 2


# 🌾 Farm Irrigation System Prediction

This project uses a **machine learning model** to predict which parcels in a farm irrigation system should be activated based on sensor data. The aim is to **automate irrigation** and **optimize water usage**, making farming smarter and more sustainable.

---

## 📌 Project Overview

The notebook walks through the full ML pipeline — from data loading to training and saving the model. The goal is to use sensor input to **predict activation status for three irrigation zones**:

- `parcel_0`
- `parcel_1`
- `parcel_2`

---

## 📊 Dataset

🗂️ **File**: `irrigation_machine.csv`  
This dataset contains sensor readings (`sensor_0` to `sensor_19`) and labels (`parcel_0`, `parcel_1`, `parcel_2`), indicating whether each parcel should be irrigated.

| Type     | Columns                     |
|----------|-----------------------------|
| Features | `sensor_0` → `sensor_19`    |
| Labels   | `parcel_0`, `parcel_1`, `parcel_2` |

---

## 🔄 ML Pipeline Steps

1. **📥 Data Loading & Exploration**
   - Previewed the data
   - Checked column types and nulls

2. **🧹 Preprocessing**
   - Dropped irrelevant column(s)
   - Scaled sensor data using `MinMaxScaler`

3. **📂 Data Splitting**
   - Train-test split for model evaluation

4. **🏗️ Model Training**
   - Used `MultiOutputClassifier` with `RandomForestClassifier`
   - Fine-tuned parameters like `n_estimators`, `max_depth`

5. **🧪 Evaluation**
   - Generated classification report
   - Measured precision, recall, F1-score

6. **📈 Visualization**
   - Time series plots of pump activity
   - Parcel-specific irrigation visualizations

7. **💾 Model Saving**
   - Saved model using `joblib` for future use

---

## 🤖 Model Summary

- **Type**: Multi-label Classification
- **Architecture**: `MultiOutputClassifier(RandomForestClassifier)`
- **Goal**: Predict irrigation needs for 3 separate zones
---

## 🧑‍💻 How to Run the Project

```bash
# 1. Install dependencies
pip install pandas scikit-learn matplotlib seaborn joblib

# 2. Open the notebook
jupyter notebook Irrigation_System.ipynb
