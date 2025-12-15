# Flipkart-Customer-Support-Data-Analysis

### **Objective:**

This project aims to develop a classification model to predict customer satisfaction scores for Flipkart. This predictive model will help the company identify areas for improvement in customer experience and optimize their marketing and service strategies, ultimately enhancing customer retention and satisfaction.

### **Dataset Overview:**

The dataset comprises 20 columns, with several features showing a strong correlation to customer behavior. Key customer-related variables include `Order_ID`, `Order_date_time`, `Customer_City`, `Item_Price`, `Channel_Name`, and `Customer_Remarks`. Additionally, key operational variables include `Issue_Responded_at`, `Issue_Responded`, `Survey_Response_Date`, `Product_Category`, `Agent_Name`, `Supervisor`, `Manager`, `Agent_Shift`, and `Sub_Category`. The target variable is the `CSAT Score`, which ranges from 1 to 5, indicating customer satisfaction—higher scores reflect greater satisfaction.

### **Data Manipulation:**

The date variables were converted from object type to datetime format for improved processing. The Connected_Handling_Time column was removed due to having 99% of its values as null. Additionally, any rows with null values in the `Order_ID` column were eliminated. To address missing data, null values in categorical columns, including `Customer_City`, `Customer_Remarks`, and `Product_Category`, as well as in numeric columns like `Item_Price`, `Issue_Reported_at`, and `Issue_Responded`, were filled appropriately.

### **Exploratory Data Analysis (EDA):**

The EDA phase involved a comprehensive exploration of the dataset to uncover trends, patterns, and relationships that could inform the model-building process.

### **Data Cleaning and Preparation:**

Handling Missing Data: The dataset was evaluated for missing values, and suitable imputation strategies were implemented to maintain data integrity.

### **Feature Engineering:**

Data Types: The year, month, day, hour, and minute were extracted from the `Order_Date_Time` column to derive additional valuable insights.
Outliers: The `Item_Price` column was analyzed for outliers using the IQR method, leading to the removal of 23.85% of data points that fell outside acceptable limits.
Encoding: One-Hot Encoding was applied to categorical features such as `Channel_name` and `Product_Category`.


### **Univariate Analysis:**

Histograms and box plots were employed to analyze the distribution of continuous variables like `Item_price` and `CSAT Score`.

### **Data Splitting:**

The data was split into training and test sets with an 80-20 ratio. Several classification models were trained, including Logistic Regression, Decision Trees, Random Forest, kNeighbors, and Extra Trees classifiers. Hyperparameter tuning was performed, focusing on F1-Score as the primary evaluation metric to balance precision and recall.

### **Model Evaluation:**

The models were evaluated using Precision, Recall, F1-Score, and Accuracy. The Extra Trees model exhibited the best performance, particularly in terms of precision and accuracy, making it the model of choice.
The confusion matrix and ROC-AUC curve further supported the model's effectiveness in distinguishing between satisfied and dissatisfied customers.
Feature Importance:

The model identified `Customer_Remarks`, `issue_responded`, `Channel_name`, and `category` as the most significant factors influencing customer satisfaction. This suggests that `Customer_Remarks`, `issue_resoponded` are crucial for enhancing customer satisfaction.

### **Conclusion:**

The final model successfully predicts customer satisfaction scores with high precision. This model can be deployed to enhance Flipkart's customer experience initiatives, ensuring that resources are allocated to customers with the highest potential for satisfaction. Insights from feature importance analysis can guide strategic decisions in marketing and service improvements.
