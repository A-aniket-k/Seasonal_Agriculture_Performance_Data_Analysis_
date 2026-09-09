# Seasonal_Agriculture_Performance_Analysis_

An exploratory data analysis (EDA) project evaluating farm-level performance across seasonal cultivation cycles (Kharif, Rabi, and Zaid) using Python, Pandas, Matplotlib, and Seaborn.

---

## 📌 Project Overview
Agricultural productivity and farm economics are strongly influenced by seasonal climate patterns, resource availability, and management choices. This project analyzes a structured dataset of **4,000 farm records** across 28 distinct attributes to evaluate how environmental metrics, irrigation practices, and input investments translate into physical crop yields and net financial margins across seasons.

---

## 📊 Dataset Summary

* **Total Records:** 4,000 observations
* **Features:** 28 columns (environmental conditions, farm inputs, crop outputs, economics)

### Seasonal Distribution
* **Kharif:** 1,779 records (44.5%)
* **Rabi:** 1,627 records (40.7%)
* **Zaid:** 594 records (14.8%)

### Key Attributes Analyzed
* **Environmental:** Rainfall (mm), Average Temperature (°C), Humidity (%), Soil Moisture (%), Soil pH
* **Agronomic & Inputs:** Irrigation Method (Drip, Flood, Sprinkler, Rainfed), Fertilizer (kg/ha), Pesticide (L/ha)
* **Performance & Financials:** Yield (tonnes/ha), Production (tonnes), Total Cost (INR), Revenue (INR), Profit (INR), Water Efficiency (tonnes/1,000 m³)

---

## ⚙️ Data Preprocessing

* **Handling Missing Values:** Imputed missing entries in `Rainfall_mm` (48 rows), `Soil_Moisture_pct` (40 rows), and `Yield_Tonnes_Ha` (32 rows) using median imputation aligned with feature distributions.
* **Deduplication:** Verified zero duplicate rows across the complete 4,000-record dataset.
* **Outlier Assessment:** Applied the $1.5 \times \text{IQR}$ threshold to skewed metrics (`Yield_Tonnes_Ha`, `Profit_INR`, `Water_Efficiency_t_per_1000m3`). High-yield values were retained as valid biological outputs characteristic of high-biomass crops (Sugarcane).

---

## 🔍 Key Findings & Insights

* **Seasonal Yield Leadership:** Kharif produces the highest average agricultural yield at **5.63 tonnes/ha**, driven by monsoon rainfall (averaging ~849 mm). Rabi follows at **5.04 tonnes/ha**, while Zaid records the lowest output at **4.64 tonnes/ha** due to elevated temperatures (>31°C) and limited moisture.
* **Seasonal Financial Disparities:** Kharif generates an average net profit of **₹1.78 Lakhs**, whereas Zaid registers an average net loss of **-₹24,804**. Median profit across all cycles hovers near the break-even line (₹0), reflecting tight baseline operational margins.
* **Crop-Specific Dynamics:** Sugarcane drives total production volume (averaging 38–53 tonnes/ha) and overall profitability. Staple grains (Wheat, Rice, Maize) yield between 1.7 and 3.0 tonnes/ha but regularly show negative net returns due to steep input and irrigation expenditures.
* **Irrigation & Resource Efficiency:** Drip irrigation preserves positive net profit margins across every season. Conversely, Flood irrigation represents the largest share of records and peak water demand without generating commensurate yield improvements, depressing margins during dry cycles.
* **Correlation Dynamics:** Land area shows a near-perfect linear correlation with total production volume ($r \approx 0.99$). Crop yield demonstrates an extremely weak direct correlation with net profit, underscoring that gross biomass gains do not ensure financial returns without strict input cost discipline.

---

## 💡 Recommendations

* **Input Cost Optimization for Grains:** Rationalize fertilizer and pesticide application rates for Rice, Wheat, and Maize to bring per-hectare operating costs below market realization levels.
* **Crop Re-evaluation in Zaid:** Restrict high-water crops during Zaid unless supported by precision micro-irrigation; substitute with short-duration pulses or drought-resilient alternatives.
* **Transition to Micro-Irrigation:** Expand adoption of Drip and Sprinkler systems over Flood irrigation to curtail energy and water expenses during dry growing seasons.
* **Targeted Pest Management:** Prioritize preventative protection schedules during the high-humidity Kharif cycle to counter its elevated pest risk index (~54.5%).

---

## 🛠️ Tech Stack & Libraries

* **Language:** Python 3
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Google Colab
* **Version Control:** Git & GitHub

## 📂 Repository Structure
```text
├── Seasonal__Agriculture__Performance__Analysis_.ipynb   # Complete analysis notebook with executed visualizations
├── seasonal_agriculture_performance_dataset.csv          # Farm-level dataset (4,000 records, 28 attributes)
├── VOIS_Major_Project_PPT_Submission_Template.pptx       # Presentation deck summarizing methodology & findings
├── Major Project_Seasonal Agriculture Performance Analysis..pdf # Project brief and guidelines
└── README.md                                             # Project overview and summary documentation


