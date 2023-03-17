# DBMS_ajai

USE exercise_hr;

-- Write a query to find the name (first_name, last name), department ID and name of all the employees.

SELECT  first_name, last_name, e.department_id, department_name 
FROM employees AS e INNER JOIN departments AS d
ON e.department_id = d.department_id;

-- Write a query to display job title, employee name, and the difference between salary of the employee and minimum salary for the job
USE exercise_hr;
SELECT first_name, last_name, job_title, salary-MIN_salary DIFFERENCE
FROM employees INNER JOIN jobs;


-- Write a query to get the department name and average salary in the department
USE exercise_hr;
SELECT department_name AS 'DEPARTMENT NAME' , AVG(SALARY) AS 'AVERAGE SALARY'
FROM employees Natural JOIN departments;


-- Write a query to find the employee ID, job title, number of days between ending date and starting date for all jobs in department 90.
USE exercise_hr;
SELECT employee_ID, job_title,end_date-start_date Days
FROM job_history INNER JOIN jobs
WHERE department_id = 90;


USE exercise_hr;

SELECT department_id, COUNT(*) AS "number of employees"
FROM employees GROUP BY department_id;

CREATE TABLE tablename (
column1 COLUMN1_DATATYPE(size) CONSTRAINTS,
column2 COLUMN2_DATATYPE(size) CONSTRAINTS,
);

CREATE DATABASE IF NOT EXISTS project;	

-- VARCHAR - Variable length Character..
CREATE TABLE user (
username VARCHAR(50) PRIMARY KEY,
password VARCHAR(50),
dob DATE,
phone VARCHAR(20),
email VARCHAR(100),
first_name VARCHAR(50),
last_name VARCHAR(50)
);

DESCRIBE user;

/*
Numbers : INT, BIGINT
Decimal numbers (eg. 3.14) : DOUBLE
Strings :
		-- if fixed length: CHAR(2)
        -- if variable length: VARCHAR(255)
Date : DATE
Datetime :  DATETIME
Boolean : TINYINT
*/

USE exercise_hr;

-- Write a query to get the total salaries payable to employees.
SELECT SUM(salary) AS "Total Salary"
FROM employees;


-- Write a query to get the maximum and minimum salary from employees table.
SELECT MAX(salary) AS "Maximum Salary",MIN(salary) AS "Minimum Salary"
FROM employees;

-- Write a query to get the average salary and number of employees in the employees table.
SELECT AVG(salary) AS "Average Salary",COUNT(salary) AS "Number of employees"
FROM employees;

-- Write a query to get the number of employees working with the company.
SELECT COUNT(*) AS "Number of employees"
FROM employees;

-- Write a query to get the number of distinct jobs available in the employees table.
SELECT COUNT(DISTINCT job_id) AS "Distinct Jobs"
FROM employees;

-- Write a query get all first name from employees table in upper case.
SELECT UCASE(first_name) AS "First Name"
FROM employees;

SELECT CONCAT(first_name, ' ',last_name) AS "Full Name"
FROM employees;

 SELECT LENGTH(CONCAT(first_name, '',last_name)) AS "Length of Full Name"
FROM employees;

SELECT ROUND(salary, 2) AS "Monthly Salary"
FROM employees;

-- Write a query to get the first 3 characters of first name from employees table.
SELECT SUBSTR(first_name,1,3) AS "First 3 Characters"
FROM employees;



DROP TABLE user;

DESCRIBE user;

-- Add a new column 'whatsapp_no' with datatype int





-- Update the 'whatsapp_no' column datatype from int to varchar(20)





-- Delete the 'whatsapp_no' column







-- rename the 'dob' column to 'dob'


CREATE DATABASE IF NOT EXISTS project;

USE project;

/*
CREATE TABLE tablename (
column1 COLUMN1_DATATYPE(size) CONSTRAINTS,
column2 COLUMN2_DATATYPE(size) CONSTRAINTS,
);
*/

/*
Numbers : INT, BIGINT
Decimal numbers (eg. 3.14) : DOUBLE
Strings: 
		-- if fixed length: CHAR(2)
        -- if variable length: VARCHAR(255)
Date: DATE
Datetime: DATETIME
Boolean: TINYINT
*/
CREATE TABLE IF NOT EXISTS user (
username VARCHAR(50) PRIMARY KEY,
password VARCHAR(50),
dob DATE,
phone VARCHAR(20),
email VARCHAR(100),
first_name VARCHAR(50),
last_name VARCHAR(50)
);
ALTER TABLE whatsapp_no;

DESCRIBE user;

use project;

ALTER TABLE user
ADD whatsapp_no INT;
DESCRIBE user;

ALTER TABLE user
MODIFY whatsapp_no varchar(20);
DESCRIBE user;


ALTER TABLE user
DROP whatsapp_no;
DESCRIBE user;


ALTER TABLE user
RENAME COLUMN dob to date_of_birth;
DESCRIBE user;



-- Insert 10 rows into your user table.
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Ajai', '1234567', '2002-03-17', '9876543210', 'anataraj@gmail.com', 'Ajai', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Susi', '7654321', '2004-03-27', '9876543012', 'smuthu@gmail.com', 'Susi', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Praveen', '3214567', '2003-03-03', '8976543210', 'pgopinath@gmail.com', 'Praveen', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Arun', '3214567', '2003-04-03', '8976543210', 'adhanraj@gmail.com', 'Arun', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Karthi', '3214567', '2003-01-03', '8976543210', 'pkarthi@gmail.com', 'Karthi', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Gowtham', '3214567', '2003-03-03', '8976543210', 'gsathya@gmail.com', 'Gowtham', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Vijay', '3214567', '2003-03-03', '8976543210', 'vkumar@gmail.com', 'Vijay', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Surya', '3214567', '2003-03-03', '8976543210', 'skumar@gmail.com', 'Surya', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Kishore', '3214567', '2003-03-03', '8976543210', 'kkumar@gmail.com', 'Kishore', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Jaya', '3214567', '2003-03-03', '8976543210', 'jkumar@gmail.com', 'Jaya', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Muthu', '3214567', '2003-03-03', '8976543210', 'mkumar@gmail.com', 'Muthu', 'Kumar');
INSERT INTO user (username, password, dob, phone, email, first_name, last_name) VALUES ('Jai', '3214567', '2003-03-03', '8976543210', 'jaikumar@gmail.com', 'Jai', 'Kumar');

SELECT *
FROM user;

describe user;



-- Write a SQL statement to create a simple table countries including columns country_id,country_name and region_id

CREATE DATABASE IF NOT EXISTS countries;

CREATE TABLE countries (
country_id VARCHAR(3) PRIMARY KEY,
country_name VARCHAR(3),
region_id decimal(10,0)
);
DESCRIBE countries;
	
USE countries;

ALTER TABLE countries
ADD country_code INT;
DESCRIBE countries;

ALTER TABLE countries
DROP country_code;
DESCRIBE countries;

INSERT into countries (country_id, country_code, region) VALUES ('value_1', 'value_2', 'value_3');
SELECT *
FROM countries;
describe countries;




USE exercise_hr;
-- INNER JSON
SELECT *
FROM employees INNER JOIN departments
ON employees .department_id = departments.department_id;

SELECT *
FROM student INNER JOIN school
ON student .school_id = school.school_id;



SELECT employee_id, first_name, last_name, e.department_id, department_name 
FROM employees AS e INNER JOIN departments AS d
ON e.department_id = d.department_id;

-- find the employees working in the 'IT' department
SELECT employee_id, first_name, last_name, e.department_id, department_name 
FROM employees AS e INNER JOIN departments AS d
ON e.department_id = d.department_id
WHERE department_name = 'IT';


-- Write a query to find the name (first_name, last name), department ID and name of all the employees.
SELECT first_name, last_name, e.department_id
FROM employees AS e INNER JOIN departments AS d
ON e.department_id = d.department_id;

-- Write a query to display the first_name of all employees who have both "b" and "c"

USE exercise_hr;
SELECT first_name
FROM employees
WHERE first_name LIKE '%b%c%';

-- Write a query to display the last name of employees whose names have exactly 6 characters.

SELECT *
FROM employees
WHERE last_name LIKE '______';

-- Last name start with Mac
SELECT *
FROM customers
WHERE last_name REGEXP '^Mac';


-- last name ends with field
SELECT *
FROM customers
WHERE last_name REGEXP 'field$';

-- last names start with Mac or ends with field 
SELECT *
FROM customers
WHERE last_name REGEXP 'Mac|field$';

-- last name contains ae/be/ce/de/ee/fe/ge/he
SELECT *
FROM customers
WHERE last_name REGEXP '[a-h]e';

-- Write a query to display the last name of employees having 'e' as the third character.
USE exercise_hr;

SELECT *
FROM employees
WHERE last_name LIKE '__e%';

-- Write a query to display the last name of employees having 6 characters.
SELECT *
FROM employees
WHERE last_name LIKE '______';

