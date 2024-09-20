

---

# Analysis of Mouse Study Data

This project focuses on analyzing a dataset from a study involving various drug regimens tested on mice. The analysis aims to explore tumor volume trends, summarize key statistics, and generate visualizations to identify any patterns or relationships in the data. Below is a detailed overview of the steps followed and insights generated from the data.

---

## 1. **Prepare the Data**

### Steps:
1. **Import dependencies and load data**: 
   - Imported all necessary Python libraries and loaded mouse data from CSV files into pandas DataFrames.
   
2. **Merge the data**: 
   - Merged the mouse data with study results on the "Mouse ID" column into a single DataFrame.

3. **Data validation**:
   - Identified the number of unique Mouse IDs in the dataset.
   - Checked for duplicate Mouse IDs and removed any duplicate rows from the dataset.
   - Verified the data cleaning process by confirming the correct number of unique Mouse IDs.

---

## 2. **Generate Summary Statistics**

Two approaches were used to generate the following statistics for each drug regimen: Mean, Median, Variance, Standard Deviation, and Standard Error of the Mean (SEM).

### Method 1: Individual Calculation
- Grouped the DataFrame by drug regimen.
- Calculated each of the following for tumor volume:
  - Mean
  - Median
  - Variance
  - Standard Deviation
  - SEM
- Concatenated the five calculated statistics into a single summary DataFrame.

### Method 2: Aggregation
- Used the `aggregate` method to calculate all summary statistics for each drug regimen in a single line of code.

---

## 3. **Create Bar Charts and Pie Charts**

### Bar Charts:
- Generated a bar chart displaying the total number of timepoints for all the mice tested, grouped by drug regimen. 
- This was done using two methods:
  - With pandas' built-in plotting functions.
  - Using `matplotlib`'s `pyplot` module.

### Pie Charts:
- Created a pie chart showing the percentage distribution of male vs. female mice in the study.
- This was also accomplished using two methods:
  - With pandas' plotting functions.
  - Using `matplotlib`'s `pyplot` module.

---

## 4. **Calculate Quartiles, Identify Outliers, and Create a Box Plot**

### Steps:
1. **Select top drug regimens**:
   - Focused on the four most promising drug regimens: Capomulin, Ramicane, Infubinol, and Ceftamin.
   - Created a DataFrame containing the final tumor volume for each mouse under these treatments.
   
2. **Quartile and outlier calculation**:
   - For each drug regimen, calculated the quartiles, interquartile range (IQR), and upper/lower bounds.
   - Identified any outliers in the tumor volume data for each regimen.

3. **Box Plot**:
   - Generated a box plot to visualize the distribution of final tumor volumes across the four drug regimens.

---

## 5. **Create Line Plot and Scatter Plot**

### Line Plot:
- Selected a specific mouse treated with Capomulin (the one with the most timepoints) and generated a line plot showing tumor volume over time.
- The line plot revealed a clear downward trend in tumor volume as treatment continued.

### Scatter Plot:
- Created a scatter plot to visualize the relationship between average tumor volume and mouse weight for mice treated with Capomulin.
- This was done by calculating the average tumor volume and weight for each mouse using pandas' `groupby` and `aggregate` functions.

---

## 6. **Calculate Correlation and Linear Regression**

### Correlation:
- Calculated the correlation coefficient between average tumor volume and weight for mice treated with Capomulin. 
- The correlation was **0.84**, indicating a strong positive relationship between mouse weight and tumor volume.

### Linear Regression:
- Performed linear regression on the scatter plot to further visualize this correlation.
- The regression line helped illustrate the positive relationship between mouse weight and tumor volume.

---

## Conclusion

-The drug seems to be less effective when the mouse weighs more.
-The effectiveness of Campomulin seems to be comparable to Ramicane and is significantly more effecitve than Infubinol and Ceftamine based on the box plots.
- Out of the four drugs I analyzed, Campomulin and Ramicane were the most effective at decreasing tumor size. The least effective were the other two drugs which were Infubinol and Ceftamin 

---


