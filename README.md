# Flipkart Customer Service Satisfaction

#### **Objective:**
The aim of this project is to develop a classification model to predict customer satisfaction scores for Flipkart. 
This predictive model will help the company identify areas for improvement in customer experience and optimize their marketing and service strategies, 
ultimately enhancing customer retention and satisfaction.

#### **Dataset Overview:**
The dataset comprises 20 columns, with several features showing a strong correlation to customer behavior. 
Key customer-related variables includes `Order_ID`, `Order_date_time`, `Customer_City`, `Item_Price`, `Channel_Name`, and `Customer_Remarks`. 
Additionally, key operational variables include `Issue_Responded_at`, `Issue_Responded`, `Survey_Response_Date`, 
`Product_Category`, `Agent_Name`, `Supervisor`, `Manager`, `Agent_Shift`, and `Sub_Category`. 
The target variable is the `CSAT Score`, which ranges from 1 to 5, indicating customer satisfaction—higher scores reflect greater satisfaction.

#### **Data Manipulation:**
The date variables were converted from object type to datetime format for improved processing. 
The Connected_Handling_Time column was removed due to having 99% of its values as null. Additionally, any rows with null values in the `Order_ID` column were eliminated. 
To address missing data, null values in categorical columns, including `Customer_City`, `Customer_Remarks`, and `Product_Category`, as well as in numeric columns like `Item_Price`,
`Issue_Reported_at`, and `Issue_Responded`, were filled appropriately.

#### **Exploratory Data Analysis (EDA):**
The EDA phase involved a comprehensive exploration of the dataset to uncover trends, patterns and relationships that could inform the model-building process.

#### **Data Cleaning and Preparation:**
Handling Missing Data: The dataset was evaluated for missing values, and suitable imputation strategies were implemented to maintain data integrity.

#### **Feature Engineering:**
Data Types: The year, month, day, hour, and minute were extracted from the `Order_Date_Time` column to derive additional valuable insights.
Outliers: The `Item_Price` column was analyzed for outliers using the IQR method, leading to the removal of 23.85% of data points that fell outside acceptable limits.
Encoding: One-Hot Encoding was applied to categorical features such as `Channel_name` and `Product_Category`.

#### **Univariate Analysis:**
Histograms and box plots were employed to analyze the distribution of continuous variables like `Item_price` and `CSAT Score`.

#### **Data Splitting:**
The data was split into training and test sets with an 80-20 ratio. Several classification models were trained, including 
Decision Trees, Random Forest, and Extratrees classifier. Hyperparameter tuning was performed, 
focusing on F1-Score as the primary evaluation metric to balance precision and recall.

#### **Model Evaluation:**
The models were evaluated using Precision, Recall, F1-Score, and Accuracy. 
The Extra trees model exhibited the best performance, particularly in terms of precision and accuracy, making it the model of choice.
The confusion matrix and ROC-AUC curve further supported the model's effectiveness in distinguishing between satisfied and dissatisfied customers.
Feature Importance:

The model identified `Customer_Remarks`, `issue_responded`, `Channel_name` and `category` as the most significant factors influencing customer satisfaction.
This suggests that `Customer_Remarks`, `issue_resoponded` are crucial for enhancing customer satisfaction


## Problem Statement: Predicting Flipkart Customer Satisfaction Scores Using Predictive Analytics and Machine Learning

## Context:

 In the highly competitive e-commerce industry, customer satisfaction is a critical determinant of brand loyalty and long-term growth. 
 As one of the largest e-commerce platforms, Flipkart handles millions of customer interactions across various support channels such as email, phone, live chat, and social media. 
 Maintaining high levels of customer satisfaction is essential for retaining customers and enhancing their shopping experience. 
 Understanding the factors that influence customer satisfaction and being able to predict CSAT scores based on 
 these factors can significantly improve Flipkart's customer service performance and help in optimizing resources.

## Objective:

The primary objective of this project is to develop a machine learning model that can predict customer satisfaction scores (CSAT) based on historical customer interaction data. 
By analyzing different features such as customer demographics, interaction types, issue resolution times, 
support channel performance, and agent efficiency, the model will identify the key drivers of customer satisfaction and 
provide actionable insights for improving the overall customer service experience. The target variable is the CSAT score, 
which reflects the satisfaction level of customers after interacting with Flipkart's support team.

## Key Challenges:

Data Imbalance: The dataset may contain an imbalanced distribution of high and low satisfaction scores, which can lead to biased predictions. 
Addressing this issue with techniques like oversampling, undersampling, or advanced algorithms will be crucial.

Feature Engineering: Accurately capturing the drivers of customer satisfaction will require careful feature engineering. 
This may involve creating new features related to agent performance, interaction duration, issue complexity, and support channel usage to improve model accuracy.

Multichannel Integration: Customer interactions occur across different support channels (e.g. inbound, outcall, email). 
Integrating and normalizing these interactions for model input poses a challenge, especially when data comes in different formats and volumes from each channel.

Scalability: Given the high volume of customer interactions, the model needs to be scalable to handle large datasets in real-time scenarios while maintaining prediction accuracy.

Model Evaluation: Since the goal is to accurately predict satisfaction levels, precision, recall, and F1-score metrics will be essential in evaluating the model’s performance, 
with a particular focus on avoiding false negatives (i.e., predicting high satisfaction when the customer is actually dissatisfied).


## Deliverables:

A machine learning model capable of predicting customer satisfaction (CSAT) based on customer interaction data.
A detailed report on data preprocessing steps, feature engineering, model selection, evaluation metrics, and key insights derived from the analysis.

## Business Impact:

By accurately predicting customer satisfaction, Flipkart can prioritize high-risk customers and take proactive measures to resolve potential issues before they escalate. The insights generated from the model will allow Flipkart to optimize its customer support processes, such as allocating more resources to underperforming channels, rewarding high-performing agents, and customizing support strategies for different customer segments. Ultimately, improving CSAT scores will enhance brand loyalty, reduce customer churn, and drive higher customer retention rates, contributing to Flipkart’s long-term success in the competitive e-commerce market.

**Conclusion:**

In this classification project, I have successfully implemented various machine learning models to predict customer satisfaction (CSAT) scores. 
After evaluating multiple algorithms, I have selected the Extra Trees model as the final choice due to its exceptional performance metrics, 
including high accuracy, recall, precision, and F1-score.

The analysis included assessing feature importance, revealing insights into which features significantly influence CSAT predictions. 
The project demonstrated the effectiveness of model selection and feature analysis in enhancing predictive capabilities. 
Overall, this classification project not only provided valuable predictions for customer satisfaction but also highlighted the importance of careful model evaluation and 
feature engineering in achieving robust outcomes.
