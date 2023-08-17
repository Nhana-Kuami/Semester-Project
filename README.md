# Semester-Project
Name: Boateng Francis
Idex Number: UEB3257222
Class: I.T C 
Project Description;
Q: What is the purpose of this code?
A: The purpose of this code is to simulate a simple banking and cryptocurrency trading system. It defines a class Account that represents a user account with functionalities to deposit and withdraw money, buy and sell cryptocurrencies (Dogecoin and Bitcoin), view account information, view transaction history, and clear transaction history. The main function provides a menu-driven interface for users to interact with their account and perform these actions.

Q: What is the significance of the Account class?
A: The Account class is the central component of the code. It encapsulates the behavior and data of a user's account, including their balance, cryptocurrency holdings, transaction history, and more. It provides methods to perform various financial transactions and manage the account's state.

Q: What are the attributes of the Account class?
A: The attributes of the Account class include:

int dogecoin, balance, bitcoin, deposit, withdraw, total_equity, dogecoin_value, bitcoin_value, crypto_invest, crypto_return: These variables store information about the account's balance, cryptocurrency holdings, transaction values, and equity.
vector<pair<string, int>> transactions: This vector holds pairs of strings (transaction type) and integers (transaction amount) to keep track of the account's transaction history.
Q: How is the initial state of an Account object defined?
A: The initial state of an Account object is defined in the constructor of the class. It initializes the total_equity, balance, dogecoin, bitcoin, withdraw, deposit, dogecoin_value, bitcoin_value, crypto_invest, and crypto_return attributes with appropriate values.

Q: How are transactions stored and displayed in the Account class?
A: Transactions are stored in the transactions vector using pairs of strings and integers, where the string indicates the type of transaction (e.g., "Deposit:", "Withdraw:", "Bitcoin Sold:", "Dogecoin Sold:") and the integer represents the transaction amount. The History method iterates through the transactions vector to display the details of each transaction.

Q: How does the user interact with the program?
A: The user interacts with the program through a menu-driven interface provided by the main function. The user is prompted to choose options to view account information, deposit money, withdraw money, view transaction history, buy cryptocurrencies, sell cryptocurrencies, or exit the program.

Q: How are cryptocurrency purchases and sales simulated?
A: Cryptocurrency purchases and sales are simulated by the BuyCrypto and SellCrypto methods in the Account class. The user is prompted to choose which cryptocurrency to buy or sell. A random factor is introduced with the help of the rand() function to determine whether the transaction is successful or not. If successful, the appropriate amount of cryptocurrency is added or removed from the account, and the balance is updated accordingly.

Q: How is the random factor used in cryptocurrency transactions?
A: The random factor is used to simulate a degree of luck or chance in cryptocurrency transactions. The code uses the rand() function to generate a random integer. If this random integer is evenly divisible by 251, the transaction is considered successful, and the user's cryptocurrency holdings and balance are updated accordingly. If the random integer doesn't meet this condition, the transaction fails.

Q: What happens if the user tries to withdraw more money than their balance?
A: If the user tries to withdraw more money than their balance, the Withdraw method returns false, indicating that the withdrawal was unsuccessful. The balance remains unchanged, and an appropriate message is displayed to the user.

Q: What happens if the user tries to sell a cryptocurrency they don't have?
A: If the user tries to sell a cryptocurrency they don't have (e.g., selling Bitcoin when the Bitcoin holdings are 0), the SellCrypto method returns false, indicating that the sale was unsuccessful. The user's cryptocurrency holdings and balance remain unchanged, and an appropriate message is displayed to the user.

Q: How does the program handle the clearing of transaction history?
A: The History method displays the user's transaction history and prompts the user whether they want to clear the transaction history or not. If the user confirms (by entering 'Y' or 'y'), the transactions vector is cleared, and the number of cleared transactions is displayed. If the user declines, the total number of transactions is displayed without clearing the history.
This is a C++ code that defines an Account class with several member functions. The Account class has the following private member variables:

dogecoin: an integer representing the number of dogecoins in the account.
balance: an integer representing the balance in the account.
bitcoin: an integer representing the number of bitcoins in the account.
deposit: an integer representing the amount of money deposited into the account.
withdraw: an integer representing the amount of money withdrawn from the account.
total_equity: an integer representing the total equity in the account.
dogecoin_value: an integer representing the value of a dogecoin.
bitcoin_value: an integer representing the value of a bitcoin.
crypto_invest: an integer representing the amount of money invested in cryptocurrency.
crypto_return: an integer representing the return on investment in cryptocurrency.
transactions: a vector of pairs of strings and integers, where each pair represents a transaction and its amount.
The class has several member functions:

Deposit(int money): a function that takes an integer argument and adds it to the balance. It also adds a transaction to the transactions vector.
GetAccountInformation(): a function that prints out information about the account, including bank balance, dogecoins, and bitcoins.
Withdraw(int money): a function that takes an integer argument and subtracts it from the balance if there is enough money in the account. It also adds a transaction to the transactions vector.
BuyCrypto(): a function that prompts the user to choose between buying dogecoin or bitcoin. If there is enough equity in the account, it randomly generates a number between 0 and 250. If this number is 0, it buys one unit of cryptocurrency and subtracts its value from the balance. It also adds a transaction to the transactions vector. If this number is not 0, it returns false. If there is not enough equity in the account, it returns false.
