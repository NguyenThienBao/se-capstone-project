# Requirement Analyst 

## 1 - Functional requirement

### 1.1 - E-commerce website

* Homepage will be showed with the special production with:
    * Top 4 hot products.
    * Top 4 best seller products.
* The menu will show categories of products.
* For each category, the system will show a list of product which belong to the category.
* Product's information will be show in the product detail page.

* The user can be sign-up or sign-in account in the system.
* To buy product, user must be register account.
* After login with Customer account, the user can choose the production to add to the shopping cart.
* The customer can manage their shopping cart with the item that has not been check-out. (Optional, the custmer can pay online with the payment gateway)
* The customer can checkout the current shopping cart.
* The customer can check the status of their orders.

### 1.2 - Admin Dashboard

* After login with the admin role or employeee role, the system will show the dashboard with the chart which visualize the current report of the selling of the shop.

### 1.2.1 - Employee Role

* Manage the categories information.
* Manage production information.
* Manage the orders.

#### 1.2.2 - Admin role 

* Manage user account.
* Manage the system configuration.

## 2 - Non-functional requirement

* The maximum loading time is 3 seconds.
* The system must be secured with authentication and authorization techniques.

## 3 - User-role

List of user-role:
* ***admin*** - is the system's manager. They only control user account and system-configuration.
* ***employee*** - is the employee of the company, they will control the product information, process the orders, ...
* ***customer*** - is the online buyer. They have information and account in the system with the Customer role. They can use the customer account to buy the products on the online website.
* ***guest*** - is the anonymous custome. They can only view the product in the system. They can register Customer account.