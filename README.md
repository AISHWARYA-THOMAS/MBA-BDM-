# MBA-BDM-
Aishwarya Thomas - 22121005 

Richy Duke - 22121038

DOMAIN NAME: BANKING SECTOR 

INTRODUCTION:

As  Business Analysts for the banking sector,We have designed a database structure for a banking application.The database must handle enormous amount of data securely also efficiently and provide a smooth experience overall with accurate and timely information to customers.Therefore, in this task, we have identified several significant entities and attributes that are deemed to be essential for designing the  structure for this domain and using which I have created an ER diagram and coverted to table to manage data effectively.


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

Loan Table:

•	Loan_ID (Primary Key)
•	Loan_Type
•	Loan_Amount
•	Interest_Rate
•	Term
•	Status
•	Customer_ID (Foreign Key)

Credit_Card Table:

•	Card_Number (Primary Key)
•	Card_Type
•	Credit_Limit
•	Balance
•	Status
•	Customer_ID (Foreign Key)

ATM Table:

•	ATM_ID (Primary Key)
•	Location
•	Status
•	Branch_ID (Foreign Key)

Currency Table:

•	Currency_Type (Primary Key)
•	Exchange_Rate
•	Status

Investment Table:

•	Investment_ID (Primary Key)
•	Investment_Type
•	Investment_Amount
•	Interest_Rate
•	Term
•	Status
•	Customer_ID (Foreign Key)

ER DIAGRAM - BANKING SECTOR


![BDM-CIA1 drawio (1)](https://user-images.githubusercontent.com/125997499/234367176-ee34c7ac-5c07-495d-9a6b-b49597b8e9c4.png)





# TABLE: Customer
| Customer ID  | Customer Name       | Contact Info  | Account Number  |  
|---------------:|------------------------|:--------------:| --------------------:|
|  9001             |  Aishwarya Thomas   |  7638926678 |  160022221111    |    
|  9002             |  Sanskar Gaur            |  8970095674 |  160022221021    |    

#TABLE: Account
|  Account Number  |  Account Type |  Balance                            |  Status | Customer ID     | 
|---------------------:|-----------------|:----------------------------:|--------:|-----------------:|
|  160022221024  |  Savings              |  1200456                           |  Open  | 9003     | 
|  160022221021  |  Mutual               |  78900                               |  Closed | 9008 | 

#TABLE: Transaction
|  Transaction ID  |  Transaction Type |  Amount |  Date |  Time |  Location |  Account Number |
|------------------:| -------------------|:----------:| ------:|-------:|-----------:|---------------------:|
|  888234             |  Cash |  10000 |  12/01/2023 |  09:22:45 |  Pune |  160022221021 |
|  888999  |  UPI |  500 |  03/02/2023 |  04:49:48 |  Chennai |  160022221771 |

#TABLE: Branch
|  Branch ID |  Branch Name |  Address |  Contact Info|
|--------:| -------- |:-----------------------:| -------------:|
|0002 | Pune   | 16 chun chowk ,Kedanaha  | 2446413       |

#TABLE: Employee
| Employee ID |  Employee Name |  Contact Info |  Position |  Salary |  Branch ID |
|--------------:| -------------------|:----------:| ------:|-------:|-----:|
| 22121008 |  Lalettan |  8940073646 |  Accountant |  120000 |  0006 |
| 22212289 |  Kajalesh |  8976543428 |  Cashier |  45000 |  0006 |

#TABLE: Loan
|  Loan ID  | Loan Type | Loan Amount | Interest Rate | Term | Status | Customer ID |
|-----------:| ----------- |:---------------:| --------------:|-------:|-------:|--------------:|
|  9166  | Home | 130000| 10% | 48 months | paid | 9002 |
|  8233  | Gold | 50000 | 15% | 18 months | pending | 9007 |

#TABLE: Credit
| Card Number  | Card Type | Credit Limit | Balance | Status | Customer ID |
|--------------:| -------------------|:----------:| ------:|-------:|-----:|
| 42222229876006  | Debit | - | 600000 | Active | 9006 |
| 42222654756786 | Credit | 100000 | Active | 9005 |

#TABLE: ATM
| ATM ID | Location | Status | Branch ID |
| ------:|-------:|-----:|---:|
|5858 | Swargat 2 | Offline | 0009 |
| ATM ID | Bandra | Active | 0005 |

#TABLE: Currency
| Currency Type  | Exchange Rate | Status |
|-------:|-----:|-----:|
| Rupee  | 61.4| Rise |
| Rupee  | 61.4 | Rise |

#TABLE: Investment
|  Investment ID  | Investment Type | Investment Amount | Interest Rate | Term | Status | Customer ID |
|------------------:| -------------------|:-----------------:|----------:|--------------:|-----------:|---------------------:|
|  23361  | Bonds | 10000 | 15% | 18 months | Completed | 9026 |
|  26223  | Fixed Deposit | 10000 | 10% | 48 Months | On-going | 9006 |







