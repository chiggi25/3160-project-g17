# 3160-project-g17
A database for a food delivery service
Group 17 Creators: Connor Higgins, Jack Hitchcock, Ashley Hutchinson

Table of Contents:

1. Scope - The reasoning and expectations for the project
2. Business Rules - Describes what is allowed to happen within the database
3. Use Case - Describes how the service could be used or implemented
4. EERD - the extensive visual description of the database and all organizing values
5. Data Dictionary - A set of database tables which stores information used to execute queries
6. MySQL Queries (three) - These are queries which display the capabilities of our system 
7. Trigger - The automated response to occur once procedure is initiated
8. Stored Procedure - The type of code, once ran, sets off the trigger
9. Description of Future Work - 
10. MySQL dump - 

1. Scope: 

For this project, we will be creating a test database to integrate into the food delivery service for campuses. We will be utilizing MySQL to create the database. The purpose of this database is to aid and assist the organization in the logistics, record keeping, and other data related operations.

2. Business Rules:

There are many persons
A person can either be a faculty, staff, or student
There are different locations to order from
A person can place many orders
An order is for one restaurant only
Only students can become delivery drivers. These drivers must be approved
A location has many items
A location can receive many orders

3. Use Case: 
	This delivery service can be very effective for conferences and business meetings mid day where individuals don’t have the time to run out and grab food, so they call for on campus delivery either for themselves, or the group of people they’re with. This would be especially useful during times like job fairs where company representatives have to be on campus for long periods of time and as a courtesy to them, the department hosting the event count could provide said service. Along with that, students who don’t have time to grab food during back to back classes could use this service to have something delivered directly to their classroom. This could be helpful to ensure students have the ability to eat during a busy schedule.
![usecase](https://user-images.githubusercontent.com/46718667/78734337-ffbbe700-7915-11ea-988a-d1167049d574.JPG)

4. EERD:

![EERD](https://user-images.githubusercontent.com/46718667/78734299-e9ae2680-7915-11ea-82e4-74d29d0c03ad.JPG)

5. Data Dictionary: 
The data dictionary could be used to store all of the information of all the certified delivery men and women who are allowed on campus to ensure the safety of the students and faculty. Along with that, you can use the data dictionary to track the information of each order being taken and delivered, tracking the delivery number, cost of the food, location of the order, route to the objective, etc. This could be crucial to have all of the information that the store needs, to know who is ordering the food, what the order is and who to give it to for delivery. It’s also important for the university to be tracking who’s on their campus to maintain a safe environment.

Tables: 
Persons: PK: personID(string, name(string), email(string), phone number(int)
Faculty: uses personID(string), title(string), highestDegree(string), degreeCollege(string)
Staff: uses personID(string), position(string), admin?(boolean)
Student: uses personID(string), graduating year(int)
Order: PK: orderID(string) FK: locationID(string) from Locations and personID(string) from persons, number of items(int), total price of order(double)
Locations: PK = locationID(string), name of location(string), pickup description (string), website(string), schedule(string), location address(string)
Items: PK: itemID, name of the item(string), price of the item(double), calorie count of the item(int)
Driver: PK: licenseNumber(int), date they were hired(string), description of their car(string), rating(int 0 - 10)

6. MySQL Queries (three) - These are queries which display the capabilities of our system 

7. Trigger - Once the procedure is initiated there is an automated response. 

8. Stored Procedure - 

9. Description of Future Work - 

10. MySQL dump - 
