# Air Quality Data Analysis – NO₂ PDF Parameter Estimation

## 📌 Overview
This project analyzes air quality data focusing on **Nitrogen Dioxide (NO₂)** concentration levels.  
The goal is to transform the NO₂ data using a roll-number-based formula and estimate the parameters of the probability density function (PDF) for the transformed data.

---

## 📂 Dataset
- **File:** `data.csv`
- **Column Used:** `no2`
- Missing values are removed during preprocessing.

---

## 🔬 Methodology

### 1️⃣ Data Cleaning
- Load the dataset using Pandas.
- Extract the `no2` column.
- Remove null or empty entries.

### 2️⃣ Data Transformation
The original NO₂ values (`x`) are transformed into a new variable (`z`) using:

\[
z = x + a_r \cdot \sin(b_r \cdot x)
\]

**Roll Number:** `102303724`  
Derived constants:
- `a_r = 0.25`
- `b_r = 1.5`

---

### 3️⃣ Parameter Estimation
- Mean and variance of the transformed data (`z`) are computed.
- Using these values, the PDF parameters are estimated:
  - **Lambda (λ)**
  - **Mu (μ)**
  - **c**

---

## 📊 Results

| Parameter | Value |
|---------|-------|
| Lambda (λ) | 0.0014617052940514906 |
| Mu (μ) | 25.818063543032295 |
| c | 0.021570239817484047 |

---

## 📈 Visualization
The distribution and fitted curve are visualized and saved as:

