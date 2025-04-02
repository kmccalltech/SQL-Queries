<h1> - Apply Filters to SQL Queries</h1>
<b>This is one of my labs I completed during my Google cybersecurity certification we used Qwiklabs to as our sandbox.</b>

Project description
The scenario of this project is that I’m a security professional at a large organization. Part of my job is to keep the system secure and investigate security issues. I’ve recently discovered some potential security issues that involve login attempts on employee machines. I will also need to pull up certain employees in specific departments to make updates to their machines so I will need to use SQL with filters to get only those machines/departments to show in the log.



<h2>List of Tasks</h2>

- Retrieve after hours failed login attempts
- Retrieve login attempts on specific dates
- Retrieve login attempts outside of Mexico
- Retrieve employees in Marketing
- Retrieve employees in Finance or Sales
- Retrieve all employees not in IT

<h2>Screenshots and description of Task Completion</h2>

<h3>Retrieve after hours failed login attempts</h3>
<p>I was asked to investigate a potential security incident that occurred after business hours which is 18:00. I will need to pull a log that shows those occurrences.

The screenshot below shows just how I execute that task using an SQL query and filter the after business hour failed login attempts.
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This query filters all the failed login attempts after 18:00. I selected all the data from the log_in_attempts table. Following that I used the Where clause to select the login_time column from the table, along with the and operator to only show the attempts that were after 18:00 and unsuccessful.
</p>
<br />

<h3>Retrieve login attempts on specific dates
</h3>
<p>A suspicious event occurred on 2022-05-09 and to investigate the event I had to review all the login attempts that occurred on that day and the day prior. 

The screenshot below shows how I executed that task using an SQL query and filter the login attempts on the specific dates.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To complete this task, I created a query that selected all the data from the log_in_attempts table and used the where clause to select the login_date column and requested only logins that happened on 2022-05-09 or 2022-05-08 by using the or operator. Doing so eliminated all the unnecessary dates from the returned log.
</p>
<br />

<h3>Retrieve login attempts outside of Mexico</h3>
<p>Later it was found that there was suspicious activity with login attempts but it was determined that the activity did not originate in Mexico but more information was needed to be gathered.

The screenshot below shows how I executed that task using an SQL query and filter the login attempts that occurred everywhere except Mexico.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To complete this task I created a query selecting all the data from the log_in_attempts table and used the where clause to select the country column and used the LIKE operator with “MEX%” string to bring up any data that represents Mexico. The % represents any number of unspecified characters when used with LIKE.
</p>
<br />

<h3>Retrieve employees in Marketing</h3>
<p>The team was given the task of updating certain employees in the Marketing department’s computers, to complete this we need to know which computers to update.

The screenshot below shows how I executed that task using an SQL query and filtered the employees in the Marketing department in the East building.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To complete this task I created a query selecting all the data in the employees table. Then I used the Where clause to target the department column, pairing that with AND operator to also target the office column as well. When targeting the office column I used East% to be sure to select all the office numbers within the east building.
</p>
<br />

<h3>Retrieve employees in Finance or Sales</h3>
<p>The next task is to update the computers for the employees in the Finance and Sales departments. It's going to be a different update from the previous one for the marketing department so a new query needs to be requested to get the information on those computers.

The screenshot below shows how I executed that task using an SQL query to filter the employees in the Finance and Sales departments.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To complete this task I created a query selecting all the data in the employees table. Then used a Where clause with the OR operator to filter the employees that's only in the Finance and Sales departments. The reason I used the OR operator instead of the AND is because I wanted to pull all information on employees that's in either department. The first condition “department = ‘Finance’” pulls all employees in the Finance department and the second condition “department = ‘Sales’” pulls all the employees in the Sales conditions.
</p>
<br />

<h3>Retrieve all employees not in IT</h3>
<p>My last task is to make a final update for all employees that are not in the I.T. (Information Technology) department. I need to get the information on all employees that are not a part of this department.

The screenshot below shows how I executed that task using an SQL query to filter the employees not in the Information Technology department.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The query shows how I selected all the employees from the employees table then used a Where clause with the NOT operator to filter the employees not in the I.T. department.
</p>
<br />

<h3>Summary</h3>
<p>To complete the task above I had to use different filters on SQL queries to get the necessary information about login attempts and employee departments. I used the AND, OR, and NOT operators to filter the information from the employee and log_in_attempts tables. Then used even more specific filters LIKE and the percentage sign to get information needed from the tables.
</p>
