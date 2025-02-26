# C_project_Semester1
: Inventory Management System

Purpose: The purpose of the code is to create a simple inventory management system with user authentication, product management, and sales tracking. It allows users to add, view, update, delete, and search for products in an inventory. Additionally, it tracks sales, updates stock levels, and supports restocking products that are low in quantity. The system ensures secure user authentication and stores data persistently using text files.
Importance: This inventory management system is important for businesses or small enterprises to efficiently manage product inventories. It helps track stock levels, monitor sales, and ensure products are always available. The code provides an organized way to handle inventory data and automate tasks like updating stock, restocking, and recording sales, thus improving business operations and decision-making. The use of file handling ensures that data is saved and can be accessed even after program termination, making the system more reliable and practical.
Features:-
1. User Authentication:
	Sign Up: Allows new users to register by providing a username and password.
	Sign In: Validates existing users and ensures secure access to inventory data.
2. Product Management:
	Add Products: Enables adding new products to the inventory.
	Update Products: Allows modification of product details such as name, price, and quantity.
	Delete Products: Removes products from the inventory.
3. Inventory Operations:
	Search Products: Retrieves product details by ID.
	Sort Products: Organizes inventory based on price, quantity, or name.
	Sold Products: Tracks and updates the quantity of sold products.
4. Data Persistence:
	Inventory data is stored in text files specific to each user.
	Ensures data is saved across program sessions.
5. Interactive Console UI:
	Colored text output for better user experience.
	Clear menu-driven navigation.
6. File Handling:
	Ensuring data integrity during simultaneous read and write operations.
	Handling cases where files do not exist or are inaccessible.
7. Error Handling:
	Validating user input to prevent crashes caused by invalid data.
	Managing edge cases, such as attempting to delete a product that does not exist.
8. Sorting Algorithms:
	Implementing sorting based on multiple criteria while maintaining code simplicity.
9. User Authentication:
	Protecting user credentials and ensuring secure login processes.


Function Descriptions
Function Descriptions
1. fileExists()
•	Checks if a specified file exists.
•	Prototype: int fileExists();
•	Parameters: filename: File name to check
•	Return Value: 1 if file exists, 0 otherwise
2. createFile()
•	Creates a new file with the specified name.
•	Prototype: void createFile(char *name);
•	Parameters: name: File name to create
•	Return Value: None
3. sign_in()
•	Handles user sign-in by verifying credentials and preparing the user's inventory file.
•	Prototype: int sign_in(struct Users user[], int *user_count);
•	Parameters: user[]: Array of users, user_count: Pointer to user count
•	Return Value: 1 if sign-in successful, 0 otherwise
4. sign_up()
•	Allows a new user to register and sign in.
•	Prototype: void sign_up(struct Users user[], int *user_count);
•	Parameters: user[]: Array of users, user_count: Pointer to user count
•	Return Value: None
5. write_product()
•	Adds a new product to the inventory, ensuring unique IDs.
•	Prototype: void write_product();
•	Parameters: None
•	Return Value: None
6. read_products()
•	Reads and displays products from the user's inventory file.
•	Prototype: void read_products();
•	Parameters: None
•	Return Value: None
7. del_product()
•	Deletes a product from the inventory based on its ID.
•	Prototype: void del_product();
•	Parameters: None
•	Return Value: None
8. update_product()
•	Updates product details based on its ID.
•	Prototype: void update_product();
•	Parameters: None
•	Return Value: None
9. search_product()
•	Searches for a product by its ID and displays details.
•	Prototype: void search_product();
•	Parameters: None
•	Return Value: None
10. sort_products()
•	Sorts products based on price, quantity, or name.
•	Prototype: void sort_products();
•	Parameters: None
•	Return Value: None
11. sold_products()
•	Records product sales and updates stock levels.
•	Prototype: void sold_products();
•	Parameters: None
•	Return Value: None
12. restock_products()
•	Identifies and displays products that need restocking.
•	Prototype: void restock_products();
•	Parameters: None
•	Return Value: None
13. main()
•	The main function that handles user interaction and drives the application flow.
Data Structures
•	Product Structure: 
o	id: Unique product identifier
o	name: Product name
o	price: Product price
o	quantity: Current stock quantity
o	items_sold: Total items sold
•	User Structure: 
o	username: User's username
o	password: User's password
Global Variables
•	fileName: Stores the unique inventory file name for the logged-in user
•	products: Array to store product information
•	product_count: Tracks the number of products in the inventory
