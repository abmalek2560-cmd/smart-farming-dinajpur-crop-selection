# Smart Farming for Dinajpur: A Machine Learning Approach to Regional Crop Selection

A data-driven machine learning solution designed to recommend optimal agricultural crops for Dinajpur, Bangladesh, based on regional soil chemistry and daily agroclimatological metrics.

---

## 📌 Project Overview
- **Target Region:** Dinajpur Sadar, Dinajpur, Bangladesh (Lat: 25.62° N, Lon: 88.64° E)
- **Objective:** Train a predictive model to select suitable crops for precision farming.
- **Model Used:** Random Forest Classifier
- **Model Accuracy:** **99.09%**

---

## 📊 Dataset & Features
The dataset (`dinajpur_crop_selection_dataset.csv`) combines 3 years (2023–2025) of daily climate parameters with regional soil attributes:

1. **Climatic Parameters (NASA POWER API):**
   - **`temperature`**: Daily average temperature (°C)
   - **`humidity`**: Relative humidity (%)
   - **`rainfall`**: Daily precipitation (mm)

2. **Soil Attributes (Derived from SRDI Guidelines):**
   - **`N` (Nitrogen):** 15 - 35 kg/ha
   - **`P` (Phosphorus):** 12 - 28 kg/ha
   - **`K` (Potassium):** 25 - 50 kg/ha
   - **`ph`:** 5.5 - 6.8 (Slightly acidic to neutral)

3. **Target Crop Labels:** `rice`, `wheat`, `maize`, `potato`, `litchi`, `jute`

---

## ⚙️ Methodology
1. **Data Acquisition:** Automated retrieval of 3-year daily climate parameters from NASA POWER API.
2. **Soil Attribute Integration:** Incorporating regional soil boundary values standard for Dinajpur.
3. **Rule-Based Mapping:** Assigning regional agronomic labels for training supervision.
4. **Model Training:** Fitting a Random Forest Classifier (80% train / 20% test split).
5. **Evaluation:** Validation through custom input testing and feature importance ranking.

---

## 📈 Key Results
- **Top Drivers:** **Temperature** and **Rainfall** are the most sensitive decision variables in crop selection.
- **Validation:** Successfully predicted winter-crop requirements (e.g., `WHEAT`) for custom winter temperature and rainfall testing values.
