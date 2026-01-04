🍽️ Zomato EDA – Exploratory Data Analysis
📌 Overview

This project performs Exploratory Data Analysis (EDA) on the Zomato dataset to understand restaurant distribution, ratings, countries of usage, online delivery availability, and city-level trends.
The focus of this notebook is data understanding, cleaning, grouping, and visualization, not machine learning.

🧱 Structure Followed in This Analysis

The notebook follows a clear and systematic EDA structure:

Handling missing values

Exploring numerical features

Exploring categorical features

Making observations from data and visualizations

🛠️ Libraries Used

Python

Pandas – data loading, cleaning, grouping

NumPy – numerical support

Matplotlib – visualizations

Seaborn – statistical plots

Jupyter Notebook

📂 Data Loading

Loaded the Zomato dataset using CSV (latin-1 encoding)

Inspected the dataset using:

.head()

.shape

.info()

.describe()

.dtypes

This helped understand:

Number of records and columns

Data types

Presence of missing values

1️⃣ Missing Value Analysis

Identified missing values using:

isnull().sum()

Filtered columns containing missing values

Visualized missing data using a heatmap

Observation:

Missing values were clearly visible in the Cuisines column.

2️⃣ Data Enrichment (Merging Datasets)

Imported an additional Excel file containing Country Codes

Merged the Zomato dataset with the country dataset using:

Country Code as the common key

Created a unified dataframe for further analysis

This step helped add country names to the main dataset.

3️⃣ Rating Analysis (Categorical + Numerical)

Grouped data by:

Rating text

Rating color

Aggregate rating

Calculated rating counts using groupby

Identified that ratings are categorical, such as:

Average

Good

Very Good

Excellent

Not Rated

Key Observations:

Rating ranges observed:

2.5–3.4

3.5–3.9

4.0–4.4

4.5–4.9

0.0 (Not Rated)

2148 records were marked as Not Rated

Total records: 9551

4️⃣ Country-wise Usage Analysis

Identified country usage using groupby and value_counts

Found top 3 countries where Zomato is used most:

India – 8652 records

USA – 434 records

UK – 80 records

Visualized top 3 countries using a pie chart

5️⃣ Rating Visualization

Created a bar plot between:

Aggregate rating

Rating count

Used rating colors as hue

Observation:

Ratings follow a roughly normal (Gaussian-like) distribution

Majority of ratings fall in the 2.5–3.4 range, categorized as Good

6️⃣ Not Rated (0 Rating) Analysis

Filtered records with Aggregate rating = 0

Analyzed country distribution of Not Rated restaurants

Observation:

India has the highest number of Not Rated restaurants

7️⃣ Currency Analysis

Grouped data by:

Country

Currency

Identified which currency is used in which country

8️⃣ Online Delivery Analysis

Filtered restaurants with online delivery = Yes

Analyzed country-wise availability

Observation:

Online delivery is available only in India and UAE

9️⃣ City-level Analysis

Checked for specific cities (e.g., Tamil Nadu – no records found)

Identified cities starting with “New”

Analyzed top 5 cities by restaurant count

Visualized city distribution using a pie chart

📊 Visualizations Used

Heatmap for missing values

Pie charts for:

Country usage

City distribution

Bar plots for:

Rating vs count with rating colors

🧠 Key Learnings

How to approach real-world datasets step by step

Importance of missing value analysis

Effective use of groupby for categorical insights

How visualizations help validate observations

Understanding how food platforms vary across countries and cities
