Name - PARUL SHARMA

Company - CODTECH IT SOLUTION

Domain - PYTHON PROGRAMMING

Duration - JULY 1st,2024 to AUGUST 1st, 2024

OVER-VIEW OF THE PROJECT :-

This Python code implements a basic inventory management system with user authentication. Here's a breakdown of the code:

1. Imports:
    sqlite3: This library allows working with SQLite databases for storing inventory data.
    bcrypt: This library is used for securely hashing user passwords.

2. Database Setup (setup_database function):
    This function creates a database named "inventory.db" if it doesn't exist.
    It defines three tables:
    users: Stores user credentials (username and hashed password).
    products: Stores product information (name, quantity, and price).
    sales: Tracks sales data (product ID, quantity sold, and date).
    It uses FOREIGN KEY constraint to ensure a product ID in the sales table references an existing product in the products table.

3. User Authentication:
    register_user(username, password):
    Hashes the password using bcrypt.
    Attempts to insert username and hashed password into the users table.
    Returns True if registration is successful (unique username), False otherwise.
    login_user(username, password):
    Retrieves the stored password for the given username.
    Compares the entered password with the hashed password using bcrypt.checkpw.
    Returns True if credentials match, False otherwise.

4. Product Management:
    add_product(name, quantity, price):
    Inserts a new product entry into the products table with the provided information.
    edit_product(product_id, name, quantity, price):
    Updates an existing product in the products table based on the product ID.
    delete_product(product_id):
    Removes a product from the products table based on the product ID.

5. Inventory Tracking and Reports:
    get_low_stock_products(threshold):
    Retrieves products with quantity below the specified threshold from the products table.
    record_sale(product_id, quantity, sale_date):
    Decrements the product quantity in the products table based on the sold amount.
    Inserts a new sale record into the sales table with product ID, quantity sold, and sale date.
    get_sales_summary():
    Joins the products and sales tables to retrieve total quantity sold and total sales for each product.

6. Main Menu (main function):
    This function presents a menu for user interaction.
    It has two main sections:
    Login section: Allows users to register or login with username and password.
    Inventory management section (after successful login): Provides options to add, edit, delete products, view low stock, record sales, and view sales summary.

7. Script Execution (if name == "main":):
    This ensures the main function runs only when the script is executed directly (not imported as a module).

Overall, this code provides a basic framework for managing inventory and user accounts. It demonstrates essential functionalities like product tracking, sales recording, and secure user authentication.
