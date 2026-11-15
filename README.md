# Healthcare-Analysis-and-Insights
## 1. Problem statement
- This project aims to analyze a comprehensive healthcare dataset comprising medical examinations, hospitalization details, and customer profiles to extract insights into patient health profiles, medical histories, and healthcare costs. By exploring relationships between various health metrics, identifying trends, and visualizing key patterns, we aim to deliver actionable insights to healthcare stakeholders for informed decision-making through rigorous data cleaning, transformation, exploration, and analysis.
  ## 2. Dataset Description
  - The data contains patient-level healthcare records for roughly 2,300 individuals, with each row representing one patient. It includes health measurements such as BMI and HbA1c, along with medical history indicators like heart issues, transplants, cancer history, and the number of major surgeries, plus smoking status.In addition, the dataset records healthcare charges for each patient, along with hospital tier, city tier, and state, which makes it suitable for analyzing how health conditions, lifestyle, and location relate to medical costs.
  ## 3. Data pre-processing
  ### Data cleaning
- In medical examination table "2" missing value with "?" has been found, in hospitalization details missing values was found in customer ID,Year,Month,Hospital tier, City tier and state ID.Missing values in month column was replaced by Sep and Year with 1993(average value).Missing values in smoker,hospital tier and city tier was replaced with Mode.Missing value in state ID repalced with "Unkown". Find and replace function was used in most of the cases.

### Data Transformation
- Text to column function was used to split the name column into 3 columns.
-  "No major surgeries" in the medical examination column was replaced by "0" using find and replace function.
-  Inconsistency in both heart issues and smoker column was corrected using "proper" function.
-  "IFS" funciton with formula" =IFS(B2<18.5,"Underweight",B2<25,"Normal Weight",B2<30,"Over Weight",B2>=30,"Obesity")" was used to categorize the weight status.
-  using "=IFS(D2<5.7,"Normal",D2<=6.4,"Prediabetes",D2>=6.5,"Diabetes")" formula "diabetes status" field was created.
-  "Concat" was used to merge the cells and form Date of brith column, and number format used to convert it into "DD-MM-YYYY" format.
-  Currency changed into "$" using number format.
  ## Exploratory Data Analysis
 - This interactive Excel dashboard analyzes a patient-level healthcare dataset of 2,335 patients. It explores how health conditions, lifestyle factors, and demographics relate to healthcare charges. The dashboard summarizes key metrics at the top and offers interactive slicers for filtering the visuals.

Key Metrics (KPI Cards)
Total Customers: 2,335 patients
Average BMI: 30.97
Average HbA1c: 6.58
Interactive Slicers
Weight Status: Normal Weight, Obesity, Over Weight, Underweight
Diabetes Status: Diabetes, Normal, Prediabetes

Both slicers update all connected charts and KPI cards at once, so users can focus on any patient segment.

### Visualizations

1. Healthcare Charges by Weight Status and Diabetes Status (Column Chart)
A clustered column chart showing total healthcare charges for each weight category, split by diabetes status. Obesity accounts for the highest total charges by a wide margin, followed by Normal Weight, Over Weight, and Underweight.

2. Number of Major Surgeries and Average HbA1c by Transplant History (Pie Chart)
Compares patients with and without a history of transplants on total major surgeries and average HbA1c. The split is roughly 50% / 50% in this view.

3. Cancer History among Smokers vs. Non-Smokers (Pie Chart)
Shows the distribution of cancer history among smokers and non-smokers. In the current view, 79% of patients have no cancer history and 21% do.

4. Average Charges by Hospital Tier and State (Column Chart)
Compares average healthcare charges across hospital tiers and states.


  
