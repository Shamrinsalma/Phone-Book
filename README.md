Phone-Book
This is a Python program that implements a simple phonebook application using a MySQL database. Here's a breakdown of the code:

Importing the pymysql library

The program starts by importing the pymysql library, which is a Python wrapper for the MySQL database.

Defining the connect_db function

The connect_db function establishes a connection to the MySQL database. It takes no arguments and returns a connection object. The function uses the following parameters to connect to the database:

host: The hostname of the MySQL server (in this case, localhost). user: The username to use for the connection (in this case, root). password: The password to use for the connection (in this case, 123mysql). database: The name of the database to connect to (in this case, phonebook). Defining the welcome function

The welcome function displays a menu to the user and prompts them to enter a choice. The function returns an integer value representing the user's choice.

Defining the display_contacts function

The display_contacts function retrieves all contacts from the contacts table in the database and displays them to the user. It takes a connection object as an argument.

It uses a with statement to ensure that the cursor is properly closed after use. It executes a SELECT * query to retrieve all contacts from the contacts table. It fetches all the rows from the result set using cursor.fetchall(). If there are rows, it iterates over them and prints each contact's name. If there are no rows, it prints a message indicating that the phonebook is empty. Defining the create_contact function

The create_contact function creates a new contact in the contacts table. It takes a connection object as an argument.

It prompts the user to enter a phone number and a contact name. It checks if the contact already exists in the database by executing a SELECT query with the phone number as a parameter. If the contact does not exist, it inserts a new row into the contacts table with the provided phone number and contact name. It commits the changes to the database. It prints a success message if the contact is created successfully. Defining the check_entry function

The check_entry function retrieves a specific contact from the contacts table based on the contact's name. It takes a connection object as an argument.

It prompts the user to enter the name of the contact they wish to view. It executes a SELECT query with the contact name as a parameter. If the contact exists, it retrieves the contact's details and prints them to the user. If the contact does not exist, it prints a message indicating that the contact does not exist. Defining the delete_contact function

The delete_contact function deletes a contact from the contacts table. It takes a connection object as an argument.

It prompts the user to enter the name of the contact they wish to delete. It checks if the contact exists in the database by executing a SELECT query with the contact name as a parameter. If the contact exists, it prompts the user to confirm the deletion. If the user confirms, it deletes the contact from the database. It commits the changes to the database. It prints a success message if the contact is deleted successfully. Defining the phonebook function

The phonebook function is the main entry point of the program. It establishes a connection to the database and enters an infinite loop.

It calls the welcome function to display the menu to the user. Based on the user's choice, it calls one of the following functions: display_contacts to display all contacts. create_contact to create a new contact. check_entry to view a specific contact. delete_contact to delete a contact. Exit the program if the user chooses to exit. If the user enters an invalid choice, it prints an error message. Running the phonebook function

The program calls the phonebook function to start the phonebook application.

Overall, this program provides a simple phonebook application that allows users to create, view, and delete contacts in a MySQL database.


