# 📊 Interactive Job Analytics Portal

This repository contains the documentation for a comprehensive job market analysis project, completed as part of an internship program. The project's goal was to transform a raw dataset into a professional, interactive Tableau dashboard.

---

### 🔗 Live Dashboard

The final, interactive dashboard is published on Tableau Public and can be viewed here:

**https://jobsanalytics.netlify.app/**

---

## 📋 Project Documentation

As per the requirements, this section details the process followed to create the final analytics portal.

### 1. Dataset Used
The project is based on the **"Job Descriptions Dataset"**, which contains over 1.6 million job postings. Key columns used for the analysis include:
* `Job_Title`, `Role`, `Experience`, `Qualifications`
* `Company`, `Company_Size`
* `Country`, `location`, `latitude`, `longitude`
* `Salary_Range`, `Work_Type`, `Preference`
* `Job_Posting_Date`, `Job_Portal`

### 2. Data Transformations & Cleaning
Before visualization, the raw data was processed to ensure quality and usability. The key transformations included:

* **Column Renaming:** Column names with spaces (e.g., "Job Title") were renamed to a code-friendly format (e.g., `Job_Title`).
* **Handling Missing Values:** Rows containing any null values were removed using `dropna()` to maintain a complete dataset for analysis.
* **Removing Duplicates:** Exact duplicate job postings were removed using `drop_duplicates()`.
* **Creating Calculated Fields:** In Tableau, new fields were created to parse raw text and make it usable for numerical filtering:
    * **`Experience (Years)`:** Extracted the minimum years of experience from text like "5 to 15 Years".
    * **`Salary (Min)`:** Converted salary text like "$59K-$99K" into a numerical value (e.g., 59000).
    * **`Continent`:** Grouped countries into continents for easier geographic filtering.

### 3. Key Features & KPIs Measured
The final Tableau dashboards are fully interactive and designed to measure several key performance indicators (KPIs) about the job market:

* **Top N Analysis:** Charts that calculate the top 5 most frequent job roles and top 10/20 hiring companies based on specific criteria.
* **Geographic Distribution:** An interactive map and heatmap showing the concentration of jobs by country and role.
* **Conditional Logic:** The dashboards allow for deep, multi-layered filtering to answer complex questions, such as finding jobs for a specific role in a non-Asian country with a salary over $50k.
* **Time-Based Analysis:** Filters that allow users to view job postings within specific date ranges.

---

## 🛠️ Technology Stack

* **Data Visualization & Analysis:** Tableau
* **Data Cleaning:** Python (Pandas)
* **Verification:** MySQL
