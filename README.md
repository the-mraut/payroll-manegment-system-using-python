Install Required Python Libraries
1. Install pip (if not already installed):  python -m ensurepip --upgrade
2. Install dependencies from requirements.txt:pip install -r requirements.txt
3. Direct installation (if not using requirements.txt): pip install pymysql
4. Verify installation:  python -c "import pymysql; print('PyMySQL installed successfully!')"

Database Installation Section
Install & Configure MySQL Database (Using XAMPP)
🔹 1. Install XAMPP
Download XAMPP from: https://www.apachefriends.org/download.html
Install it on your system (choose default settings).
Open XAMPP Control Panel and start any more than two  service not work in one seriver and only compalsary MySQL.
Click Admin to open phpMyAdmin in your browser.

🔹 2. Create Database & Table with phpMyAdmin
In phpMyAdmin, click Databases → Create Database → enter ems.
Select the new database and open the SQL tab.
Paste this SQL code:
CREATE TABLE emp_salary (
    e_id VARCHAR(50) PRIMARY KEY,
    designation VARCHAR(100),
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10),
    email VARCHAR(100),
    hired VARCHAR(100),
    dateofbirth VARCHAR(20),
    dateofjoin VARCHAR(20),
    experience VARCHAR(50),
    id_proof VARCHAR(100),
    contact VARCHAR(20),
    status VARCHAR(50),
    address TEXT,
    month VARCHAR(20),
    year VARCHAR(10),
    salary DECIMAL(10,2),
    total_days INT,
    absent INT,
    medical DECIMAL(10,2),
    fund DECIMAL(10,2),
    convence DECIMAL(10,2),
    net_salary DECIMAL(10,2)
);
Click Go to execute.

🔹 3. Configure Connection in employee_system.py
By default, XAMPP MySQL runs at localhost with user root and no password:
con = pymysql.connect(
    host='localhost',
    user='root',
    password='',
    database='ems'
)
🔹 4. Test Database Connection
Run this in Python:
import pymysql
con = pymysql.connect(host='localhost', user='root', password='', database='ems')
print("Database connected successfully!")
con.close()

🔹 5.Run it
