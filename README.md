# 🏥 ER Wait Time Analysis & Prediction

This project analyzes emergency room (ER) wait times using historical hospital data and builds a predictive model to estimate future wait times. The goal is to uncover operational inefficiencies and improve service delivery through data-driven insights.

---

## 📂 Dataset Summary

The dataset includes records of ER visits with timestamps, hospital details, patient urgency levels, and service time intervals. It also contains outcome variables such as *Total Wait Time (min)*.

---

## 🔍 Features in the Pipeline (with Rationale)

### 1. Facility Size (Beds)
- *Description:* Number of beds available in the hospital.
- *Why it's useful:* Larger facilities may have more resources but also more complex patient flows, which can affect wait time.

---

### 2. Nurse-to-Patient Ratio
- *Description:* Ratio of nursing staff to patients in the ER.
- *Why it's useful:* Higher ratios often lead to quicker triage and care, reducing wait times.

---

### 3. Specialist Availability
- *Description:* Number of medical specialists available at the time of visit.
- *Why it's useful:* Greater availability of specialists helps reduce treatment delays and patient bottlenecks.

---

### 4. Appointment Load
- *Description:* Number of scheduled appointments on the day of the ER visit.
- *Why it's useful:* Higher appointment volumes typically increase overall workload, which may lead to longer wait times.

---

### 5. Urgency Level (One-Hot Encoded)
- *Description:* Triage level of each patient (e.g., Critical, High, Medium, Low).
- *Why it's useful:* Critical patients receive priority, which affects how long non-critical patients wait.

---

### 6. Region (One-Hot Encoded)
- *Description:* Geographical region of the hospital.
- *Why it's useful:* Different regions may have varying policies, resources, and patient volumes, impacting wait times.

---

### 7. Day of Week (One-Hot Encoded)
- *Description:* Day the patient visited the ER.
- *Why it's useful:* ER volumes and staffing vary by day; for example, Mondays may see more patient inflow than weekends.

---

### 8. Registration to Triage
- *Description:* Time taken from patient registration to initial triage.
- *Why it's useful:* Reflects front desk and triage efficiency, which influences overall experience and delays.

---

### 9. Triage to Medical
- *Description:* Time between triage and the patient seeing a medical professional.
- *Why it's useful:* Helps identify bottlenecks in the care initiation process.

---

### 10. Hour and Month (Time-Based Features)
- *Description:* Extracted from visit timestamp.
- *Why it's useful:* Captures patterns like peak hours or seasonal demand (e.g., flu season or evening surges).

---

## 🧠 Model Summary

- *Model Used:* Linear Regression
- *Target Variable:* Total Wait Time (min)
- *Features:* Numeric, categorical (one-hot encoded), and engineered features as listed above.
- *Output:* Predicted wait time added as a new column in the dataset.

---

## 📊 Visualizations & Insights

The notebook includes a range of exploratory data visualizations such as:
- Distribution of wait times
- Comparisons by region, day of week, and urgency level
- Trends over time
- Correlation with hospital capacity and staffing

---

## 📤 Output

- Processed file: er_wait_time_processed.csv
- Contains all original data plus a new column: Predicted Wait Time (min)
- Developed an interactive dashboard to analyze patient wait times across departments, highlighting peak hours, bottlenecks, and delay patterns,
  Enabled data-driven insights for optimizing staffing and improving patient flow efficiency.
  This is the link to the PowerBI dashboard:[View Project Dashboard](https://app.powerbi.com/groups/me/reports/636f57d9-eb11-4287-a8f3-a59968f87fd2/26683d14cb6e721d2296?experience=power-bi)

---
