# Pewlett-Hackard-Analysis

**Overview of the analysis**
- Explain the purpose of this analysis.
This analysis was conducted for Bobby, an analyst at a company called Pewlett-Hackard. The analysis used SQL to determine the number of employees who might retire soon based on their birth_date, from_date, and to_date. The analysis was conducted to help the company prepare for retirement packages and to identify the positions they will need to fill soon. Pewlett-Hackard is a big company and need to have a solid plan if a big portion of the employee will be retiring soon. The analysis also included identifying employees who are eligible to participate in a mentorship program. 
- Approach
SQL was used to conduct the analysis on six CSV files containing information about the employees at Pewlett-Hackard company. After identifying the primary keys, foreign keys, and the data types, we created the entity relationship diagram (**ERD**) to visualize the relationships between the different files. A copy of the ERD is inserted below.

![EmployeeDB.png](https://github.com/FUNMIIB/Pewlett-Hackard-Analysis/blob/main/EmployeeDB.png)

![QuickDBD-export.pdf](https://github.com/FUNMIIB/Pewlett-Hackard-Analysis/blob/main/QuickDBD-export.pdf)

**Results**
Provide a bulleted list with four major points from the two analysis deliverables. Use images as support where needed.
- Two analysis was conducted for this requirement.
**Retirement**
- The first anaysis is **retirement by title**. In this analysis we joined multiple datasets and filtered on different columns within the datasets to create a **retirement titles table** containing all the titles of current employees born between January 1,1952 and December 31, 1955. There are a huge number of senior Engineers, and Engineers who are eligible for retirement in the near future  as shown in the screen shot below. The screen shot shows part of the table with several senior level titles who may retire soon. This result will help inform the recruiting team at the company to plan ahead to recruit senior level engineers to fill these roles. 
- Based on our analysis, there are few middle level management employees who will be retiring anytime soon. However, a lot of senior staff are eligible for retirement which means that the company would need to allocate more resources towards senior level staff recruitment but less resources towards middle level management hire.  

**Mentorship**
- The second analysis was performed to identify current employees who were born in 1965 so that the retiring employees can participate in a mentoring program in which they train some employees in the roles of the positions they are leaving. Our analysis showed a list of employee who are eligible for the mentorship program as shown below

![mentorship_eligibilty.csv](https://github.com/FUNMIIB/Pewlett-Hackard-Analysis/blob/main/Data/mentorship_eligibilty.csv)

- Also, the analysis reveal that the number of employees who could be mentored will not be sufficient to fill the positions that engineers are leaving. 

**Summary** 
Provide high-level responses to the following questions, then provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami."
How many roles will need to be filled as the "silver tsunami" begins to make an impact?
The company will need to fill 90,398 positions. 
SELECT COUNT(*)FROM unique_titles;

Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

Yes, there are enough qualified (1549 employees), retirement-ready employees ready to mentor the next generation of Pewlett-Hackard employees. Majority of the employees retiring are senior level as shown in the previous image. Again, the number of employess who are eliigble for mentorship is low and may not be sufficient to fill the position that would be open. 
SELECT COUNT(*)FROM mentorship_eligibilty;




