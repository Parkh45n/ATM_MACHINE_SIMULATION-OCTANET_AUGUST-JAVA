# ATM_MACHINE_SIMULATION-OCTANET_AUGUST-JAVA
here i upload all my project task of OCTANET_AUGUST Internship of Java Development
---------------------------------------------------------------------------------------

This Java program simulates a simple ATM (Automated Teller Machine) system. The program allows a user to perform basic banking transactions such as checking the account balance, withdrawing money, depositing money, changing the PIN, and viewing transaction history. 

The program is divided into two main classes:

1. **ATM Class**: This class contains all the necessary methods to handle the different functionalities of the ATM.
2. **ATMMachine Class**: This class contains the `main` method and is responsible for starting the program.

#### ATM Class

The `ATM` class is the core of the program and is responsible for handling all the operations related to the ATM. Let's go through each component of the `ATM` class:

- **Variables**:
  - `Balance`: This is a `float` variable that holds the account balance of the user.
  - `PIN`: This is an `int` variable that holds the current PIN (Personal Identification Number) for the account. It is initially set to `2545`.
  - `history`: This is an `ArrayList<String>` that keeps track of all the transactions made by the user.

- **Methods**:
  
  1. **checkpin()**:
     - This method prompts the user to enter their PIN.
     - If the entered PIN matches the stored PIN (`2545` by default), the method calls the `menu()` method to display the main menu.
     - If the entered PIN is incorrect, the method prompts the user to enter the correct PIN again by recursively calling `checkpin()`.

  2. **menu()**:
     - This method displays the main menu with options for different operations: check balance, withdraw money, deposit money, change PIN, view transaction history, and exit.
     - Based on the user's choice, the corresponding method is called.

  3. **checkBalance()**:
     - This method displays the current account balance.
     - After displaying the balance, the method calls `menu()` to return to the main menu.

  4. **withdrawMoney()**:
     - This method prompts the user to enter the amount they wish to withdraw.
     - It checks if the entered amount is greater than the available balance. If it is, the method displays an "Insufficient Balance" message.
     - If the amount is less than or equal to the balance, it deducts the amount from the balance and records the transaction in the `history` ArrayList.
     - After the transaction, the method calls `menu()` to return to the main menu.

  5. **depositMoney()**:
     - This method prompts the user to enter the amount they wish to deposit.
     - It adds the entered amount to the current balance and records the transaction in the `history` ArrayList.
     - After the transaction, the method calls `menu()` to return to the main menu.

  6. **changePin()**:
     - This method allows the user to change their PIN.
     - It first prompts the user to enter the current PIN. If the entered PIN is correct, it prompts the user to enter a new PIN and updates the `PIN` variable with the new value.
     - If the entered current PIN is incorrect, it displays an "Incorrect PIN" message.
     - After changing the PIN or handling the error, the method calls `menu()` to return to the main menu.

  7. **transactionHistory()**:
     - This method displays the transaction history by iterating over the `history` ArrayList.
     - If there are no transactions, it displays a "No transactions available" message.
     - After displaying the transaction history, the method calls `menu()` to return to the main menu.

 ATMMachine Class

- **main()**:
  - The `ATMMachine` class contains the `main` method, which is the entry point of the program.
  - The `main` method creates an instance of the `ATM` class and calls the `checkpin()` method to start the process.

