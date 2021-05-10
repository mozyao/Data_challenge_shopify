# Data-Science-Challenge
# Q1

a. It might involve extreme large values of order_amount. And which can be caused by large total_items or large average amount(price) of items in a single order.
b. I would use the metric USD dollars.
c. The final AOV is $151.69 if we ignore those orders palced by user_id 607 with 2000 items each time - option A. 
    While if we take those orders with total_items = 2000 into account, the final AOV is $307.01 - option B.
Roadmap of my solution:
(Feel free to explore the jupyter notebooks of both options inclued in the repo:)

Option A
1) Data Import and Clean.
2) Plot the figure, analysize the noise.
3) Filter out extreme points with ['total_items'] == 2000.
4) Plot again and analysize the further issue casued by large average amount(price) of items in a single order.
5) Filter out extreme points with ['ave_amount_of_item'] > 5000.
6) Plot the final figure which looks perfect.
7) Calcute the final AOV.

Option B
1) Data Import and Clean.
2) Filter out orders with average price that is extremly expensive. 
3) Calculate the AOV.

# Q2
Platfom: Chrome
a)
SELECT COUNT(OrderID) AS Orders 
FROM Orders, Shippers 
WHERE Shippers.ShipperID = Orders.ShipperID AND Shippers.ShipperName = "Speedy Express"

Thus, we have 54 orders shipped by Speedy Express.

b)

SELECT LastName FROM Employees
INNER JOIN (SELECT EmployeeID, count(EmployeeID) as num FROM Orders AS P 
GROUP BY EmployeeID ORDER BY num DESC LIMIT 1) AS P 
WHERE Employees.EmployeeID = P.EmployeeID

Thus, the last name of the employee with most orders is Peacock.

c)


