# Marketing Analytics: Predicting Engagement - What Drives Ad Performance?

This project aims to analyze and predict factors that drive **Ad Performance**, specifically conversion rates, using a dataset from a bank's marketing campaigns. The main objective is to identify the key factors that influence customer conversion and build a predictive model using a Decision Tree.

## Dataset

The dataset is sourced from [Bank Marketing Data](https://raw.githubusercontent.com/rajeevratan84/datascienceforbusiness/master/bank-full.csv), which contains details of marketing campaigns by a Portuguese bank.

- **Number of rows**: 45,211
- **Number of columns**: 17

The dataset includes features such as customer demographics, campaign information, and customer responses (whether they subscribed to a term deposit or not).

## Project Highlights

### Data Preprocessing:
- **Data Cleaning**:
  - Converted the target column (`y`) to a binary variable (`converted`), where `yes` is represented as `1` and `no` as `0`.
  
- **Feature Engineering**:
  - Encoded categorical variables such as `job`, `marital`, `housing`, `loan`, `education`, `contact`, and `poutcome` using one-hot encoding.

### Exploratory Data Analysis (EDA):
- Visualized the relationship between **average bank balance** and **conversion**.
- Analyzed **conversion rates** based on:
  - **Campaign contact frequency** (number of contacts with each customer)
  - **Job types** (e.g., admin, technician, etc.)
  
### Predictive Modeling:
- **Decision Tree Classifier**:
  - Built a **Decision Tree** to predict customer conversion based on various features.
  - Visualized the decision tree to better understand the splitting criteria.
  
- **Feature Importance**:
  - Used a custom method to evaluate feature importance by iteratively dropping each feature and measuring its impact on model performance.

## Key Results

- **Conversion Rate by Campaign**: The number of contacts with a customer significantly affects the conversion rate, with diminishing returns as the number of contacts increases.
  
- **Conversion Rate by Job**: Different professions had varying conversion rates, providing insights into customer segments more likely to convert.

- **Feature Importance**:
  - Features like **balance**, **campaign**, and **poutcome** (outcome of the previous marketing campaign) were critical in predicting customer conversions.

### Model Performance:
- The **Decision Tree** provided interpretable rules for identifying customers likely to convert.
  
## Visualizations:
- **Box Plots** and **Violin Plots** for conversion rates across different balance levels.
- **Bar Charts** for conversion rates by the number of campaign contacts and job type.
  
## How to Run

1. Clone the repository:
   
   git clone https://github.com/your-repo/marketing-analytics-ad-performance.git
   
2. Install dependencies:
   
   pip install pandas matplotlib seaborn scikit-learn graphviz
   
3. Load and run the notebook to perform the analysis and visualize the decision tree.

## Conclusion

This project provides a detailed analysis of factors that drive customer engagement in marketing campaigns, using a decision tree model to predict conversions. By identifying the key drivers of conversion, marketers can optimize their campaigns and focus efforts on the most promising customer segments.
