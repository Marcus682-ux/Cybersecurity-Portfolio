
# Project Description

You are a security professional at a large organization. Part of your job is to investigate security issues to help keep the system secure. You recently discovered some potential security issues that involve login attempts and employee machines.

Your task is to examine the organization’s data in their employees and log_in_attempts tables. You’ll need to use SQL filters to retrieve records from different datasets and investigate the potential security issues.

# Retrieve After Hours Failed Login Attempts

Your team is investigating failed login attempts that were made after business hours. You want to retrieve this information from the login activity. You’ll identify all unsuccessful attempts after 18:00.

To query login attempts made after business hours and return only the failed attempts, use the following search parameters. Since ``` FALSE ``` is Boolean and not a string, it does not need to be in quotations.

``` SELECT * FROM log_in_attempts WHERE login_time > '18:00:00' AND success = FALSE; ```

This will return the following results:

![Screenshot 2024-06-09 152431](https://github.com/nosajman33/Cybersecurity-Portfolio/assets/152820081/71b3dea3-848c-4a55-be1e-f64652d20d50)


# Retrieve Login Attempts on Specific Dates

Your team is investigating a suspicious event that occurred on ``` 2022-05-09 ```. You want to retrieve all login attempts that occurred on this day and the day before ``` (2022-05-08) ```.

Use the ``` OR ``` operator to retrieve login attempts on multiple specific days.

``` SELECT * FROM log_in_attempts WHERE login_date = '2022-05-09' OR login_date = '2022-05-08'; ```

The results show login attempts made only on _2022-05-09_ and _2022-05-08_.

![image](https://github.com/nosajman33/Cybersecurity-Portfolio/assets/152820081/17290ba3-f177-4555-972b-7dc5c074e7f5)

# Retrieve Login Attempts Outside of Mexico

Now, your team is investigating logins that did not originate in Mexico, and you need to find this information.

Mexico is represented in the table as both ``` MEXICO ``` and ```MEX ```, so the wildcard symbol ``` % ``` can be used to include both results. The ``` NOT ```  operator will be used to exlude login attempts from Mexico.

``` SELECT * FROM log_in_attempts WHERE NOT country LIKE 'MEX%'; ```

The results show only login attempts from the US and CANADA

![image](https://github.com/nosajman33/Cybersecurity-Portfolio/assets/152820081/814b0cf6-9244-4cbe-8295-3375cf12afbd)

# Retrieve Employees in Marketing

Your team is updating employee machines, and you need to obtain the information about employees in the ``` Marketing ``` department who are located in all offices in the East building (such as ``` East-170 ``` or ``` East-320 ```).

This query pulls employees in Marketing working in the East Building from the ``` employees ``` database. 

``` SELECT * FROM employees WHERE department = 'Marketing' and office LIKE 'East%'; ```
The results show that there are 7 people working in the Marketing department.

![image](https://github.com/nosajman33/Cybersecurity-Portfolio/assets/152820081/12e52bdb-306c-4eb7-b86c-563bb3652376)

# Retrieve Employees in Finance or Sales

Now, your team needs to perform a different update to the computers of all employees in the Finance or the Sales department, and you need to locate information on these employees.

The ``` OR ``` operator is used to query results for multiple criteria.

``` SELECT * FROM employees WHERE department = 'Finance' or department = 'Sales'; ```

![image](https://github.com/nosajman33/Cybersecurity-Portfolio/assets/152820081/dd67a8f3-d2ec-475e-bdd1-1bc69feefc0c)

# Retrieve All Employees Not in IT

Your team needs to make one more update. This update was already made to employee computers in the Information Technology department. The team needs information about employees who are not in that department.

The ``` NOT ``` operator is used once again to exclude computers in the ``` Information Technology ``` department.

``` SELECT * FROM employees WHERE NOT department = 'Information Technology'; ```

![image](https://github.com/nosajman33/Cybersecurity-Portfolio/assets/152820081/8dc9a506-a839-4ef1-a0b2-db7ecf5890cb)

# Summary
This was a simple demonstration for using ``` AND ```, ``` OR ```, and ``` NOT ``` to filter query results in SQL. Hopefully this clarified which circumstance to use each of the operators and the syntax for using them.








