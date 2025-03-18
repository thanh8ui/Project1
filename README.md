Team 1 Mist 4610 Group Project 1
Team Name:
al_Group_47114_G6 Group 6
Team Members:
Luke Eckert @Luke-Eckert 
Elyse Robbins @


Problem Description:
The task at hand is to model and build a relational database for the general workings of a bakery business. The central entity in the model is the Bakery entity, representing each physical bakery location that the company owns and operates in various areas. The bakery operates in conjunction with the products it sells, the ingredients it sources, the suppliers it works with, and the customers who purchase from them, whether in-store or via special orders.
We are interested in accurately modeling these relationships, generating sample data, and populating the entities and their attributes with this sample data. Furthermore, we are interested in performing functioning queries on this data to provide valuable business insights about the bakery’s operations, such as tracking best-selling products, monitoring ingredient inventory, evaluating supplier reliability, and analyzing customer purchasing trends.


Data Model
Our model represents the structure of a bakery business, encompassing various essential entities and their relationships to support operations such as order management, employee assignments, and inventory tracking.
1. Suppliers & Ingredients
The Suppliers entity represents vendors that provide raw materials for the bakery. Each supplier has an ID, name, contact information, and a list of products they supply. Suppliers have a one-to-many relationship with Ingredients, meaning a single supplier can provide multiple ingredients.
The Ingredients entity tracks essential materials used in baking, including ingredient names, stock quantities, unit costs, expiration dates, and the associated supplier.
2. Products & Product Ingredients
The Products table contains all items available for sale in the bakery, including their names, categories, prices, and availability status. Since bakery products are made up of multiple ingredients, we introduce the Product_Ingredients associative entity, which establishes a many-to-many relationship between Products and Ingredients. This table tracks the required quantity of each ingredient for a specific product.
3. Customers & Orders
The Customers table maintains records of customer details such as names, contact information, and loyalty program status. Customers place Orders, forming a one-to-many relationship where a customer can have multiple orders.
The Orders entity contains order-specific details such as order date, total cost, and order status. Since each order consists of multiple products, we introduce the Order_Items table, which links Orders to Products in a many-to-many relationship. This table tracks the quantity of each product in an order and its subtotal.
4. Employees & Assignments
The Employees table records bakery staff details, including their names, roles, salaries, and work schedules. Employees are assigned to specific tasks via the Employee_Assignments table, which tracks the task description and assignment dates.
Employees also play a role in fulfilling orders, which is represented by the Employees_Orders table. This entity captures which employees are responsible for each order and their roles in the process (e.g., cashier, baker, delivery).



Data Dictionary:
Table: Customers















Queries:

Query 1 lists the number of reservations at each dining establishment that were made for between 6 and 8pm as well as the name of each dining establishment these reservation were made for. The results are also ordered by number of reservations in descending order.

Query 1 allows allows managers to see which establishments have received the most number of reservations during their busiest time (6-8pm) which is typically dinner time. These establishments likely need more support, resources, and personnel around dinner time. Therefore, this query allows managers to identify which establishments to allocate this extra help to. Listing the results in descending order of number of reservations makes it easier to see which establishment to prioritize.
Query 2 lists the number of dining reservations made by guests on each floor. The results are ordered in ascending order of floor number.

Query 2 allows managers to see whether there is a trend between what floor a guest stays on and how much they reserve tabes at the resort's dining establishments. If managers were to find that dining reservations decreased as the floor number increased, it would have possibly indicated that guests were not dining at dining establishments because they felt the distance of the dining establishment from their room was too far and inconvenient.
Query 3 lists the information for all the guests who have not made an activity reservation.

Query 3 allows the resort to market toward specific customers and contact them (e.g. promotional emails/coupons) about must-try activities. This helps to maximize revenue and increase efficiency by specifically targeting those who are not engaging in activities, rather than wasting time and resources to advertise to those who are already aware of and partaking in these activities.
Query 4 lists the names and phone numbers of dining employees who work in the highest rated dining establishment.

A restaurant with a high star rating is a large source of revenue for the resort and management may want to know the names of the employees who work there and how to contact them to reward them for maintaining such a high achieving restaurant (e.g. via a bonus, raise, awards, recognition) or to know which employees to target for continuous training and supervision in order to keep service within the establishment in top shape.
Query 5 lists the guests’ names and the hotel they are checking into if their reservation is during the PM, their room is a single or suite, their check in dates are between 2023-04-01 and 2023-04-10, and their hotel rating is above a 4.

Query 5 allows the resort to manage how busy their check in will be during the PM hours of early April in their better hotels where the check in rooms are singles or suites. This can help the resort determine how many employees need to be working the check in desks to check in single or suite reservations in the afternoon of these dates in these specific hotels.
Query 6 lists the names of guests who have over 10 activity reservations and the activities that they have those reservations in.

Query 6 allows the resort to determine what guests are contributing the most to each activity’s revenue. The resort may use this information to reward guests who spend the most on activities by offering special prizes and promotions, creating guest loyalty and creating an incentive to reserve even more.
Query 7 lists the the amount of dining reservations per guest and the average amount of guests these reservations have.

Query 7 allows the resort to see how many guests they should plan to seat, how the tables should be set up, and can lead to the resort figuring out how much revenue should be expected for the average visit.
Query 8 lists the guestID, guest name, and the number of room reservations per guest.

Query 8 allows the resort to identify their frequent customers and how many times they have stayed. This could lead to a card system down the line. If a guest reaches 5 or 10 visits, there could be a platinum card which would gift the user reservation priority, food discounts, and other perks.
Query 9 lists all the rooms along with their average room view rating if the rating is above a 4 star. Additionally, the query is sorted by the view rating and arranged in descending order.

Query 9 allows the employees and customers to see which rooms have an average view rating of 4 or more. Rooms with extravagant views are huge attractions to customers and can be a deciding factor when picking which room to stay in. This will help employees find which rooms have the best views fast and efficiently when asked.
Query 10 lists the names and prices of all activities offered by the resort that have not yet been booked by any guests and that are less than or equal to $50. Additionally, the results of the query are ordered by price in ascending order.

Query 10 allows the employees and customers to see what activities have not been booked yet, and the prices for these activities. The price is sorted in ascending order to make it easier to find the most affordable activities which most people are looking for. Activities are a huge part of the resort experience and using this script will make it easy for employees to find which activities are available as well as the prices for these activities.
Database information:
Name of the database: ns_21479_1
Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format:
