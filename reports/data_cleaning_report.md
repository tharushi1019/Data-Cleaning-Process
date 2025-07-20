# Data Cleaning Report: Hotel Booking Demand Dataset

## Executive Summary

The **Hotel Booking Demand Dataset** from Kaggle contains detailed information on bookings from two types of hotels (City and Resort) between **July 2015 and August 2017**. This dataset includes 119,390 rows and 32 columns, capturing guest demographics, booking behavior, pricing, special requests, and cancellation data.

The primary objective of this data cleaning task was to prepare an **analysis-ready dataset** by addressing data quality issues such as **missing values, outliers, inconsistencies, and duplicates**. All cleaning operations were performed using **Python (pandas, NumPy, seaborn, matplotlib)**.

---

## Data Quality Assessment

### Original Dataset Characteristics

- **Total Records**: 119,390  
- **Total Columns**: 32  
- **Data Types**: Mixed (Numerical, Categorical, Dates)  
- **Missing Values Detected In**: `children`, `country`, `agent`, `company`  
- **Duplicate Rows**: 101  
- **Outliers Detected In**: `lead_time`, `adr`, `babies`, `adults`  
- **Inconsistent Data Examples**: Bookings with 0 guests, undefined/unknown categories  

### Identified Issues and Their Severity

| Issue                 | Columns Affected              | Severity | Notes                                      |
|----------------------|-------------------------------|----------|--------------------------------------------|
| Missing Values        | children, country, agent, company | High     | Affects customer details and booking behavior |
| Duplicates            | Entire rows                   | Medium   | 101 rows removed                            |
| Outliers              | lead_time, adr                | High     | Extreme values impact statistical modeling  |
| Inconsistencies       | adults=0 and children=0 and babies=0 | High     | Logically impossible bookings               |
| Categorical Noise     | 'undefined', 'Unknown' values | Medium   | Impacts classification and grouping         |

---

## Cleaning Methodology

### Missing Values

| Column     | Strategy               | Rationale                                 |
|------------|------------------------|-------------------------------------------|
| `children` | Replace with `0`       | Assume no children if not specified       |
| `country`  | Replace with mode      | Most bookings are local or repeat customers |
| `agent`    | Replace with `0`       | Implies no intermediary was involved      |
| `company`  | Replace with `0`       | Implies no company booking                |
| `total_guests` | Recalculated       | Ensures logical validity                  |

> **Missing value types:**
- `children`: **MCAR**
- `country`: **MAR**
- `agent`, `company`: **MNAR**

---

### Duplicate Handling

- Found **101 exact duplicate rows**
- **All duplicates removed**
- No near-duplicates were found (based on key features comparison)

---

### Outlier Detection & Treatment

| Column     | Method Used         | Treatment         |
|------------|---------------------|-------------------|
| `lead_time`, `adr` | IQR & Z-score | Outliers removed  |
| `babies`, `adults` | Logic check       | Values capped or cleaned |

---

### Inconsistency Fixes

- Replaced "Unknown" in `meal` with "Self-Catering"
- Combined and converted `arrival_date_year`, `month`, and `day` into valid `datetime` format
- Replaced invalid values (e.g., adults = 0, no guests) with logical assumptions or removed
- Created and validated `total_guests` column

---

### Integrity Checks

- Ensured **total_guests > 0**
- Validated all **arrival dates between July 2015 and August 2017**
- Ensured **categorical values** are from expected sets
- Checked that numeric values fall within realistic ranges

---

## Results and Impact

### Before vs. After Cleaning

| Metric             | Before      | After        |
|--------------------|-------------|--------------|
| Records            | 119,390     | ~118,000+    |
| Missing Values     | 4 columns   | 0 columns    |
| Duplicates         | 101 rows    | 0 rows       |
| Logical Errors     | 180+ rows   | 0            |
| Categorical Noise  | Multiple    | Cleaned      |

### Quality Improvements Achieved

- Ensured **data reliability**
- Removed invalid and illogical records
- Improved consistency in categorical and date formats
- Dataset is now ready for **exploratory analysis and modeling**

---

## Recommendations

### Future Data Collection Improvements

- Enforce **mandatory fields** for key attributes (e.g., country, agent)
- Implement **data validation rules** in the booking system
- Standardize categorical inputs to prevent typos or unknown values

### Ongoing Maintenance Suggestions

- Create a **reusable data cleaning pipeline**
- Use **automated data validation checks**
- Version control the dataset for transparency and auditability

---
