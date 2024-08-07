# Coffee Shop Management System

Tables and Their Relationships


Customers

customer_id (Primary Key)
name
email
phone
loyalty_points


Employees

employee_id (Primary Key)
name
position
email
phone
salary


Suppliers

supplier_id (Primary Key)
name
contact_person
phone
email


Products

product_id (Primary Key)
name
description
price
category
stock_quantity
supplier_id (Foreign Key referencing Suppliers)


Orders

order_id (Primary Key)
customer_id (Foreign Key referencing Customers)
order_date
total_amount
order_status (e.g., pending, completed, cancelled)


OrderDetails

order_detail_id (Primary Key)
order_id (Foreign Key referencing Orders)
product_id (Foreign Key referencing Products)
quantity
price


Inventory

inventory_id (Primary Key)
product_id (Foreign Key referencing Products)
quantity
last_updated


Payments

payment_id (Primary Key)
order_id (Foreign Key referencing Orders)
payment_date
amount
payment_method (e.g., cash, card, online)


EmployeeShifts

shift_id (Primary Key)
employee_id (Foreign Key referencing Employees)
shift_date
start_time
end_time
