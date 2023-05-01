Download Link: https://assignmentchef.com/product/solved-cis247a-ilab-5-inheritance
<br>
CIS247A iLab 5: Inheritance

General Questions – General General Questions

iLab 5 of 6: Inheritance

Scenario and Summary

The objective of the lab is to take the UML Class diagram and enhance last week’s Employee class by making the following changes:

Create a class called Salaried that is derived from Employee. Create a class called Hourly that is also derived from Employee. Override the base class calculatePay() method. Override the displayEmployee() method.

Deliverables

Due this week:

Capture the Console output window and paste into a Word document. Zip the project folder file. Put the zip file and screenshots (Word document) in the Dropbox.

i L A B  S T E P S

STEP 1: Understand the UML Diagram

Notice the change in UML diagram. It is common practice to leave out the accessors and mutators (getters and setters) from UML class diagrams, since there can be so many of them. Unless otherwise specified, it is assumed that there is an accessor (getter) and a mutator (setter) for every class attribute.

Employee #firstName : string #lastName : string #gender : char #dependents : int #annualSalary : double #benefit : Benefit -static numEmployees : +Employee() +Employee(in fname : string, in lname : string, in gen : char, in dep : int, in benefits : Benefit) +static getNumEmployees() : int +CalculatePay() : double +displayEmployee() : void Benefit -healthinsurance : string -lifeinsurance : double -vacation : int +Benefit() +Benefit(in hins : string, in lins : double, in vac : int) +displayBenefits() : void Salaried -MIN_MANAGEMENT_LEVEL : -MAX_MANAGEMENT_LEVEL : -BONUS_PERCENT : -managementLevel : int +Salaried() +Salaried(in fname : string, in lname : string, in gen : char, in dep : int, in sal : double, in ben : Benefit, in manLevel : int) +Salaried(in sal : double, in manLevel : int) +CalculatePay() : double +displayEmployee() : void Hourly -MIN_WAGE : -MAX_WAGE : -MIN_HOURS : -MAX_HOURS: -wage : double -hours : double -category : string +Hourly() +Hourly(in wage : double, in hours : double, in category : string) +Hourly(in fname : string, in lname : string, in gen : char, in dep : int, in wage : double, in hours : double, in ben : Benefit, in category : string) +CalculatePay() : double +displayEmployee() : void

STEP 2: Create the Project

Create a new project and name it CIS247C_WK5_Lab_LASTNAME. Copy all the source files from the Week 4 project into the Week 5 project.

Before you move on to the next step, build and execute the Week 5 project.

STEP 3: Modify the Employee Class

Using the updated Employee class diagram, modify the attributes to be protected. Delete the iEmployee interface class, and remove the reference from the Employee class.

STEP 4: Create the Salaried Class

Using the UML Diagrams from Step 1, create the Salaried classes, ensuring to specify that the Salary class inherits from the Employee class. For each of the constructors listed in the Salaried class, ensure to invoke the appropriate base class constructor and pass the correct arguments to the base class constructor. This will initialize the protected attributes and update the numEmployees counter. The valid management levels are 0, 1, 2, and 3, and should be implemented as a constant. Override the calculatePay method to add a 10 percent bonus for each of the management levels (i.e., bonus * .10). The bonus percentage should be implemented as a constant. Override the displayEmployee() method to add the management level to the employee information.

STEP 5: Label Title

Using the UML Diagrams from Step 1, create the Hourly classes, ensuring to specify that the Hourly class inherits from the Employee class. For each of the constructors listed in the Hourly class, ensure to invoke the appropriate base class constructor and pass the correct arguments to the base class constructor. This will initialize the protected attributes and update the numEmployees counter. The valid category types are “temporary”, “part time”, and “full time”. The provided hours must be more than 0 hours and less than 50 hours, and the limits should be implemented as constants. The provided wage must be between 10 and 75, and the limits should be implemented as constants. Override the calculatePay method by multiplying the wages by the number of hours. Override the Employee setAnnualSalary method and set the annual salary by multiplying the weekly pay by 50. Override the displayEmployee() method to add the category to the hourly employee information.

STEP 6: Label Title

Using previous weeks’ assignments as an example, create at least one Employee, Hourly, and Salaried employee. For each object created, display the number of employees created. For each object created, write statements to exercise each of the public methods listed in the Class diagram. For each object created, invoke the object’s displayEmployee() method to display the employee’s information. For employee, the following information needs to be displayed:

Partial Sample output

Screenshot of program output that reads: Employee Information ________________________________________ Name: Nana Liu Gender: F Annual Salary: 60000.00 Weekly Salary: 1153.85 Benefit Information ________________________________________ Health Insurance: PPO Life Insurance: 1.50 Vacation: 20 days — Number of Employee Object Created — Number of employees: 1

6.  For salaried employee, the following information needs to be displayed:

Partial Sample output

Screenshot of program output that reads: Name: Jackie Chan Gender: M Dependents: 1 Annual Salary: 50000.00 Weekly Salary: 1250.00 Benefit Information ________________________________________ Health Insurance: HMO Life Insurance: 100.00 Vacation: 16 days Salaried Employee Management Level: 3 — Number of Employee Object Created — Number of employees: 2

7.  For hourly employee, the following information needs to be displayed:

Partial Sample output

Screenshot of program output that reads: Name: James Bond Gender: M Dependents: 0 Annual Salary: 100000.00 Weekly Salary: 2000.00 Benefit Information ________________________________________ Health Insurance: PPO Life Insurance: 5.00 Vacation: 17 days Hourly Employee Category: Unknown Wage: 40.00 Hours: 50.00 — Number of Employee Object Created — Number of employees: 3

STEP 7: Compile and Test

When done, compile and run your code.

Then, debug any errors until your code is error-free.

Check your output to ensure that you have the desired output, modify your code as necessary, and rebuild.

Below is the complete sample program output for your reference.

Screenshot of program output that reads: ************** Employee 1 ************** Please enter your First Name Nana Please enter your Last Name Liu Please enter your Gender Female Please enter your Dependents 2 Please enter your Annual Salary 60000 Please enter your HealthInsurancePPO Please enter your LifeInsurance1.5 Please enter your Vacation Days20 Employee Information ________________________________________ Name: Nana Liu Gender: F Annual Salary: 60000.00 Weekly Salary: 1153.85 Benefit Information ________________________________________ Health Insurance: PPO Life Insurance: 1.50 Vacation: 20 days — Number of Employee Object Created — Number of employees: 1 ************** Employee 2 ************** Please enter your First Name Jackie Please enter your Last Name Chan Please enter your Gender Male Please enter your Dependents 1 Please enter your HealthInsuranceHMO Please enter your LifeInsurance100 Please enter your Vacation Days16 Employee Information ________________________________________ Name: Jackie Chan Gender: M Dependents: 1 Annual Salary: 50000.00 Weekly Salary: 1250.00 Benefit Information ________________________________________ Health Insurance: HMO Life Insurance: 100.00 Vacation: 16 days Salaried Employee Management Level: 3 — Number of Employee Object Created — Number of employees: 2 *************** Employee 3 *************** Please enter your First Name James Please enter your Last Name Bond Please enter your Gender Male Please enter your Dependents 0 Please enter your Health InsurancePPO Please enter your Life InsurancePPO Please enter your Vacation Days17 Employee Information _______________________________________ Name: James Bond Gender: M Dependents: 0 Annual Salary: 100000.00 Weekly Salary: 2000.00 Benefit Information ________________________________________ Health Insurance: PPO Life Insurance: 5.00 Vacation: 17 days Hourly Employee Category: Unknown Wage: 40.00 Hours: 50.00 — Number of Employee Object Created — Number of employees: 3 The end of the CIS247C Week 5 iLab. Press any key to continue…

STEP 8: Label Title

Capture the Console output window and paste into a Word document. Put the zip file and screenshots (Word document) in the Dropbox.

Submit your lab to the Dropbox located on the silver tab at the top of this page. For instructions on how to use the Dropbox, read these Step-by-Step Instructions or watch this  Dropbox Tutorial.

See Syllabus “Due Dates for Assignments &amp; Exams” for due date information.