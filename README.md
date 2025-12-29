# Zara Database

## Description
The Zara database includes an E-R diagram, a relational model, data definition language, data generation and population, and a command line. Together, they create a functional interactive database environment. This is a valuable project because it provides a realistic simulation of Zara's core business operations and enables data driven decision making. The command line, where the user interacts with the database, is an accessible platform for customers and managers of Zara. Customers have the option to make a member account, place an order, view order details, add new payment information to their account, and change their personal information. Managers have the ability to view individual store trends, customer trends, overall company trends, and add inventory to the store or warehouse.

## Where to find necessary components
The E-R diagram and relational model are included as screenshots in our write ups. The data definition language is in the ‘CREATINGTABLES.ipynb’ file, the data generation and population code is in the ‘DATAGENERATION.ipynb’ file, and the command line is in the ‘COMMANDLINE.ipynb’ file.

## How to install and run the project

1. Packages to install if not installed already:
python-dotenv
mysql-connector-python
pandas 
Faker
random
datetime
sys 
Running all of the three ipynb files will load in the required modules.

2. Creating and filling the database
- create a new database connection in mysql 
- Open each ipynb file in Jupyter Notebook
- in the example.env file, change the information of user, password, host, and database to your personal mysql database information to be reflected in ‘DATAGENERATION.ipynb’, ‘COMMANDLINE.ipynb’, and ‘CREATINGTABLES.ipynb’ files. then copy this information into a .env file.
- Run all cells of ‘CREATINGTABLES.ipynb’
- Run all cells of ‘DATAGENERATION.ipynb’
- Scroll down to the bottom of the file to the second to last cell that has the output “Data population successful!” Rerun just this cell. After re-running, the output should be executed queries. After doing so, all the data will be correctly populated.
- Run all cells of ‘COMMANDLINE.ipynb’

## How to use the command line
The command line prompts the user for input
For testing purposes, use id’s ranging from 1-10 to account for limited data population

The command line could be used to look at our generated data by:
- Saying you are a customer (1)
- Saying you are part of the membership program (1)
- Enter your customer id (any number less than 10)
- View your order details (2)
- Enter your order number you would like to view (number 1-10)
- Press enter
- Change your personal information (4)
- Enter the personal information you would like to change
- Type either yes or no
- This allows you to see order details for a generated customer and allows you to see the generated customers personal information

The command line could be used to add data to the database by:
- Saying you are a customer (1)
- Saying you are part of the membership program (1)
- Enter your customer id (any number less than 10)
- Add a new payment method (3)
- Enter either credit or gift
- Enter your name if it is a credit card
- Enter a 16 digit number for the credit or gift card
- Add a 3 digit cvv for the credit or gift card
- Add a balance if it is a gift card
- Add an expiration date if it is a credit card in the form of YYYY-MM-DD that is in the near future
- Press enter
- Then place an order (1)
- Enter a product_id that is in stock at the store, options are shown 
- Enter a quantity of that product that is in stock, stock is shown as quantity of the product
- Type yes or no depending on if you want to add another product
- Enter a payment_id from the options shown to choose what payment you want to use with the order
- Press enter
- Then you could view order details (2)
- And enter the order_id that was just generated from the order you placed

This allows you to enter a new payment type and then when you place an order it shows you all your valid payment types, which shows that the payment type you just added was added to the database. It also allows you to show that an order was added correctly to the database. Another option you have to run would be to order n-10 of quantity n of a product, meaning to run the quantity down to 10. Then place the order. Then you could go back and place another order and you should see that the quantity of that product you ordered would be 110, and not 10 anymore because a reorder was triggered.

You are also able to create a new member account, then log in with your new customer_id and then place an order as a new member. You could also just place an order as a guest.

To view the analytical queries:
- Say you are a store manager (2)
- View store and member trends (1)
- Then go through clicking options 1-4
- Then click 5 to go back
- Then view overall zara trends (2)
- Then go through clicking options 1-5

You also have the option to add inventory to the warehouse and store. 

If you want to start the menu from the beginning, you can pause the code chunk, and then rerun the last code chunk that includes the main function.

## Collaborators
Cianna Grama and Carly Trapeni created the Zara database project and application. Please let us know if you have any difficulties running the application. We hope you enjoy interacting with our Zara database!
