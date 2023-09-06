# currency_conveter
This Python code creates a simple currency converter application using the Tkinter library for the graphical user interface (GUI). Here's an explanation of how the code works:

1. Importing Necessary Libraries:
   - The code imports several libraries required for building the application, including tkinter for GUI components, requests for making HTTP requests to a currency exchange rate API, datetime for displaying the current date, and tkinter.messagebox for displaying warning messages.

2. CurrencyConverter Class:
   - This class initializes and interacts with an external currency exchange rate API (https://api.exchangerate.host/latest) to fetch the latest exchange rates. It stores exchange rate data in the 'self.rates' variable.

   - The 'convert' method takes an amount, a base currency, and a destination currency as input and calculates the converted amount. If the base currency is not 'EUR' (Euros), it converts the input amount to Euros using the exchange rates. Then, it multiplies the amount in Euros by the exchange rate for the destination currency to get the converted amount. The result is rounded to two decimal places and formatted with commas every three digits for readability.

3. Main Class:
   - This class represents the main application window and inherits from the 'tk.Tk' class.

   - The GUI elements of the application are created within this class, including labels, input fields, dropdown menus for selecting currencies, and buttons for conversion and clearing.

   - The 'clear' method clears the amount entry field and the final result label.

   - The 'processed' method is triggered when the "Convert" button is pressed. It retrieves the input amount, base currency, and destination currency from the GUI components, converts the amount using the 'CurrencyConverter' class, and displays the result in the final result label. If the input is not a valid number, it displays a warning message box.

4. Main Application Setup:
   - The script's main code block initializes an instance of the 'CurrencyConverter' class, creates an instance of the 'Main' class (the main application window), and enters the main event loop using 'mainloop()' to start the GUI application.

Overall, this code creates a simple currency converter application that allows users to enter an amount in one currency, select another currency to convert to, and see the converted amount. It fetches exchange rate data from an external API to perform the currency conversion.
