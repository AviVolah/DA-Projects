This is a project from Practicum Program

Its about finding the credit score of customers in a bank <br>
Its done in Jupyter<br>
Language: Python<br>
Source file: credit_scoring_eng.csv

# Analyzing borrowers’ risk of defaulting

👉 View the `notebook` **[here](https://nbviewer.org/github/AviVolah/AviVolah/blob/Practicum/Projects/1st%20Project/Project%201%20-%20Analyzing%20borrowers%20risk%20of%20defaulting.ipynb)** using **nbviewer**.


## Project description
### Objective
To prepare a report for a bank’s loan division; Find out if a customer’s marital status and number of children has an impact on whether they will default on a loan. The bank already has some data on customers’ credit worthiness.
The report will be considered when building a credit scoring of a potential customer. A credit scoring is used to evaluate the ability of a potential borrower to repay their loan.

### Description of data

`credit_scoring_eng.csv`:  Data on customers’ credit worthiness
- **children**: the number of children in the family
- **days_employed**: how long the customer has been working
- **dob_years**: the customer’s age
- **education**: the customer’s education level
- **education_id**: identifier for the customer’s education
- **family_status**: the customer’s marital status
- **family_status_id**: identifier for the customer’s marital status
- **gender**: the customer’s gender
- **income_type**: the customer’s income type
- **debt**: whether the customer has ever defaulted on a loan
- **total_income**: monthly income
- **purpose**: reason for taking out a loan


### Libraries to run the notebook locally
***Python version 3.8.8***
|Library| Version|
|---|---|
|Pandas | 1.3.5 |
|NumPy | 1.20.1 |
|Matplotlib | 3.5.2 |


## Project overview

### Prepare data
- Removed fully duplicated rows that show simultaneous repeated actions by the same user.
- Extracted date & time from the timestamp and saved them to new columns for easier analysis.

### Exploratory analysis
*Overall dataset exploration*
- Analyzed overall event frequency over time: both throughout the day and daily.
- Filtered out dates with incomplete data to focus on the true range of the experiment.
- Checked experiment groups to ensure they are similar sizes and that no users were mistakenly assigned multiple groups.

*Sales funnel analysis*
- Idenitified event types and their total frequency.
- Calculated the proportion of users who completed each action (conversion rate).
- Determined the most common order of events (discounting the optional tutorial) by ordering the first instance of each event type per user, and identifying the most common paths.
- Separately analyzed user paths of users who watched the tutorial using th esame method as above.
- Calculate overall conversion rate, as well as user retention at each stage of the event funnel.

### Analyze the results of the A/A/B test (*hypothesis testing*)
- Plotted & compared the conversion funnel of each experiment group.
- Created a hypothesis testing function to calculate the z-scores comparing the retention rate of each group at each stage of the sales funnel.
- First compared the two control groups to ensure there were no unanticipated problems with our test.
- Compared the experimental group to each control group separately.
- Compared the experimental group to the combined control groups.
- Calculated the Family-Wise Error Rate to determine if alpha values should be adjusted.

### Conclusion

No significant differences were found between the experiment group and the control groups, even without adjusting the alpha. The font change seems to have no impact on customer retention or conversion. 

The greatest loss of customers occurs immediately after accessing the main screen. 95% of customers who reach their carts go on to complete a purchase. We should focus our efforts on improving retention up until this stage, particular from the main screen to the offer screen. It is possible that watching the tutorial first may play a role in customer retention, but further experiments research is needed.
