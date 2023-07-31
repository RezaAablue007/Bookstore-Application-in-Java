# Bookstore Application, created using Java and JavaFX

## Application Name
Bookstore App

## Participating Actors
Owner, Multiple Clients/Customers

## Entry Conditions
Participating actors are logged into the application with a unique username and password. The loginVerification method (abstract method) checks and verifies the entered username and password to allow the user to log in to the application.

## Flow of Events

1. Customer Flow:
a. The customer logs into the application by entering their username and password, gaining access to the customer start screen.
b. The start screen displays a welcome message, along with their points and status, above the table of available books. The table shows all available books in the store, along with their prices.
c. The customer has the option to select books they want to buy, redeem points, and then buy books or log out.
d. If the customer chooses to add books, they can proceed to pay with either redeemable rewards points or money. The total cost is displayed along with their updated rewards points balance and member status (silver or gold).
e. The customer can then choose to buy another book or log out if needed.

2. Owner Flow:
a. The owner logs in and gains access to their start screen, which provides options between "books," "customers," and "log-out" buttons.
b. If the owner chooses "books," they can access a screen displaying a table with all the books in the store and their prices. The owner can add or delete a book from the table.
c. If the owner chooses "customers," they can access a screen displaying all the customers and their individual data, including usernames, passwords, and rewards points balance. The owner can add or delete a customer from the database.
d. Finally, the owner can log out when they finish their work.

## Exit Conditions
Both the Owner and customers have "back" and "log-out" buttons to exit the application.

## Exceptions
Owners and customers are immediately notified if the connection between them is lost.

## Special Requirements
None

## Use of Design Patterns in the Project
The State Design Pattern is used in this design project. The main idea behind using this pattern is that it allows an object to change its behavior when its internal state changes. In the program, customers have two different types of status: Silver or Gold, based on their reward points.

## How the State Design Pattern is applied
- In the class diagram, classes Gold and Silver inherit from the state class, which depends on the reward points.
- The state of a customer can be changed based on the points gained when books are bought.
- If the customer has less than 1000 reward points, they have a "Silver" status; otherwise, they have a "Gold" status.
- This is where the state design pattern application comes in: verification of a certain condition (reward points in this case) changes the state of an attribute (customer).
- By implementing the State Design Pattern, the Bookstore App can dynamically update the customer's status based on their reward points, providing different functionalities and options for Silver and Gold members.
