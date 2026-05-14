Project Overview:

The Bank Account Management System is a file-based application developed in the C programming language using random-access file handling techniques. The system is designed to manage customer account information efficiently by storing records in a binary file (credit.dat).
This application enables users to perform essential banking operations such as creating new accounts, updating account balances, deleting existing records, and generating a formatted report of all customer details.
The project mainly focuses on implementing binary file processing, structured data storage, and direct record manipulation using random-access methods.

Features:
i)Creation of new customer account records
ii)Updating account balance information
iii)Deletion of existing account records
iv)Generation of formatted text reports
v)Random-access data retrieval and modification
vi)Binary file storage for efficient processing
vii)Menu-driven user interface
viii)Structured and modular program design

Concepts Used:
The project incorporates several important concepts of C programming and file management.
 i)Structures:
Structures are used to store customer account details such as:
1.Account Number
2.Customer Name
3.Account Balance
struct clientData
{
    unsigned int acctNum;
    char lastName[15];
    char firstName[10];
    double balance;
};

ii)Random Access File Handling
The program uses random-access techniques to directly locate specific records in the file without reading all previous records sequentially.
iii)Binary File Processing
Account records are stored in binary format using:
1.fread()
2.fwrite()

iv)Modular Programming
The program is divided into separate functions for better readability and maintainability.
Functions used include:
1.textFile()
2.updateRecord()
3.newRecord()
4.deleteRecord()
5.enterChoice()

v)Menu-Driven Interface
A menu-based system allows users to interact with the application easily and perform operations based on their requirements.

vi)File Handling Functions Used
Function	             Description
fopen()	              Opens a file in the specified mode
fclose()	             Closes the opened file
fread()	               Reads binary data from a file
fwrite()	             Writes binary data into a file
fseek()	               Moves the file pointer to a specified position
rewind()               Resets the file pointer to the beginning
fprintf()	             Writes formatted output to a text file

Algorithm
Step 1: Start the Program
Open the binary file credit.dat in read/write mode.
If the file cannot be opened, terminate the program with an error message.
Step 2: Display Main Menu
Display the list of available operations:
1 - Generate formatted text file
2 - Update account information
3 - Add new account
4 - Delete account
5 - Exit

Step 3: Execute Selected Operation

Option 1 – Generate Text File
Read all records from the binary file
Filter valid account records
Store formatted account details in accounts.txt

Option 2 – Update Existing Account
Accept account number from the user
Locate the corresponding record using fseek()
Read the existing account details
Modify the balance
Write the updated record back into the file

Option 3 – Add New Account
Accept a new account number
Verify whether the record already exists
If the location is empty:
Read customer details
Store the new record in the appropriate file position

Option 4 – Delete Account
Accept the account number to be deleted
Locate the corresponding record
Replace the existing record with an empty structure

Option 5 – Exit
Close the file
Terminate the application

Sample Input and Output:
Enter your choice

1 - store a formatted text file of accounts called
    "accounts.txt" for printing
2 - update an account
3 - add a new account
4 - delete an account
5 - end program

Adding a New Account:

Input:
3
Enter new account number (1 - 100): 1
Enter lastname, firstname, balance
Smith John 5000

Output:
Account successfully created.

Updating an Account:
Input:
2
Enter account to update (1 - 100): 1
Enter charge (+) or payment (-): 500

Output:
1     Smith          John          5500.00

Deleting an Account:
Input:
4
Enter account number to delete (1 - 100): 1

Output:
Account deleted successfully.



