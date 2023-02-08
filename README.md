
# Consumer Complaint Resolution Analysis

This repository contains code and resources for the Consumer Complaint Resolution Analysis Project, which aims to predict whether a consumer complaint will result in a dispute or not.


## Project Overview

The Consumer Complaint Resolution Analysis Project aims to predict whether a consumer complaint will result in a dispute or not. The project will use data from consumer complaints to build a model that can identify patterns and relationships in the data, and then make predictions about whether a given complaint is likely to lead to a dispute. This information can be used by businesses to proactively address potential issues and resolve complaints before they escalate into disputes. The outcome of this project will be a predictive model that can help organizations improve customer satisfaction and minimize the number of disputes they face.
## Scenario

Product review is the most basic function/factor in resolving customer issues and increasingthe sales growth of any product. We can understand their mindset toward our service without asking each customer.When consumers are unhappy with some aspect of a business, they reach out to 

customer service and might raise a complaint. Companiestry their best to resolve the complaints that they receive. However, it might not always be possible to appease every customer.

So Here, we will analyze data, and with the help of different algorithms, we are finding the best classification of customer categoryso thatwe can predict our test data
## Objective

Useing Python libraries such as Pandas for data operations, Seaborn and Matplotlib for data visualization and EDA tasks, Sklearn for model building and performance visualization, and based on the best model,make a prediction for the test file and save the output.

The main objective is to predict whether our customer is disputed or not with the help of given data.
## Dataset description

- Customers faced some issues and tried to report their problems to customer care.
- Dispute: This is our target variable based on train data we have two groups, one with a dispute with the bank and another don’t have any issue with the bank.
- Date received: The day complaint was received.
- Product: different products offered by the bank (credit cards, debit cards, different types of transaction methods, accounts, locker services, and money-related)
- Sub-product: loan, insurance, other mortgage options
- Issue: Complaint of customers 
- Company public response: Company’s response to consumer complaint
- Company: Company name 
- State: State where the customer lives (different state of USA)
- ZIP code: Where the customer lives
- Submitted via: Register complaints via different platforms (online web, phone, referral, fax, post mail)
- Date sent to company: The day complaint was registered
- Timely response?: Yes/noConsumer 
- disputed?: yes/no (target variable)
- Complaint ID: unique to each consumer
## Prerequisites

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- NLTK
## Step by step workflow of the project
### `EDA`
- Reading the Data from the excel file.
- Checking the data type for both data (test file and train file)
- Missing value analysis and droping columns where more than 25% of data are missing 
- Extracting Day, Month,and Year from Date Received Column and createing new fields for a month, year,and day 
- Calculateing the Number of Days the Complaint was with the Company and createing a new field as “Days held”
- Droping "Date Received","Date Sent to Company","ZIP Code", "Complaint ID" fields
- Imputing Null value in “State” by Mode
- With the help of the days we calculated above,createing a newfield 'Week_Received' where we calculate the week based on the day of receiving.
- Storeinh data of disputed people into the “disputed_cons” variable for future tasks 

### `Data Visualization`
- Plot bar graph of the total no of disputes of consumers with the help of seaborn
- Plot bar graph of the total no of disputes products-wise with the help of seaborn
- Plot bar graph of the total no of disputes with Top Issues by Highest Disputes, with the help of seaborn
- Plot bar graph of the total no of disputes by State with Maximum Disputes
- Plot bar graph of the total no of disputes Submitted Via differentsource
- Plot bar graph of the total no of disputes where the Company's Response to the Complaints
- Plot bar graph of the total no of disputes where the Company's Response Leads to Disputes
- Plot bar graph of the total no of disputes.Whether there are Disputes Instead of Timely Response
- Plot bar graph of the total no of disputes over Year Wise Complaints
- Plot bar graph of the total no of disputes over Year Wise Disputes
- Plot bar graph of Top Companies with Highest Complaints

### `Data Preprocessing`
- Converte all negative days held to zero(it is the time taken by the authority that can't be negative)
- Droping Unnecessary Columns for the Model Building like:'Company', 'State', 'Year_Received', 'Days_held'
- Change Consumer Disputed Column to 0 and 1(yes to 1, and no to 0)
- Create Dummy Variables for categorical features and concat with the original data framelike: 'Product,’'Submitted via,’'Company response to consumer,’'Timely response?'

### ` Feature Engineering`
- Scaling the Data Sets and Makeing the feature Selection with the help of PCA up to 80% of the information.
- Splitting the Data Sets Into X and Y by the dependent and independent variables (data selected by PCA)

### `Model Building`
- Building models and measure their test and validation accuracy:
- Logistic Regression

- DecisionTree Classifier

- RandomForest Classifier

- AdaBoost Classifier

- GradientBoosting Classifier

- KNeighbors Classifier
- XGB Classifier
### `Prediction`
RandomForest Classifier gives us the most accurate result hence RandomForest Classifier will be the final model used for prediction
## Conclusion
In conclusion, this project aimed to build a machine learning model to predict whether a consumer complaint will be despute or not. The model was trained on a preprocessed dataset of consumer complaints and evaluated based on accuracy scores and classifier comparison plots. The best performing model was used to make the final prediction.

The results of this project can be useful for organizations that handle consumer complaints, as it can provide them with insights into which complaints are likely to be resolved and which ones are likely to escalate into disputes. This information can then be used to allocate resources more effectively and improve the overall complaint resolution process.

Overall, this project highlights the power of machine learning in solving real-world problems and its potential to help organizations make data-driven decisions.
## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/malikjanattar)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/malikjan-attar-69a7a317b)

