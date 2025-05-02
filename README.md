# Personal Budget App

####

Our Personal Budget System is a digital tool made to help users efficiently track, manage, and plan their finances. It can record transactions, categorize expenses, set financial goals, and provide insightful reports to promote better budgeting habits.


## Tech Stack

**Database:** MySQL WorkBench

**Backend:** PHP

**Frontend:** HTML/CSS

**Deployment:** Docker

**ERD Modeling:** Lucidchart



## Key Features

- Expense Categorization: Divide expenses into different categories.
- Goal-Based Savings Tracking: Allows users to set and track savings goals with visual progress indicators showing percentage saved toward goal….
- Income Tracking: User can add and manage multiple income sources.
- Bills Management: Track due dates and amounts to stay on top of payments.
- Reports: Monthly breakdown of income vs. expenses and bills.


## Challenges Encountered & Viable Solutions
- Challenge: Finding relevant datasets
   - Solution: Using Mockaroo for data generation
- Challenge: Cleaning and validating large datasets
   - Solution: Implementing data cleaning scripts


## Schema Structure
```plaintext
Personal Budget App
├── users
|   ├── user_id
|   ├── email
|   ├── username
|   ├── password
|   ├── data_joined                 
|
├── Income
|   ├── income_id
|   ├── user_id
|   ├── income_source
|   ├── income_amount
|   
├── Categories
|   ├── categories_id
|   ├── categories_name
|
├── Savings Goals
|   ├── user_id
|   ├── goal_id
|   ├── categories_id
|   ├── goal_name
|   ├── target_amount
|   ├── current_amount
|
├── Transactions
|   ├── user_id
|   ├── categories_id
|   ├── transaction_id
|   ├── transaction_amount
|   ├── transaction_date
|   ├── transaction_location
|
├── Bills
|   ├── bill_id
|   ├── user_id
|   ├── bill_name
|   ├── bill_amount
|   ├── due_date
|   ├── payment_date
|   ├── payment_status
|
├── Report
|   ├── report_id
|   ├── user_id
|   ├── report_month
|   ├── total_income
|   ├── total_transactions
|   ├── budget_status
|
└── README.md
```

## Requirements on how to open the program
- XAMPP (for Apache server, MySQL, and phpMyAdmin)
- A web browser

---

## How to set up the environment?
  ### 1. Download & Install XAMPP
    - Go to the official XAMPP website: [https://www.apachefriends.org/download.html](https://www.apachefriends.org/download.html)
    - Download the version best for your operating system

  ### 2. Launch XAAMP
    - Open the XAMPP Control Panel
    - Start the the following servers:
      - Apache
      - MySQL

  ### 3. Access phpMyAdmin
    - In the XAMPP Control Panel, clock **"Admin"** next to MySQL
    - This open **phpMyAdmin** in your web browser
    - From here, make sure the database 'finalproject' exists
      - If it doesn't, download the sql files directly from the github to access it
      - Then go to the **Import** tab and upload the SQL files with all the table definitions.

  **`Look for the SQL folder`**


## Accessing the Program
### 4. Place your files
  - Download 'budget_web' as a zip folder
  - Unzip the 'budget_web' and place it into your XAMPP 'htdocs' folder: Example path: 'C:\xampp\htdocs\budget_web'

### 5. Edit Database Connection
  - In 'db.php', adjust the connection settings to match your systems. Example:
    ```php
    $servername = "localhost";
    $username = "root";
    $password = "";
    $dbname = "finalproject";
    $conn = new mysqli($servername, $username, $password, $dbname);

### 6. Running the Program
  - Run the url on your local machine:
    'http://localhost/budget_web/front_end/index.html'


## Authors

- [Jennifer Nyguen](https://github.com/Jennygit03)
- [Tyler Roediger](https://github.com/tar3qMT)
- [Rahma Seid](https://github.com/rahmaseid)


## 🔗 Links
- [GitHub Repository](https://github.com/Jennygit03/budgeting_web)
- [Presentation](https://docs.google.com/presentation/d/1nu7YUajwIhhEvWLHyYrKfjP0L3KbYELVvl8LDzjkTFg/edit?usp=sharing)
- [Final Report](https://www.overleaf.com/project/67aaa486397e3fec25eea43a)
