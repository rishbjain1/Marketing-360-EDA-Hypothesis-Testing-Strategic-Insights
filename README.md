# Data-Science

# Marketing Campaigns Analysis  

## **Project Overview**  
This project focuses on **exploratory data analysis (EDA)** and **hypothesis testing** to understand various factors affecting **customer acquisition** in marketing campaigns. The analysis covers customer demographics, purchasing behavior, and sales channels, aligning with the **four Ps of marketing**:  
- **People**: Customer demographics (age, education, income, marital status).  
- **Product**: Customer expenditures on various items like wine, fruits, and gold.  
- **Place**: Sales channels used by customers (web, catalog, in-store).  
- **Promotion**: Effectiveness of marketing campaigns.  

## **Objective**  
As a data scientist, the goal is to derive insights into customer behavior, test hypotheses, and visualize key trends that impact marketing strategies.  

---

## **Dataset Description**  
The dataset contains customer-level information, including:  
- **Demographics**: Age, birth year, education, marital status, income.  
- **Spending Data**: Amount spent on wine, fruits, meat, fish, sweets, and gold over two years.  
- **Shopping Preferences**: Number of purchases made via **website, catalog, or in-store**.  
- **Promotional Campaigns**: Response to different marketing campaigns.  

---

## **Steps to Perform**  

### **1. Data Import and Cleaning**  
- Verify the accurate import of key variables like `Dt_Customer` and `Income`.  
- Handle missing income values using **imputation**, considering that **customers with similar education and marital status** have comparable yearly incomes.  
- Clean and standardize **education** and **marital status** categories.  

### **2. Feature Engineering**  
- Create new variables:  
  - **Total Children**: `Kidhome + Teenhome`  
  - **Age**: `2025 - Year_Birth`  
  - **Total Spending**: Sum of all product expenditures  
  - **Total Purchases**: Sum of purchases across **web, catalog, and in-store** channels  

### **3. Exploratory Data Analysis (EDA)**  
- Generate **box plots** and **histograms** to understand variable distributions and detect outliers.  
- Apply **outlier treatment** where necessary.  
- Perform **ordinal and one-hot encoding** for categorical variables.  
- Generate a **correlation heatmap** to visualize relationships between variables.  

### **4. Hypothesis Testing**  
Conduct statistical tests to validate key business assumptions:  

#### **(a) Technological Proficiency vs. Shopping Preferences**  
- **H₀**: Older individuals do not significantly prefer in-store shopping over online.  
- **H₁**: Older individuals significantly prefer in-store shopping.  
- **Test Used**: Paired **Z-test** or **t-test**, depending on data normality.  

#### **(b) Parents and Online Shopping Convenience**  
- **H₀**: Customers with children do not prefer online shopping more than in-store.  
- **H₁**: Customers with children prefer online shopping due to time constraints.  
- **Test Used**: Paired **Z-test** or **t-test**.  

#### **(c) Cannibalization of Physical Stores**  
- **H₀**: Sales at physical stores are not significantly affected by online/catalog sales.  
- **H₁**: Sales at physical stores are significantly cannibalized by alternative distribution channels.  
- **Test Used**: Paired **Z-test** or **t-test**.  

#### **(d) U.S. vs. Global Purchase Volumes**  
- **H₀**: The U.S. does not significantly outperform the rest of the world in total purchases.  
- **H₁**: The U.S. significantly outperforms the rest of the world in total purchases.  
- **Test Used**: Two-sample **t-test**.  

### **5. Visual Data Analysis**  
- **(a) Best and Worst Performing Products**:  
  - Identify products with the **highest** and **lowest revenue** using bar charts.  
- **(b) Customer Age vs. Campaign Acceptance**:  
  - Analyze if **older customers** are more/less likely to accept the last campaign.  
- **(c) Country with Highest Campaign Acceptances**:  
  - Determine which country has the most **successful campaign responses**.  
- **(d) Number of Children at Home vs. Total Spending**:  
  - Investigate whether **households with more children** spend more or less.  
- **(e) Complaints vs. Education Level**:  
  - Examine the **educational background** of customers who **lodged complaints** in the past two years.  

---

## **Technologies Used**  
- **Programming Language**: Python  
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy.stats`  

## **How to Run the Project**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/marketing-campaign-analysis.git
