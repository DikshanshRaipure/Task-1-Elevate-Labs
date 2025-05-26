# Task-1-Elevate-Labs
I used the netflix data for the task 1 as it is something I thought would be great to work with.

# Netflix Data Cleaning Project
This project demonstrates my approach to data cleaning and preprocessing using the Netflix Movies and TV Shows dataset. The goal was to prepare the raw data for further analysis by addressing missing values, duplicates, inconsistent formats, and incorrect data types.
---

##Each subheading is the explaination of each code cell in the jupyter file.

### 1. Loading the Data

I started by loading the dataset using Python and Pandas. This allowed me to efficiently handle and manipulate the data for cleaning.

---

### 2. Inspecting the Data

Before making any changes, I inspected the dataset to understand its structure and quality. I checked the first few rows, reviewed the data types, and counted missing values in each column:


This initial inspection helped me identify which columns had the most missing data and what types of cleaning would be necessary.

---

### 3. Handling Missing Values

Several columns had missing values, most notably `director`, `cast`, and `country`.

- For **`director`** and **`cast`**, which had a significant number of missing entries, I filled these with the placeholder `"No Data"`. This ensures that the dataset remains as complete as possible without losing valuable records.
  
- For **`country`**, I filled missing values with the most common country in the dataset. This approach helps maintain consistency and avoids introducing bias by arbitrarily assigning a country.
  
- For **`date_added`** and **`rating`**, since only a small number of rows were missing, I chose to drop those rows to maintain data integrity.

---

### 4. Removing Duplicates

Next, I checked for duplicate rows and removed any that were found. This step ensures that each record in the dataset is unique and prevents skewed analysis results.


---

### 5. Standardizing and Cleaning Data

To make the dataset easier to work with and more consistent, I standardized several aspects:

- **Column Names:** I converted all column names to lowercase and replaced spaces with underscores.
- **Date Formats:** I converted the `date_added` column to a proper datetime format for easier date-based analysis.
- **Data Types:** I ensured that columns like `release_year` were stored as integers.
- **Categorical Values:** I standardized values in columns such as `type` and `rating` for consistency in analysis.

---

### 6. Checking for Outliers and Inconsistencies

I reviewed columns such as `duration` for inconsistent formats (e.g., "90 min" vs. "1 Season"). While the main focus was on cleaning, I also noted these inconsistencies for future analysis, such as separating numeric duration from text labels.

---

### 7. Saving the Cleaned Dataset

After all cleaning steps were complete, I exported the cleaned DataFrame to a new CSV file:


---

## Summary of Changes

- Filled missing `director` and `cast` values with `"No Data"`.
- Filled missing `country` values with the most common country.
- Dropped rows missing `date_added` and `rating`.
- Standardized column names to lowercase with underscores.
- Converted `date_added` to datetime format.
- Removed duplicate rows.
- Checked and fixed data types for all columns.

---

## Conclusion

This cleaning process has prepared the Netflix dataset for robust analysis and visualization. The steps I took ensure that the data is consistent, complete, and ready for any future data science or analytics projects.

## Please Note - 
I explained the task thought process and gave my code to ChatGPT. This README file is by AI generated with minor tweaks after my foolproofing.
