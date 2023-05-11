PROBLEM STATEMENTS:

1.To retrieve the names of customers whose accounts are currently active in order to identify the active customer base. By obtaining this information, the bank can determine the popularity of its services and tailor its offerings to meet the needs of its customers.


Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/760050a7-414f-4da1-adb2-e01adfce6db4)

Graph:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/5998a939-55db-4b21-b0d9-4901c74320f2)

Code:

SELECT customer.Customer_ID, Customer_Name, account.Account_Number,account.Balance
FROM Customer 
JOIN Account  ON customer.Customer_ID = account.Customer_ID;

 2.To retrieve the names and account numbers of all customers who have a balance greater than 40,000. By obtaining this information, the bank can identify high-net-worth individuals and potentially offer them personalized services to retain their loyalty.

 
 Output:
 
![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/69954343-4d8d-460e-ab5b-f1e37916d3f7)

Code:

SELECT DISTINCT Customer_Name, account.Account_status
FROM Customer  JOIN Account  ON customer.Customer_ID = account.Customer_ID WHERE Account_status = 'Open';

3.The objective is to retrieve the names of customers who have a savings account with a balance greater than 40,000. By identifying these customers, the bank can potentially offer them exclusive investment opportunities and financial services to retain their business.
 
 Output:
 
 ![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/6264e77a-ae7b-4889-85a4-507f4f976c5c)

Graph: 

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/585da577-609e-4359-b253-af1036f2483f)
 
 Query:
 
 SELECT Customer.Customer_ID, Customer_Name, account.Account_Number,account.Balance
FROM Customer 
JOIN Account  ON customer.Customer_ID = account.Customer_ID
WHERE Balance > 40000;


4.To retrieve the names of customers who currently hold a savings account with a balance greater than 300,000. This information is crucial for the Bank to identify its high net worth customers and potentially offer them specialized services and benefits. By extracting this data, the Bank can also gain insights into its savings account holders, understand their banking behaviors and preferences, and use this information to improve its products and services.
 
Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/33d5af67-b2d9-4d66-891c-93ab7dcb8075)

Graph:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/c7d0d041-45f2-431a-a344-06061f34a527)

Query:
 
 SELECT DISTINCT customer.Customer_Name, account.Balance
FROM Customer 
JOIN Account  ON customer.Customer_ID = account.Customer_ID
WHERE Account_type = 'Savings' AND Balance > 300000;


5.To determine the total balances of account types in order to gain insights into the financial behavior of the Bank's customers. By analyzing the total balances of various account types, such as savings, checking, and investment accounts, the Bank can identify patterns and trends among its customers and make informed decisions regarding its financial products and services. This information can also be used to tailor marketing and promotional strategies to specific customer segments, based on their account type and balance.

Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/53ea56bf-3d39-48f9-9133-789c8d23bd57)

Graph:
![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/6006febd-6f7c-4c96-8192-a3d762fd7589)

Code:

SELECT Account_Type, SUM(Balance) AS Total_Balance
FROM account
GROUP BY Account_Type;

6.To retrieve the customer ID, name, Email ID of customers who have taken a loan and have a credit card. By obtaining this information, we aim to identify potential opportunities for cross-selling and up-selling, as well as tailor our marketing efforts towards these customers based on their borrowing and spending behavior. Additionally, this data can help us better understand the financial needs and preferences of our customers and improve our loan and credit card offerings accordingly.

Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/29cdf05b-7850-4652-8a5b-061e03e66751)

Query:

 SELECT customer.Customer_ID, customer.Customer_Name, customer.Email_ID, loan.Loan_type, credit.Card_type
FROM Customer 
JOIN Credit  ON credit.Customer_ID = customer.Customer_ID
JOIN Loan  ON loan.Customer_ID = customer.Customer_ID;

7.We need to retrieve the customer ID and name of customers who have a loan with a status of 'Infunding' and a credit card with a balance greater than 100,000. By identifying these customers, the bank can potentially offer them personalized financial advice and services to improve their financial situation.

Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/4e20a89b-1ea2-464b-871c-7c518dcc8af8)

Graph:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/46b69726-07ab-4f57-981b-1afbaf03c53e)

Code:

  SELECT customer.Customer_ID, customer.Customer_Name,credit.Balance,credit.Status
FROM Customer 
    JOIN Loan ON customer.Customer_ID = loan.Customer_ID
    JOIN Credit  ON customer.Customer_ID = credit.Customer_ID
WHERE loan.Status = 'Infunding'and balance > 100000; 

8.The objective is to calculate the total loan amount by loan type in order to gain insights into the bank's loan portfolio and identify any potential risks. By analyzing this information, the bank can make informed decisions regarding its lending policies and strategies.

Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/50e29e27-6f7e-41ca-8dbf-d4f50a4f8729)

Graph:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/6f1c6bce-469e-4cf5-b292-882ede773b91)

Code:
SELECT Loan_type, SUM(Loan_Amount) as Total_Loan_Amount
FROM Loan
GROUP BY Loan_type;

9.To determine the count of inactive credit cards for each customer based on the credit card type. By analyzing the number of inactive credit cards for each type, we aim to gain insights into customer behavior and potentially make informed decisions regarding the credit card products and services offered by the company.
10.We need to display the number of active loans by loan type in order to analyze the bank's lending portfolio and identify any potential risks. By analyzing this information, the bank can make informed decisions regarding its lending policies and strategies.

Output:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/c57ee526-d344-4239-9592-f5809176a91a)

Graph:

![image](https://github.com/AISHWARYA-THOMAS/MBA-BDM-/assets/125996803/ab2b678d-3410-4534-8588-664a6c26d8ed)

Code:
SELECT Loan_type, COUNT(*) as Number_of_Active_Loans
FROM Loan
WHERE Status = 'Active'
GROUP BY Loan_type;

10.Display the number of active loans by loan type. By obtaining this information, the organization can assess the performance of each loan type, identify areas of improvement, and make informed decisions regarding their loan portfolio. Additionally, this data can be used to develop effective strategies for loan management and to provide insights to stakeholders about the organization's financial health.

Output:

Graph:

Query:

11.We need to retrieve the count of ATMs by status in order to ensure that the bank's ATMs are functioning properly and to identify any potential issues. By analyzing this information, the bank can make informed decisions regarding its ATM maintenance and repair policies.
Output:

Graph:

Code:



