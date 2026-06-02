# 🐾 The Power of a Name: A/B Testing Animal Shelter Outcomes

**Author:** Hilal Ozkan
**Date:** June 2, 2026  
**Methodology:** PACE Framework (Plan, Analyze, Construct, Execute)

## 📌 Project Overview
This project investigates a highly actionable operational question for animal shelters: **Does assigning a name to an animal upon arrival significantly reduce its wait time for adoption?** By analyzing a real-world dataset from the Austin Animal Center, this project demonstrates the end-to-end data science lifecycle. It moves beyond basic statistical significance to uncover deeper operational realities, specifically addressing high cardinality in outcome types and identifying statistical phenomena like "Time Bias."

## 📊 The Dataset
* **Source:** [Austin Animal Center Outcomes](https://data.austintexas.gov/Health-and-Community-Services/Austin-Animal-Center-Outcomes/gsvs-ypi7/about_data)
* **Snapshot Date:** June 2, 2026
* **Scope:** To ensure an accurate A/B test without noise from alternative outcomes (e.g., transfers or euthanasias), the dataset was strictly filtered to include only successful **Adoptions**.

## 🛠️ Tech Stack & Skills Demonstrated
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, SciPy (Welch's T-Test), Matplotlib, Seaborn
* **Techniques:** Data Cleansing & Wrangling, Feature Engineering, Exploratory Data Analysis (EDA), A/B Testing, Business Intelligence & Storytelling.

## 🔍 Key Findings (The Two-Act Narrative)

### Act 1: The Core Operational Impact
For the vast majority of animals, having a name significantly accelerates the adoption process. 
* The **median length of stay** for named animals is notably shorter (253 days) compared to unnamed animals (299 days).
* An independent Welch's t-test confirmed this 46-day reduction in shelter time is statistically significant ($p < 0.05$).

### Act 2: Uncovering "Time Bias" (The Outlier Paradox)
While the median strongly favors named animals, the mathematical *mean* showed extreme right-skewness for the named group (animals staying 600+ days). Rather than indicating that names delay adoption, a deeper percentile analysis revealed **Time Bias**: Animals that are highly difficult to adopt stay in the shelter for extended periods. As they stay longer, it becomes inevitable that shelter staff will form bonds and eventually name them. Thus, the "Named" category naturally absorbs all extreme chronic cases.

## 💡 Business Recommendation
The data strongly advocates for a zero-cost operational intervention: **Shelter management should implement a standard operating procedure (SOP) to assign warm, temporary names to all incoming animals immediately upon intake.** Overriding "Unknown" or blank records creates a psychological anchor for potential adopters. In a shelter environment operating at capacity, saving a median of 46 days of resources (food, space, medical care and staff bandwidth) per adopted animal yields a massive return on investment for both animal welfare and operational efficiency.

## 🚀 How to Run the Project
1. Clone this repository.
2. Ensure you have the required Python libraries installed (`pip install pandas numpy scipy matplotlib seaborn`).
3. Open `ab_testing_shelter_naming_impact.ipynb` in Jupyter Notebook or JupyterLab to view the code, visualizations, and detailed analysis.
