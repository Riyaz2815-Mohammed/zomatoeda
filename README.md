# 🍽️ Zomato EDA – Exploratory Data Analysis

## 📌 Overview
This project performs **Exploratory Data Analysis (EDA)** on the Zomato dataset to understand restaurant distribution, ratings, country-wise usage, online delivery availability, and city-level trends.

The focus of this notebook is **data understanding, cleaning, grouping, and visualization**, not machine learning or prediction.

## 🧱 Structure Followed in This Analysis
The notebook follows a clear EDA structure:

1. Handling **missing values**  
2. Exploring **numerical features**  
3. Exploring **categorical features**  
4. Making **observations based on analysis and visualizations**

## 🛠️ Libraries Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

## 📂 Data Loading
- Loaded the Zomato dataset using CSV (`latin-1` encoding)
- Performed initial inspection using:
  - `.head()`
  - `.shape`
  - `.info()`
  - `.describe()`
  - `.dtypes`

This helped understand:
- Dataset size
- Column data types
- Presence of missing values

## 1️⃣ Missing Value Analysis
- Identified missing values using:
  - `isnull().sum()`
- Filtered columns containing missing values
- Visualized missing data using a **heatmap**

### Observation
- Missing values were mainly found in the **Cuisines** column.

## 2️⃣ Data Enrichment (Merging Datasets)
- Imported an additional Excel file containing **Country Codes**
- Merged both datasets using:
  - `Country Code` as the common key
- Created a unified dataset for further analysis

This step added **country names** to the main Zomato dataset.

## 3️⃣ Rating Analysis
- Grouped data by:
  - Rating text
  - Rating color
  - Aggregate rating
- Calculated rating counts using `groupby`

### Observations
- Ratings are categorical:
  - Average
  - Good
  - Very Good
  - Excellent
  - Not Rated
- Rating ranges observed:
  - 2.5–3.4
  - 3.5–3.9
  - 4.0–4.4
  - 4.5–4.9
  - 0.0 (Not Rated)
- **2148 records** are marked as *Not Rated*
- Total records: **9551**

## 4️⃣ Country-wise Usage Analysis
- Analyzed restaurant usage by country using `groupby` and `value_counts`

### Top 3 Countries
1. India – 8652  
2. United States – 434  
3. United Kingdom – 80  

- Visualized top countries using a **pie chart**

## 5️⃣ Rating Visualization
- Created a bar plot between:
  - Aggregate rating
  - Rating count
- Used rating color as hue

### Observation
- Ratings follow a **roughly normal (Gaussian-like) distribution**
- Most restaurants fall in the **2.5–3.4 (Good)** rating range

## 6️⃣ Not Rated (0 Rating) Analysis
- Filtered restaurants with `Aggregate rating = 0`
- Analyzed country-wise distribution

### Observation
- **India** has the highest number of *Not Rated* restaurants

## 7️⃣ Currency Analysis
- Grouped data by:
  - Country
  - Currency
- Identified which currency is used in each country

## 8️⃣ Online Delivery Analysis
- Filtered restaurants offering online delivery
- Analyzed country-wise availability

### Observation
- Online delivery is available **only in India and UAE**

## 9️⃣ City-level Analysis
- Checked for specific cities (e.g., Tamil Nadu – no records found)
- Identified cities starting with "New"
- Analyzed **top 5 cities** by restaurant count
- Visualized city distribution using a **pie chart**

## 📊 Visualizations Used
- Heatmap for missing values  
- Pie charts for:
  - Country-wise usage
  - City-wise distribution  
- Bar plots for rating analysis  

## 🧠 Key Learnings
- Practical approach to real-world data analysis  
- Importance of handling missing values  
- Effective use of `groupby` for categorical insights  
- How visualizations support data-driven observations  
- Understanding restaurant trends across countries and cities  

## 👤 Author
**Mohammed Riyaz A**  
GitHub: https://github.com/Riyaz2815-Mohammed
