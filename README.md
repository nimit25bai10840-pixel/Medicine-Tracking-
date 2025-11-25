**Medicine-tracking**
This project is a console-based application program developed in Python designed to simulate a basic inventory management system for a small pharmacy . It serves as a practical demonstration of fundamental programming concepts, including data structures, modular programming using functions, and persistent data storage through file handling. Medicine Inventory Tracker For screenshots, kindly refer the screenshotsbranch of repository Project Overview

The Medicine Inventory Tracker is a simple, console-based application built in Python 3 designed for managing medical stock. This project demonstrates core programming concepts, including modular function design, persistent file I/O, and robust input validation using if/else conditional logic. It is ideal for small clinics or pharmacies needing a straightforward stock management solution.

**Key Features**

**Menu-Driven Interface**: Easy navigation through five distinct options.

**Data Persistence**: Saves inventory data to and loads it from inventory.txt upon startup and exit.

**Stock Management**: Functions to add new medicine and update the quantity of existing stock (add or remove).

**Low Stock Alerts**: Automatically flags items falling at or below the defined LOW_STOCK_INDICATOR (default: 10).

**Explicit Validation**: Uses the .isdigit() method and if/else statements to validate all numerical user input, ensuring data integrity. Setup and Installation

This project requires only a standard installation of Python 3.

Prerequisites Python 3.x (Installed and accessible from your terminal/command prompt)

Running the Application

**Save the Code**: Save the Python code (e.g., inventory_tracker.py) to a directory on your computer.

**Open Terminal**: Navigate to the directory where you saved the file using your command line or terminal.

**Execute the Script**: Run the following command:

**python inventory_tracker.py**

**Data File**: The application will automatically create a file named inventory.txt in the same directory to store data once you save and exit for the first time.

Usage Guide (Main Menu)

Upon launching, the program presents the main menu: 
1. Show Inventory Displays all current medicine stock in a formatted table.

2. Add New Medicine Prompts for name, initial quantity, and expiry date.

3. Update Stock Allows adding or removing (dispensing) stock from an existing item. Includes stock safety check.

4. Check Low Stock Lists all items where quantity is below the LOW_STOCK_INDICATOR.

5. Save & Exit Saves the current inventory state to inventory.txt and closes the program.

Technical Documentation and Code Details INVENTORY_FILE

"inventory.txt"

The name of the file used for persistent storage.

LOW_STOCK_INDICATOR

10

The indicator value used to trigger a low stock alert.

Core Functions and Modularity

The application is built on a foundation of independent functions, each responsible for a single task:

**load_inventory():** Handles reading the inventory.txt file and parsing the pipe-separated (|) data into the main Python dictionary. It includes explicit checks for corrupted data lines.

**save_inventory(inventory):** Writes the current dictionary data back to inventory.txt in the correct pipe-separated format.

**display_inventory(inventory):** Formats and prints the inventory data to the console in a clear, tabular layout.

**add_new_medicine(inventory):** Collects details for a new item and uses the validation helper before committing the data.

**update_stock(inventory):** Manages add or remove operations for existing items, featuring the critical stock safety check.

**check_low_stock(inventory):** Iterates through the inventory to find and report items below the LOW_STOCK_INDICATOR.

**run_inventory_tracker() (Main Loop):** Initializes the program and manages the primary menu loop.

Focus on If/Else Input Validation As per the project requirements, the application exclusively uses if/else logic for validation, demonstrating fundamental control flow principles:

**Input Type Validation:** The helper function checks if user_input.isdigit(): to confirm the input is a valid whole number string before converting it to an integer.

**Stock Safety Logic:** In the update_stock function, the check if inventory[name]['quantity'] >= change: is explicitly used to prevent the stock count from ever becoming negative during a removal operation.

**File Data Checks:** The load_inventory function uses if len(parts) == 3: to verify the expected structure of each line of data read from the file.

**Author**

**Nimit jain**

**25BAI10840# Medicine-Tracking**
