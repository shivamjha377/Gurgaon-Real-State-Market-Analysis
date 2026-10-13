# Gurgaon Real Estate Market Analysis 🏙️

## 📌 Project Overview

This project focuses on analyzing the residential real estate market in Gurgaon using Python, Pandas, Matplotlib, and Seaborn.

The objective is to explore property prices, localities, property sizes, BHK configurations, RERA approvals, construction status, and builders to understand pricing patterns and identify factors associated with property costs.

The project involves **data cleaning, data preprocessing, exploratory data analysis (EDA), and data visualization** to extract meaningful insights from real estate data.

## 🎯 Project Objectives

- Clean and prepare raw real estate data for analysis.
- Identify the costliest property in the dataset.
- Compare average property prices across different localities.
- Find localities with the highest average price per square foot.
- Compare ready-to-move and under-construction properties.
- Analyze the relationship between RERA approval and property prices.
- Investigate the relationship between property area, price, and price per square foot.
- Compare pricing across BHK configurations and property types.
- Identify builders with the highest average price per square foot.

## 🛠️ Technologies Used

- **Python** – Data analysis and programming.
- **Pandas** – Data cleaning, transformation, grouping, and aggregation.
- **Matplotlib** – Data visualization.
- **Seaborn** – Statistical visualization and scatter plots.
- **Jupyter Notebook / Python IDE** – Code development and analysis.

## 📂 Project Structure

```text
Gurgaon-Real-Estate-Analysis/
│
├── data.csv          # Raw real estate dataset
├── analysis.py       # Python analysis script
└── README.md         # Project documentation
```

*Note: Update the script filename in this structure if your Python file has a different name.*

## 🧹 Data Cleaning and Preparation

Before performing the analysis, I prepared the dataset through the following steps:

1. **Column name standardization:** Removed leading and trailing spaces, converted column names to lowercase, and replaced spaces with underscores.
2. **Numeric data conversion:** Removed commas from `price`, `area`, and `rate_per_sqft` columns and converted them into numeric data types.
3. **Categorical data cleaning:** Removed unnecessary spaces and standardized the text values in `status` and `flat_type`.
4. **RERA approval transformation:** Converted RERA approval descriptions into Boolean values (`True` and `False`) for easier analysis.
5. **Duplicate removal:** Removed duplicate records to reduce repeated entries in the dataset.
6. **Exploratory analysis:** Used grouping, aggregation, conditional filtering, and scatter plots to investigate real estate pricing patterns.

## 🔍 Business Questions Answered

The project investigates the following 10 business questions:

### 1. Which is the costliest flat in the dataset?

Identified the property with the maximum listed price using the `idxmax()` function. The analysis extracts its BHK configuration, locality, price, and society name.

### 2. Which locality has the highest average property price?

Grouped properties by locality and calculated their average prices to identify the locality with the highest mean property price.

### 3. Which locality has the highest average price per square foot?

Calculated the average `rate_per_sqft` for each locality and identified the locality with the highest average rate.

### 4. Do ready-to-move properties cost more than under-construction properties?

Compared the average prices of ready-to-move and under-construction properties to determine which category has the higher average listed price.

### 5. Do RERA-approved properties command a price premium?

Compared the average listed prices of RERA-approved and non-RERA-approved properties to investigate whether approval status is associated with higher prices.

### 6. How does property area impact the total price?

Used a scatter plot to examine the relationship between property area and total price and explore whether larger properties tend to have higher listed prices.

### 7. Which BHK configuration has the highest average price per square foot?

Grouped properties by `bhk_count` and compared their average price per square foot to identify the configuration with the highest mean rate.

### 8. Which property type has the highest average price per square foot?

Compared average price-per-square-foot rates across different `flat_type` categories to identify the highest-priced category by this metric.

### 9. Do certain builders price their properties higher?

Grouped properties by `company_name`, calculated average price per square foot, sorted the results in descending order, and displayed the top five builders by this measure.

### 10. Are larger homes more expensive per square foot?

Created a scatter plot with property area on the X-axis and price per square foot on the Y-axis to examine the relationship between property size and unit pricing.

## 📊 Data Visualization

The project uses Seaborn scatter plots to explore relationships between key variables.

**Visualization 1: Area vs. Total Price**

```python
sns.scatterplot(data=df, x='area', y='price')
plt.show()
```

Purpose: To examine how the total listed price varies with property area.

**Visualization 2: Area vs. Price per Square Foot**

```python
sns.scatterplot(data=df, x='area', y='rate_per_sqft')
plt.show()
```

Purpose: To investigate whether property size is associated with differences in price per square foot.

## 📈 Key Analytical Techniques

- Data cleaning and preprocessing
- Duplicate record removal
- Data type conversion
- Boolean mapping
- Grouping and aggregation using `groupby()`
- Maximum value identification using `idxmax()`
- Sorting and ranking using `sort_values()`
- Conditional filtering
- Mean and average price comparisons
- Exploratory data analysis
- Scatter plot visualization

## 💡 Key Learnings

Through this project, I gained practical experience in:

- Working with real-world datasets containing numeric and categorical data.
- Cleaning inconsistent data and preparing it for analysis.
- Using Pandas to answer business-oriented questions.
- Comparing real estate pricing across locations, builders, and property categories.
- Creating visualizations to investigate relationships between variables.
- Translating raw data into insights that can support property market research.

## 🚀 Future Improvements

- Handle missing values and invalid records systematically.
- Add correlation analysis to investigate relationships between numeric variables.
- Create locality-wise and builder-wise comparison charts.
- Analyze median prices alongside averages to reduce the influence of outliers.
- Build an interactive dashboard using Power BI, Tableau, or Plotly.
- Develop a property price prediction model using machine learning.
- Add more detailed geographical and property-specific analysis.

## ⚠️ Limitations

- Findings are based on the dataset provided and may not represent the entire Gurgaon real estate market.
- Average prices can be influenced by unusually expensive or inexpensive properties.
- Observed relationships do not establish causation.
- The analysis does not independently verify property listings, transaction prices, or RERA registration details.
- Missing values and outliers should be investigated before drawing final conclusions.

## 👨‍💻 Author

**Shivam Kumar**

Aspiring Data Analyst | Python | Pandas | Exploratory Data Analysis

---

⭐ If you find this project useful, feel free to explore the code and share your feedback.
