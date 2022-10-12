# VendingMachine
Program that simulates a vending machine.

# Features
1. Display all of the items and their respective prices when the program starts, option to exit the program.
2. The user must put in some amount of money before an item can be selected.
3. Only one item can be vended at a time.
4. If the user selects an item that costs more than the amount the user has, 
   - Display a message indicating insufficient funds 
   - Redisplay the amount the user had put into the machine.
5. If the user selects an item that costs equal to or less than the amount the user has, 
   - Display the change returned to the user. 
   - Change must be displayed as the number of quarters, dimes, nickels, and pennies returned.
6. Vending machine items must be stored in a file. 
   - Inventory for the vending machine must be read from this file when the program starts 
   - Written out to this file just before the program exits. 
   - The program must track the following properties for each item:
     - Item name
     - Item cost
     - Number of items in inventory
7. When an item is vended, the program must update the inventory level appropriately. 
   - If the machine runs out of an item, it should no longer be available as an option. 
   - Items that have an inventory level of zero must still be read from and written to the inventory file and stored in memory.

# HINT
To make change, create a Change class that takes the amount of change due to the user (in pennies) and then calculates the number of quarters, dimes, nickels, and pennies due back to the user. 
This class should have accessors for each of the coin types.

# Guidelines
1. Follow the MVC pattern
   - App class, Controller, View, Service Layer, DAO
   - Use of constructor-based dependency injection.
2. Unit tests for your DAO and Service Layer components.
3. Use BigDecimal for all monetary calculations
4. Include at least one lambda function in the solution.
5. Use application-specific exceptions 
   - Application must fail gracefully under all conditions 
   - Application-specific exceptions thrown by your Service Layer:
      - One that is thrown when the user tries to purchase an item but doesn't deposit enough money 
        - (i.e. InsufficientFundsException)
      - One that is thrown when the user tries to purchase an item that has zero inventory 
        - (i.e. NoItemInventoryException)
6. Use enums to represent the values of different coins.
7. Include an Audit DAO to log events and the time they occurred.

