# Healthcare-Analysis-and-Insights
## 1. Problem statement
- This project aims to analyze a comprehensive healthcare dataset comprising medical examinations, hospitalization details, and customer profiles to extract insights into patient health profiles, medical histories, and healthcare costs. By exploring relationships between various health metrics, identifying trends, and visualizing key patterns, we aim to deliver actionable insights to healthcare stakeholders for informed decision-making through rigorous data cleaning, transformation, exploration, and analysis.
  ## 2. Dataset Description
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
