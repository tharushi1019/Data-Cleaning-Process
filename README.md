# 🧹 Hotel Booking Dataset - Data Cleaning Project

This repository contains a complete data cleaning pipeline for the Hotel Booking dataset using Python and Jupyter Notebook. It includes:

- 📂 Raw and Cleaned Datasets  
- 📝 Jupyter Notebook with step-by-step cleaning process  
- 📄 Markdown Report summarizing all cleaning tasks  

---

## 📁 Project Structure

```

student\_name\_data\_cleaning/
├── data/
│   ├── hotel\_bookings.csv               # Original dataset
│   └── hotel\_bookings\_cleaned.csv       # Cleaned dataset
├── notebooks/
│   └── data\_cleaning\_process.ipynb      # Jupyter notebook with cleaning process
├── reports/
│   └── data\_cleaning\_report.md          # Summary report (Markdown version)
└── scripts/
└── cleaning\_functions.py            # Optional Python script (if any)

````

---

## 📊 Dataset Info

- **Source:** [Kaggle - Hotel Booking Demand Dataset](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)
- **Rows:** ~119,000  
- **Columns:** 32  
- **Features include:** hotel type, booking date, customer type, cancellations, stays, prices, etc.

---

## ✅ Cleaning Tasks Performed

- Removed irrelevant columns  
- Renamed ambiguous column names  
- Handled missing data:
  - Replaced null values with appropriate defaults
- Fixed data types (e.g., date columns)  
- Removed duplicates  
- Normalized inconsistent values (e.g., replacing `NULL`, `Na`, etc.)

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/hotel-booking-data-cleaning.git
   cd hotel-booking-data-cleaning
````

2. Install required libraries (optional):

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

3. Open and run the notebook:

   ```bash
   jupyter notebook notebooks/data_cleaning_process.ipynb
   ```

---

## 📌 Author

* 👩‍💻 Tharushi (Undergraduate, BSc (Hons) in Information Technology)

---

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).

---

