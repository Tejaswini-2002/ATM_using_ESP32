# ATM using ESP32

Requirements: Arduino IDE, ESP32 development board, data cable, Telegram app, google sheet.

Concept: 
   ATM system has to be implemented using ESP32. The user has to login with the username and password. Then make the transaction, either debit or credit. The opening balance is 15000. The username and password will be stored in google sheets and should be verified with the one entered by the user. After verification,
user has to make transaction, (either credit or debit), amount has to be entered in the multiples of 100. After transaction the summary of the transaction should be displayed in the google sheets.

Procedure:
1. In the implementation of ATM using ESP32, Telegram bot and Google sheets. Firstly we have to verify the login credentials. So a Telegram bot has been created.
2. Creation of Telegram bot: For creating bot, search for BotFather in Telegram and create a bot and note down token(will be displayed in Botfather) and Id(will be displayed in IDBot) which are unique.
3. Get the id.
4. Then write code in Arduino. Make 3 google sheets. In 1st one store username and write the app script and store that username in variable named ”User name” from google sheet. In 2nd one store password and write the app script and the password in variable named ”Password” from google sheet. In 3rd one the transactions will be updated according to debit and credit.
5. Verification of Username and Password: In Telegram bot enter ”/start” , so username will be asked to enter, enter the username. If the username matches with the one entered in the google sheets, the password will be asked to enter. Then enter the Password.
– After entering the password, if it matches with the one stored from the google sheet(storage in Password variable) it will ask if the user want to make any transaction. The user can proceed whether to credit or debit.
6. Crediting and Debiting the amount:
– If credit is the option chosen in transaction, then user has to enter number of denominations of 100, then the amount will be calculated(100* no. of denominations of 100) and will be deducted from balance available balance(balance - credited amount).
– If debit is the option chosen in transaction, then user has to enter number of denominations of 100, then the amount will be calculated(100* no. of denominations of 100) and will be added from balance available balance(balance + debited amount).
7. Verification of login credentials.
8. Updation in Google sheets The transactions made will be updated simultaneosly in the google sheet with the help of sheetupdate function in 4 columns(Credit, Debit, Total balance, Type of transaction).

you tube video link: https://www.youtube.com/watch?v=BdroWOkqNSo 


