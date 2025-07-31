# 🌾 Smart Sprinkler System

This project is developed as part of **AICTE Internship Cycle 2**.

---

## 📌 Project Title

**Smart Sprinkler System**

---

## 🎯 Learning Objectives

* To develop an intelligent irrigation system that optimizes water usage in agriculture.
* To predict the optimal sprinkler status (ON/OFF) for different parcels based on real-time sensor data.
* To utilize machine learning techniques for accurate and efficient water management.

---

## 🎯 Goal

The primary goal is to create a smart irrigation solution that minimizes water wastage and enhances crop yield by providing precise control over sprinkler operations. This is achieved through a predictive model that determines when and where irrigation is needed based on environmental sensor readings.

---

## 🧰 Tools and Technology Used

* **Programming Language**: Python
* **Python Libraries**:

  * `pandas`: Data manipulation and analysis
  * `numpy`: Numerical operations
  * `matplotlib.pyplot`, `seaborn`: Data visualization
  * `scikit-learn (sklearn)`:

    * `train_test_split`: Data splitting
    * `RandomForestClassifier`: Base estimator
    * `MultiOutputClassifier`: Multi-label prediction
    * `MinMaxScaler`: Feature scaling
    * `classification_report`: Model evaluation
  * `joblib`: Model saving/loading
  * `streamlit`: Interactive web app development
* **Dataset**: `irrigation_machine.csv`
* **Trained Model**: `Farm_Irrigation_System.pkl`

---

## 🔄 Methodology

### 1. Data Loading

The dataset `irrigation_machine.csv` containing sensor readings and sprinkler statuses is loaded using pandas.

### 2. Data Preprocessing

* Removed irrelevant column `Unnamed: 0`
* Separated features (`sensor_0` to `sensor_19`) and targets (`parcel_0`, `parcel_1`, `parcel_2`)
* Scaled features using `MinMaxScaler` (0 to 1 range)

### 3. Data Splitting

* Applied `train_test_split` for evaluation

### 4. Model Training

* Used `RandomForestClassifier` as the base model
* Wrapped with `MultiOutputClassifier` for predicting all parcels
* Trained using the training set

### 5. Model Evaluation

* Used `classification_report` to evaluate precision, recall, F1-score

### 6. Model Saving

* Saved the trained model using `joblib`

### 7. Web App Development

* Created a **Streamlit** UI
* Users input 20 scaled sensor values
* Predictions are displayed for parcels 0, 1, and 2

---

## 🧠 Problem Statement

Traditional irrigation methods often lead to excessive water consumption due to inefficient scheduling and lack of precise water delivery. This results in significant water wastage, increased operational costs, and potential harm to crops from over or under-watering.

---

## 💡 Solution

The **Smart Sprinkler System** addresses inefficient irrigation through an intelligent, ML-based approach:

* **Water Conservation**: Minimizes unnecessary water usage
* **Optimized Resource Allocation**: Balances water usage across farm parcels
* **Improved Crop Health**: Prevents under/over-watering
* **Automation**: Eliminates manual intervention in irrigation

---

## 📸 Screenshot of Output

Insert a screenshot of the Streamlit app here:

**➡️ \[[Smart Sprinkler System_00.png](https://github.com/Sunny-commit/Smart_irrigation_AICTE_Shell/blob/main/Smart%20Sprinkler%20System_00.png)]**

*The image should include:*

* Sliders for sensors
* Predictions like:

  * "Sprinkler 0 (parcel\_0): ON"
  * "Sprinkler 1 (parcel\_1): OFF"

---

## ✅ Conclusion

The **Smart Sprinkler System** demonstrates the power of machine learning in enhancing modern agriculture. It optimizes irrigation practices, ensures sustainable water usage, and provides a scalable solution to agricultural water management.

By automating predictions and integrating an easy-to-use interface, this system empowers farmers to make smarter decisions, save resources, and grow healthier crops.
