# MBA-BDM-
Aishwarya Thomas - 22121005 

Richy Duke - 22121038

DOMAIN NAME: BANKING SECTOR 

INTRODUCTION:

As a Business Analyst for the banking sector, I have been tasked with designing the database structure for a banking application. In the banking industry, it is essential to have a structured and efficient database to manage customer data, account information, and transaction details to ensure a smooth banking experience for customers. The database must be able to handle a large amount of data securely and efficiently, as well as provide accurate and timely information to customers and bank staff. Therefore, in this task, I have identified several significant entities and attributes that are essential for designing the database structure for the banking domain. Using this information, I have created an ER diagram and converted it into a table design that will help us to organize and manage the data effectively.


ENTITIES:
1.	Customer
2.	Account
3.	Transaction
4.	Branch
5.	Employee
6.	Loan
7.	Credit Card
8.	ATM
9.	Currency
10.	Investment


ATTRIBUTES:

Customer Table:
•	Customer_ID (Primary Key)
•	Customer_Name
•	Contact_Info
•	Account_Number (Foreign Key)

Account Table:
•	Account_Number (Primary Key)
•	Account_Type
•	Balance
•	Status
•	Customer_ID (Foreign Key)

Transaction Table:
•	Transaction_ID (Primary Key)
•	Transaction_Type
•	Amount
•	Date
•	Time
•	Location
•	Account_Number (Foreign Key)

Branch Table:
•	Branch_ID (Primary Key)
•	Branch_Name
•	Address
•	Contact_Info

Employee Table:
•	Employee_ID (Primary Key)
•	Employee_Name
•	Contact_Info
•	Position
•	Salary
• Branch_ID (Foreign Key)

