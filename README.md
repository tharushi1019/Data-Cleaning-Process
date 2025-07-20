# 🧼 Hotel Booking Data Cleaning Project

This project focuses on cleaning and preparing the **Hotel Booking Demand Dataset** for further analysis or machine learning tasks. The cleaning process includes handling missing values, correcting data types, removing duplicates, renaming columns, and formatting for consistency.

---

## 📂 Project Structure

```

student\_name\_data\_cleaning/
├── data/
│   ├── hotel\_bookings.csv               # Original raw dataset
│   └── hotel\_bookings\_cleaned.csv       # Cleaned dataset
├── notebooks/
│   └── data\_cleaning\_process.ipynb      # Jupyter Notebook with step-by-step cleaning process
├── reports/
│   └── data\_cleaning\_report.md          # Markdown report with detailed explanation
├── scripts/
│   └── cleaning\_functions.py            # Python script with reusable cleaning functions (optional)
└── README.md                            # Project overview and instructions

````

---

## 📌 Dataset Info

- **Source:** [Hotel Booking Demand Dataset - Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)
- **Records:** 119,390 rows
- **Features:** 32 columns
- **File Format:** CSV

---

## ✅ Cleaning Summary

| Step                          | Description                                         |
|-------------------------------|-----------------------------------------------------|
| 🧹 Missing Value Handling     | Filled missing values in `children`, `country`, etc.|
| 🔄 Type Conversion            | Converted `is_canceled`, `lead_time`, etc. to `int` |
| 🧽 Column Cleaning            | Removed extra spaces and renamed columns            |
| 🧾 Duplicate Removal          | Dropped duplicate rows                              |
| 📊 Output                     | `hotel_bookings_cleaned.csv`                        |

---

## 📘 How to Use

1. Clone this repository:

   git clone https://github.com/yourusername/hotel-booking-data-cleaning.git
   cd hotel-booking-data-cleaning

2. Open the Jupyter Notebook:

   jupyter notebook notebooks/data_cleaning_process.ipynb

3. Review the `data/` folder for raw and cleaned datasets.

4. Read the full markdown report at:

   reports/data_cleaning_report.md


---

## 🛠️ Tools & Libraries

* Python 🐍
* Pandas 📊
* NumPy 🔢
* Jupyter Notebook 📓

---

## ✍️ Author

* **Name:** Tharushi
* **Degree:** BSc (Hons) in Information Technology
* **Institution:** Horizon Campus, Sri Lanka
* **Course:** Intelligent Systems & Data Analytics

---

## 📜 License

This project is open-source under the [MIT License](LICENSE).

---

## 📬 Contact

For feedback or collaboration, feel free to open an issue or reach out via GitHub!

---

