# 🛒 E-commerce Data Cleaning using Python

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python" />
  <img src="https://img.shields.io/badge/Pandas-2.x-green?logo=pandas" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter" />
  <img src="https://img.shields.io/badge/Status-Completed-success" />
</p>

---

## 📌 Project Overview

Data cleaning is the foundation of every successful data analysis project. This project focuses on transforming a raw e-commerce dataset into a clean, consistent, and analysis-ready dataset using **Python** and **Pandas**.

The cleaning process involved identifying missing values, checking for duplicate records, correcting data types, validating numerical fields, and preparing the dataset for further analysis and visualization.

---

## 🎯 Objectives

- Identify missing values
- Handle missing data appropriately
- Check and remove duplicate records
- Correct incorrect data types
- Validate numerical data
- Generate a clean dataset for analysis

---

## 📂 Dataset Information

- **Dataset:** E-commerce Orders Dataset
- **Total Records:** 1,200
- **Total Columns:** 14

### Dataset Features

| Column | Description |
|---------|-------------|
| OrderID | Unique identifier for each order |
| Date | Date on which the order was placed |
| CustomerID | Unique customer identifier |
| Product | Name of the purchased product |
| Quantity | Number of units purchased |
| UnitPrice | Price per unit |
| ShippingAddress | Customer delivery address |
| PaymentMethod | Mode of payment used |
| OrderStatus | Current order status |
| TrackingNumber | Shipment tracking number |
| ItemsInCart | Number of items in the cart |
| CouponCode | Applied discount coupon (if any) |
| ReferralSource | Customer acquisition source |
| TotalPrice | Total order amount |

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- Jupyter Notebook

---

# 📋 Project Workflow

### 1️⃣ Dataset Loading

- Imported the raw dataset using Pandas.
- Performed an initial inspection using:
  - `head()`
  - `shape`
  - `info()`
  - `describe()`

---

### 2️⃣ Missing Value Handling

- Identified missing values using:

```python
df.isnull().sum()
```

### Findings

- Missing values were found only in the **CouponCode** column.

### Action Taken

```python
df["CouponCode"] = df["CouponCode"].fillna("No Coupon")
```

Since not every customer uses a discount coupon, replacing missing values with **"No Coupon"** preserves the integrity of the dataset.

---

### 3️⃣ Duplicate Check

Checked duplicate records using:

```python
df.duplicated().sum()
```

### Findings

- No duplicate rows were found.

---

### 4️⃣ Data Type Correction

The **Date** column was originally stored as an **object** datatype.

Converted using:

```python
df["Date"] = pd.to_datetime(df["Date"])
```

This enables accurate date-based analysis and time-series operations.

---

### 5️⃣ Data Validation

Validated numerical columns including:

- Quantity
- UnitPrice
- ItemsInCart
- TotalPrice

Checked for:

- Negative values
- Zero values
- Invalid numerical entries

No incorrect numerical records were identified.

---

# 📊 Data Cleaning Summary

| Task | Status |
|------|--------|
| Missing Values Identified | ✅ |
| Missing Values Handled | ✅ |
| Duplicate Records Checked | ✅ |
| Data Types Corrected | ✅ |
| Numerical Data Validated | ✅ |
| Clean Dataset Generated | ✅ |

---

# 📸 Project Preview

### Dataset Overview

<img width="1625" height="372" alt="image" src="https://github.com/user-attachments/assets/bf9ac5d3-9884-4a98-9231-7567ee984926" />


```markdown
![Dataset Overview](Images/dataset_overview.png)
```

---

### Missing Values

<img width="502" height="420" alt="image" src="https://github.com/user-attachments/assets/61298ab4-8381-4356-aaab-86c98b818fc2" />


```markdown
![Missing Values](Images/missing_values.png)
```

---

### Data Type Conversion

<img width="550" height="496" alt="image" src="https://github.com/user-attachments/assets/37792740-49e9-49dd-976e-aa064f970f52" />


```markdown
![Data Types](Images/data_types.png)
```

---

### Cleaned Dataset

<img width="1176" height="873" alt="image" src="https://github.com/user-attachments/assets/4cb45d7c-85ec-46e4-81a2-ce8020423d80" />

```markdown
![Cleaned Dataset](Images/cleaned_dataset.png)
```

---

# 📈 Key Outcomes

- Successfully cleaned the raw dataset.
- Handled missing values without losing data.
- Verified the dataset contained no duplicate records.
- Corrected the Date column to datetime format.
- Validated numerical columns for data consistency.
- Prepared the dataset for Exploratory Data Analysis (EDA) and visualization.

---

# 💡 Skills Demonstrated

- Data Cleaning
- Data Preprocessing
- Missing Value Treatment
- Duplicate Detection
- Data Type Conversion
- Data Validation
- Pandas
- Python
- Jupyter Notebook

---

# 🚀 Future Scope

The cleaned dataset can be further used for:

- Exploratory Data Analysis (EDA)
- Customer Purchase Analysis
- Sales Trend Analysis
- Dashboard Development
- Business Intelligence Reporting
- Machine Learning Applications

---

# 📬 Connect With Me

### 👩‍💻 Pallavi Sandilya

- **LinkedIn:** https://www.linkedin.com/in/pallavi-sandilya-7a3839281
- **GitHub:** https://github.com/pallavisandilya4-hash

---

⭐ If you found this project useful, consider giving this repository a **Star**.
