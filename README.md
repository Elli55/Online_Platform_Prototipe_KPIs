# Online_Platform_Prototipe_KPIs
The little analitik dashboard for Onlien Portal
  
   
   # SWOT & Sales Analysis Database

This project consists of a structured SQL database designed for analyzing customer purchases, product sales, and competitor SWOT analysis. The goal is to leverage structured data for insights into business performance, competitive positioning, and market trends.

   Technologies Used
- **SQL** for database management and queries
- **Power BI** for data visualization and dashboard creation
- **Excel/CSV** for data import/export (if applicable)

##  Database Structure

###  Customers Table
Stores customer information, including their country and registration date.

```sql
CREATE TABLE Customers (
    Customer_ID INT PRIMARY KEY,
    Name VARCHAR(255),
    Country VARCHAR(50),
    Registration_Date DATE
);
```
# Sample Data:
| Customer_ID | Name          | Country      | Registration_Date |
|------------|--------------|-------------|------------------|
| 1          | Anna Müller  | Germany     | 2023-01-15      |
| 2          | Tom Schneider | Germany     | 2023-03-22      |
| 3          | Elena Fischer | Switzerland | 2022-11-10      |

---

## Products Table
Contains details about the products available for purchase.

```sql
CREATE TABLE Products (
    Product_ID INT PRIMARY KEY,
    Product_Name VARCHAR(255),
    Category VARCHAR(100),
    Price DECIMAL(10,2)
);
```
### Sample Data:
| Product_ID | Product_Name               | Category     | Price  |
|-----------|---------------------------|-------------|--------|
| 101       | Online Marketing Course    | Education   | 199.99 |
| 102       | E-commerce Guide           | Books       | 49.99  |
| 103       | SEO Toolkit                | Software    | 299.99 |

---

#### Sales Table
Tracks sales transactions, linking customers and products.

```sql
CREATE TABLE Sales (
    Sale_ID INT PRIMARY KEY,
    Customer_ID INT,
    Product_ID INT,
    Quantity INT,
    Sale_Amount DECIMAL(10,2),
    Sale_Date DATE,
    Channel VARCHAR(50),
    FOREIGN KEY (Customer_ID) REFERENCES Customers(Customer_ID),
    FOREIGN KEY (Product_ID) REFERENCES Products(Product_ID)
);
```
#### Sample Data:
| Sale_ID | Customer_ID | Product_ID | Quantity | Sale_Amount | Sale_Date  | Channel      |
|--------|------------|-----------|----------|------------|-----------|------------|
| 1001   | 1          | 101       | 1        | 199.99     | 2023-02-01 | Website    |
| 1002   | 2          | 102       | 2        | 99.98      | 2023-04-10 | Social Media |
| 1003   | 3          | 103       | 1        | 299.99     | 2023-12-05 | Affiliate  |

---

###### Competitor SWOT Analysis Table
Stores SWOT analysis data for our company and competitors.

```sql
CREATE TABLE SWOT_Analysis (
    Company VARCHAR(255),
    Strengths TEXT,
    Weaknesses TEXT,
    Opportunities TEXT,
    Threats TEXT
);
```


# Power BI Dashboard
A **Power BI Dashboard** has been created using the sales data from this database. The visualizations include:
- **Total Revenue Analysis**
- **Sales by Product Category**
- **Customer Demographics by Country**
- **Competitor SWOT Insights**





  Author
 Alrahman Verdiyev  
https://www.linkedin.com/in/alrahman-elli-verdiyev/  
 Email:mr.elreman@gmail.com



