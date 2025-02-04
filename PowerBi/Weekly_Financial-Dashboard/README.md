
---

# Financial Analysis Dashboard Project

This project involves creating a financial analysis dashboard using **MySQL** for data management and **Power BI** for visualization. The goal is to analyze customer and credit card data to derive actionable insights and track key performance indicators (KPIs).

---

## **Project Overview**
The project consists of the following steps:
1. **Data Collection**: Collect customer and credit card data from CSV files.
2. **Database Setup**: Create a MySQL database and load the data into tables.
3. **Data Analysis**: Perform SQL queries to analyze the data.
4. **Dashboard Creation**: Build interactive dashboards in Power BI for customer and credit card KPIs.
5. **Real-Time Data Simulation**: Append additional data to simulate real-time updates.

---

## **Files Included**
1. **Data Files**:
   - `customer.csv`: Contains customer-related data.
   - `credit_card.csv`: Contains credit card transaction data.
   - `cust_add.csv`: Additional customer data for real-time simulation.
   - `cc_add.csv`: Additional credit card data for real-time simulation.

2. **Database Scripts**:
   - SQL scripts to create the database and tables.

3. **Power BI Files**:
   - `Dashboard.pbix` and contains dashboard is made using initall data files 
   - `Dashboard-Extended.pbix` : Power BI file containing the dashboards creaed using  Additional data along with the initall data.

4. **Documentation**:
   - `README.md`: This file.
   

---

## **Database Schema**
The MySQL database consists of two main tables:

### **1. Customer Table (cust_detail)**
- **Columns**:
  - `Client_Num` (Primary Key)
  - `Customer_Age`
  - `Gender`
  - `Dependent_Count`
  - `Education_Level`
  - `Marital_Status`
  - `state_cd`
  - `Zipcode`
  - `Car_Owner`
  - `House_Owner`
  - `Personal_loan`
  - `contact`
  - `Customer_Job`
  - `Income`
  - `Cust_Satisfaction_Score`

### **2. Credit Card Table (cc_detail)**
- **Columns**:
  - `Client_Num` (Foreign Key)
  - `Card_Category`
  - `Annual_Fees`
  - `Activation_30_Days`
  - `Customer_Acq_Cost`
  - `Week_Start_Date`
  - `Week_Num`
  - `Qtr`
  - `current_year`
  - `Credit_Limit`
  - `Total_Revolving_Bal`
  - `Total_Trans_Amt`
  - `Total_Trans_Ct`
  - `Avg_Utilization_Ratio`
  - `Use_Chip`
  - `Exp_Type`
  - `Interest_Earned`
  - `Delinquent_Acc`

---

## **Steps to Set Up the Project**

### **1. MySQL Database Setup**
1. Create a database:
```sql
   CREATE DATABASE ccdb;
   USE ccdb;
   ```




1. Create the `customer` and `credit_card` tables using the provided SQL scripts.

2. Load the data from the CSV files into the tables:
   ```sql
   LOAD DATA INFILE 'path/to/customer.csv'
   INTO TABLE customer
   FIELDS TERMINATED BY ','
   ENCLOSED BY '"'
   LINES TERMINATED BY '\n'
   IGNORE 1 ROWS;
   ```

3. Append additional data for real-time simulation:
   ```sql
   LOAD DATA INFILE 'path/to/cust_add.csv'
   INTO TABLE customer
   FIELDS TERMINATED BY ','
   ENCLOSED BY '"'
   LINES TERMINATED BY '\n'
   IGNORE 1 ROWS;
   ```

---

### **2. Power BI Dashboard Setup**
1. Open Power BI Desktop.
2. Connect to the MySQL database:
   - Go to **Home** > **Get Data** > **MySQL Database**.
   - Enter the server and database details.
3. Load the `customer` and `credit_card` tables.
4. Create the following dashboards:
   - **Customer Dashboard**:
     - KPIs: Total Customers, Average Income, Customer Satisfaction Score. 
     - Visualizations: Customers by Gender, Customers by Education Level, Income Distribution.
   - **Credit Card Dashboard**:
     - KPIs: Total Transactions (Count), Average Utilization Ratio (Avg), Total Interest Earned and total Revenue.
     - Visualizations: Transactions by Card Category, Utilization Ratio by Card Category, Quarterly Revenue and Transaction Volume Trends and some more for making comparison b/w groups on the bases of revenue.

---

## **Key Features**
1. **Interactive Dashboards**:
   - Users can filter data by date, card category, gender, etc.
2. **Real-Time Data Simulation**:
   - Append additional data to simulate real-time updates.
3. **Scalable Database**:
   - MySQL database can handle large datasets efficiently.

---

## **Tools Used**
- **MySQL**: For database management.
- **Power BI**: For data visualization and dashboard creation.
- **CSV Files**: For initial data loading.



## **How to Use**  
1. Clone the repository:  
```bash  
git clone https://github.com/7fighter/DataAnalyst.git  
```  
2. Navigate to the Power BI project directory:  
```bash  
cd DataAnalyst/PowerBi/Weekly_Financial-Dashboard  
```  
3. Set up the MySQL database using the provided scripts.  
4. Open the Power BI file (`Dashboard.pbix`) and connect it to your MySQL database.  
5. Explore the dashboards and analyze the data.  

## **Contributors**  
- [Syed Abbas](https://github.com/7fighter)  



## **Contact**  
For any questions or feedback, please contact:  
- Email: abbassyed389@gmail.com  
- GitHub: [7fighter](https://github.com/7fighter)  

---  


---

