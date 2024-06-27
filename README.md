# Customer Segmentation Dashboard

### Dashboard Link : https://drive.google.com/file/d/1J6i97Nobunew1oF2ZXYJK-qgyyADeO9J/view?usp=drive_link

### Problem Statement

The provided Power BI dashboard aims to segment and analyze customer data for an insurance company. This analysis helps the company understand customer demographics, preferences, and behaviors to tailor services, improve customer satisfaction, and identify potential areas for business growth.

### Steps to Create the Dashboard

#### Step 1: Load Data into Power BI Desktop
- Import the dataset (CSV files provided) into Power BI Desktop.

#### Step 2: Open Power Query Editor
- In Power BI Desktop, open the Power Query Editor to clean and transform the data.
- In the View tab under Data preview, enable "Column distribution," "Column quality," and "Column profile" options.

#### Step 3: Data Profiling
- Ensure column profiling is based on the entire dataset to get a complete view of data quality and distribution.
- Check for errors, empty values, and inconsistencies in the data.

#### Step 4: Data Cleaning and Transformation
- Handle any missing or erroneous data appropriately.
- For instance, if there are null values in critical columns like "Income Level" or "Coverage Amount," decide how to handle these (e.g., imputing values, removing rows).

#### Step 5: Create Calculated Columns and Measures
- *Age Group Calculation*:
  DAX
  Age Group = 
  IF(
      [Age] <= 25, "0-25",
      IF(
          [Age] <= 50, "26-50",
          IF(
              [Age] <= 75, "51-75",
              "76-100"
          )
      )
  )
  
- *Count of Customers*:
  DAX
  Total Customers = COUNT(customer_segmentation_data[Customer ID])
  
- *Percentage of Customers*:
  DAX
  % Customers = DIVIDE(COUNT(customer_segmentation_data[Customer ID]), CALCULATE(COUNT(customer_segmentation_data[Customer ID]), ALL(customer_segmentation_data))) * 100
  

#### Step 6: Import and Create Custom Visuals
1. *Infographic Visuals*:
   - Import infographic visuals from the Power BI marketplace.
   - Use these visuals to create more engaging and insightful representations of customer demographics and behaviors.
   - For example, use icons or images to represent different genders, education levels, and occupations.


  ![infographic](https://github.com/Shru6104/PowerBI-Dashboard-Project/assets/121664722/39d1bb7d-3375-441b-9ad3-e6d1bee2ce97)



#### Step 7: Create Visualizations
- *Demographic Breakdown*: Create bar charts and pie charts to show the distribution of customers by gender, marital status, education level, and geographic information.
- *Income and Coverage Analysis*: Use line charts and tables to display the sum of income levels by age and coverage amounts by different policies.
- *Behavioral Data*: Create visuals to show customer preferences and behaviors, such as preferred communication channels and interaction history.
- *Policy Type Analysis*: Use matrix visuals to show the count of policy types by marital status and customer ID.

#### Step 8: Add Visual Filters (Slicers)
- Add slicers for fields like "Gender," "Education Level," "Policy Type," and "Geographic Information" to allow users to filter the data dynamically. 

*Snapshot of slicers*

![cs slicers](https://github.com/Shru6104/PowerBI-Dashboard-Project/assets/121664722/9087718f-a346-4c50-9aee-4b2eec6faae7)

#### Step 9: Design the Report
- Use themes and design elements to make the dashboard visually appealing and easy to navigate.
- Add text boxes for titles, descriptions, and insights.

#### Step 10: Publish the Report
- Once the dashboard is finalized, publish it to the Power BI Service for wider access and sharing.

### Insights from the Dashboard

#### Demographics
1. *Gender Distribution*:
   - Visualize the count of customers by gender using a bar chart or infographic visual.
   
2. *Marital Status*:
   - Display the distribution of marital status using a pie chart or a bar chart.

3. *Education Level*:
   - Show the count of customers by education level using a bar chart or infographic visual.

4. *Geographic Information*:
   - Highlight customer distribution across different geographic locations using a map visual.

#### Financial Metrics
1. *Income Level by Age*:
   - Use a line chart to show how income levels vary across different age groups.

2. *Coverage Amounts*:
   - Display the total coverage amounts for different policies using a table or a bar chart.

#### Customer Preferences and Behaviors
1. *Communication Channels*:
   - Visualize preferred communication channels (e.g., Email, Phone, In-Person Meeting) using a bar chart or infographic visual.

2. *Interaction History*:
   - Show the interaction history, such as the number of in-person meetings, calls, and emails using a timeline visual.

#### Policy Analysis
1. *Policy Types by Marital Status*:
   - Use a matrix visual to show the count of policy types segmented by marital status and customer ID.

2. *Product Ownership*:
   - Display the number of insurance products owned by customers using a bar chart or infographic visual.

# Dashboard Snapshot

 
![customer segmentation dashboard](https://github.com/Shru6104/PowerBI-Dashboard-Project/assets/121664722/923bb0da-c367-4056-94be-79105a5bbaf2)

