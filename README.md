# Inventory Management System - C Project (PRG255)

## Overview
This project is a console-based Inventory Management System developed in C. The system provides functionalities to manage a simple inventory for a small store, allowing users to add, sell, and update items, as well as view profits and save/load data. It was created as part of the PRG255 course by **Vansh Dave**.

## Features
- **View Inventory**: Displays the current items in stock, showing their name, ID, cost, quantity in stock, and total value.
- **Sell Items**: Allows users to select an item by ID and record a sale, updating the stock and calculating the total profit.
- **Order Existing Items**: Increase the stock quantity of an existing item.
- **Order New Items**: Add new items to the inventory by entering details such as name, ID, cost, and initial stock.
- **Profit Calculation**: View detailed profit for each item and the overall profit of the store.
- **Data Persistence**: Inventory data is saved to a file (`inventory_data.txt`) and can be reloaded when the program starts, ensuring data persistence across sessions.

## How to Compile and Run
1. **Clone the Repository**:  
   ```
   git clone https://github.com/yourusername/inventory-management-system.git
   ```
2. **Compile the Program**:  
   Use a C compiler such as `gcc` to compile the code:  
   ```
   gcc -o inventory main.c
   ```
3. **Run the Program**:  
   ```
   ./inventory
   ```

## Program Usage
The application provides a simple menu-driven interface. Upon running, you can select from the following options:

1. **Show items in inventory (a)**  
   Displays all items currently in stock, showing the ID, quantity, unit cost, and total value for each item.

2. **Sell an item (b)**  
   Allows you to enter an item ID and quantity sold, updating the inventory and profit.

3. **Show profit (c)**  
   Shows a breakdown of the profit for each item and the total profit for the store.

4. **Order more of an existing item (d)**  
   Enables you to order more stock for an existing item by specifying the item ID and quantity.

5. **Order new items (e)**  
   Add new items to the inventory by entering the item name, ID, cost, and initial stock.

6. **Quit and save data (f)**  
   Saves the current state of the inventory to the `inventory_data.txt` file and exits the program.

## Code Structure
- **`struct Item`**: Defines the structure for each item, including name, ID, cost, quantity in stock, quantity sold, and total profit.
- **`struct Inventory`**: Manages an array of items (`MAX_ITEMS` set to 12) and tracks the overall store profit.
- **Function Descriptions**:
  - **`displayMenu()`**: Prints the menu options for the user.
  - **`showInventory()`**: Displays the current inventory status.
  - **`sellItem()`**: Handles the sale of an item and updates stock/profit.
  - **`showProfit()`**: Displays the profit for each item and the total profit.
  - **`orderItem()`**: Updates stock quantity for an existing item.
  - **`orderNewItem()`**: Adds a new item to the inventory.
  - **`saveToFile()`**: Saves the inventory data to `inventory_data.txt`.
  - **`loadFromFile()`**: Loads inventory data from `inventory_data.txt`.

## Data Storage
The inventory data is stored in `inventory_data.txt` in the following format:

```
itemName idNumber cost quantityInStock quantitySold totalProfit
```

For example:
```
Apple 1001 0.50 30 10 7.50
Banana 1002 0.20 50 20 6.00
```

Each line corresponds to one item in the inventory, and the data is loaded automatically when the program starts.

## Limitations
- **Maximum Items**: The system can only handle up to 12 items (`MAX_ITEMS` is set to 12).
- **Static Data Size**: All data fields are stored with fixed sizes, so overflow issues may arise if data exceeds these limits.
- **Basic Error Handling**: The program handles basic input errors, but complex scenarios might not be managed properly.

## Future Improvements
- Implement dynamic memory allocation to handle a larger inventory.
- Add a graphical user interface (GUI) for improved usability.
- Include additional features like search, filtering, and report generation.

Feel free to explore and modify the project as needed!

## License
This project is open-source and available under the MIT License.
