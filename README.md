<h1>Applying filters to SQL queries</h1>

<h2>Project Description</h2>
<p>
In this scenario, I am a security analyst at a fictional organization. 
Part of my job is to investigate security issues to help keep the system secure. 
I recently discovered some potential security issues that involve login attempts and employees’ machines.
</p>
<p>
My task is to examine the organization’s data in the employees and log_in_attempts tables.
I use SQL filters to retrieve records from different datasets and investigate the potential security issues.  
</p>
<br />

<h2>Walkthrough:</h2>

<h3 align="left">Retrieve after hours failed login attempts</h3>
<img src="https://i.imgur.com/p6A39uJ.png" height="100%" width="100%" alt="Retrieve after hours failed login attempts"/>
 <p>
  A potential security incident occurred after business hours. To investigate this, I needed to query the log_in_attempts table and review login attempts made after 6:00pm or in this case, 18:00.  
 </p>
 <p>
   I made a query by selecting all data from the log_in_attempts table and used the WHERE clause and the AND operator to filter login_time > ‘18:00’ and success = 0 (for FALSE while 1 is for TRUE). 
   The results show that 19 unsuccessful login attempts were made after 6:00pm.
 </p>
<br />
<br />

<h3 align="left">Retrieve login attempts on specific dates</h3>
<img src="https://i.imgur.com/j9zzOpc.png" height="100%" width="100%" alt="Retrieve login attempts on specific dates"/>
 <p>
  There was a suspicious event that occurred on 2022-05-09 and the day before. I wanted to review all the login attempts that occurred on this day and the day before. The below screenshot shows the query to filter on these dates. 
 </p>
 <p>
   I made a query to select all data from the log_in_attempts table and used the WHERE clause and the OR operator on login_date. The OR operator is used instead of AND to include login attempts that were made either on  2022-05-09 or 2022-05-08. 
 </p>
<br />
<br />

<h3 align="left">Retrieve login attempts outside of Mexico</h3>
<img src="https://i.imgur.com/j7jjEWv.png" height="100%" width="100%" alt="Retrieve login attempts outside of Mexico"/>
 <p>
  I wanted to filter for suspicious login attempts that were made outside of Mexico.
 </p>
 <p>
   The query in the screenshot above used the NOT operator to filter for all attempts not in Mexico. 
   The LIKE operator is used with the pattern “MEX%” to exclude all attempts that have either MEXICO or MEX in the results. 
   The % in the pattern means any other characters as long as the previous characters before % match. 
 </p>
<br />
<br />

<h3 align="left">Retrieve employees in Marketing</h3>
<img src="https://i.imgur.com/0VhAVid.png" height="100%" width="100%" alt="Retrieve employees in Marketing"/>
 <p>
  The marketing team in the East office needs to have their computers updated.
 </p>
 <p>
  I made a query to select all data from the employees table and then used the WHERE operator to filter for employees that work in the Marketing department and whose office is in the East. 
   The LIKE operator is used with the pattern “East%” to include all East offices in the results.  
 </p>
<br />
<br />

<h3 align="left">Retrieve all employees not in IT</h3>
<img src="https://i.imgur.com/n1eejiz.png" height="100%" width="100%" alt="Retrieve all employees not in IT"/>
 <p>
  A few days later, we decided to apply another update to all employees’ computers that are not in the Information Technology department. 
 </p>
 <p>
  Once again, I made another query to select all data from the employees table and used the WHERE clause and the NOT operator to not include employees who work in the Information Technology department in the results. 
 </p>
<br />
<br />

<h2>Summary</h2>
<p>
  I learned how to apply filters in a SQL query to look for specific information. 
  The AND operator is used to filter for data that have a specific criteria in 2 different categories. 
  The OR operator is used to filter for data that have 2 different criterias in the same category. 
  The NOT operator is used to filter for data that do not have a specific criteria. 
  The LIKE operator, when used with a string pattern, can be used to find a specific pattern of data. 
</p>
