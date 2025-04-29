Expense Tracker Help Guide
This guide provides detailed instructions on using the Expense Tracker application, troubleshooting common issues, and answers to frequently asked questions.
Table of Contents

Overview
Getting Started
Using the Application
Managing Transactions
Setting Opening Balances
Managing Budgets
Viewing Summaries
Managing Notifications
Exporting and Importing Data
Using Dark Mode


Troubleshooting
FAQs
Contact

Overview
The Expense Tracker is a web-based tool designed by Santosh Phuyal to help users manage personal finances. It allows tracking of income and expenses, setting budgets, generating reports, and receiving reminders via browser notifications. The application is built with HTML, JavaScript, and Bootstrap, using localStorage for data persistence.
Getting Started

Open the Application:
Download or clone the project files.
Open index.html in a modern browser (Chrome, Firefox, Edge) by:
Hosting via a local server (e.g., python -m http.server 8000 and navigate to http://localhost:8000/index.html).
Or double-clicking index.html (note: some features may be limited without a server).




Grant Permissions:
Allow browser notifications when prompted to enable reminders.


Explore the Interface:
The main interface includes sections for balances, transactions, budgets, summaries, and transaction history.



Using the Application
Managing Transactions

Add a Transaction:
Go to the "Add New Transaction" section.
Fill in:
Type: Income or Expense.
Category: Select from predefined categories or choose "Add New Category" to create one.
Description: A brief description (e.g., "Grocery Shopping").
Amount: Positive number (e.g., 50.00).
Date: Select a date (defaults to today).
Currency: Choose a currency or add a new one.
Notes: Optional notes (e.g., "Weekly groceries").
Tags: Optional comma-separated tags (e.g., "Food, Urgent").
Status: Cleared, Pending, or Canceled.


Click "Add Transaction" to save.


Edit a Transaction:
In the "Transaction History" list, click "Edit" next to a transaction.
Modify fields in the modal and click "Save Changes".


Duplicate a Transaction:
Click "Duplicate" to create a copy of the transaction with the same details.


Delete a Transaction:
Click "Delete" to remove a transaction (no confirmation prompt, so use caution).



Setting Opening Balances

Set Balances:
In the "Opening Balances" section, enter values for "Opening Bank Balance" and "Opening Cash Balance".
Click "Save Opening Balances".


Edit Balances:
Click "Edit" to modify existing balances.


Delete Balances:
Click "Delete" and confirm to reset balances to zero.



Managing Budgets

Set Budgets:
In the "Set Budgets" section, enter budget amounts for each expense category.
Click "Save Budgets".


Budget Alerts:
If expenses in a category exceed the budget, an alert will notify you when adding or editing transactions.



Viewing Summaries

Select Period:
In the "Summary" section, choose a period (Daily, Weekly, Monthly, Current Week, Current Month, Current Year).
Optionally select a date for Daily, Weekly, or Monthly summaries.


View Details:
The summary displays income, expense, and net amounts for the selected period.



Managing Notifications

Enable Notifications:
Click the "Notifications" dropdown and select "Enable".
Confirm the action in the prompt.
Grant browser notification permission if prompted.
Notifications will appear at 8 A.M. and 8 P.M. daily, reminding you to add transactions.


Disable Notifications:
Select "Disable" from the dropdown and confirm.
Notifications will stop until re-enabled.


Notes:
Notifications require browser support for the Notification API.
Settings are saved in localStorage and persist across sessions.



Exporting and Importing Data

Export Options:
CSV: Click "Export CSV" to download a CSV file of all transactions.
Excel: Click "Save to Excel" to download an XLSX file.
PDF: Click "Save to PDF" to generate a PDF report.
Print Report: Click "Print Report" to open a printable summary.


Backup Data:
Click "Backup Data" to download a JSON file containing all data (transactions, categories, budgets, etc.).


Restore Data:
Click "Restore Data", select a JSON backup file, and upload to merge with existing data.


Import Data:
Click "Import CSV/Excel", select a CSV or XLSX file, and upload to add transactions.
Ensure the file has columns: Date, Description, Amount, Type, Currency, Category, Notes, Tags, Status.



Using Dark Mode

Click "Dark Mode" in the header to toggle between light and dark themes.
The setting is saved in localStorage and persists across sessions.

Troubleshooting

Notifications Not Appearing:
Cause: Browser does not support notifications, permission was denied, or notifications are disabled.
Fix:
Check if Notification is supported by your browser (modern browsers like Chrome, Firefox support it).
Go to browser settings and ensure notifications are allowed for the site.
Verify notifications are enabled in the "Notifications" dropdown.
Test by temporarily changing notification times in the code (e.g., edit hours === 8 || hours === 20 to current time for testing).




Error: Unchecked runtime.lastError: The message port closed before a response was received:
Cause: A browser extension (e.g., ad blocker, password manager) is sending messages that close prematurely. Logs mention chext_driver.js and chext_loader.js.
Fix:
Disable extensions one by one via chrome://extensions/ to identify the culprit.
Test in incognito mode (most extensions are disabled by default).
Host the application locally instead of on a platform that injects scripts (e.g., Cloudflare).




Warning: @import rules are not allowed here:
Cause: An extension injecting chunk-mgcl-WVGWXQR6.js uses a CSS @import rule in a Constructable Stylesheet, which is unsupported.
Fix:
Same as above: disable extensions or test in incognito mode.
Use a static server (e.g., python -m http.server) to avoid injected scripts.




Data Not Saving:
Cause: localStorage is disabled or cleared.
Fix:
Ensure localStorage is enabled in browser settings.
Avoid clearing browser data or using private browsing modes that disable storage.




Import Fails:
Cause: Invalid file format or missing required columns.
Fix:
Ensure CSV/Excel files have headers: Date, Description, Amount, Type, Currency, Category.
Check console logs for specific errors (console.warn messages).





FAQs

Q: Can I use the app offline?
A: Yes, after the initial load (CDN dependencies), the app works offline using localStorage. Notifications and data persistence will function normally.


Q: How do I reset all data?
A: Clear the browser’s localStorage for the site via developer tools (Application > Storage > Local Storage) or manually delete all transactions and balances.


Q: Why don’t notifications show up?
A: Ensure notifications are enabled, browser permissions are granted, and the browser supports the Notification API. See Troubleshooting.


Q: Can I add my own notification times?
A: Currently, notifications are fixed at 8 A.M. and 8 P.M. To customize, modify the startNotifications method in index.html (search for hours === 8 || hours === 20).


Q: Is my data secure?
A: Data is stored in localStorage on your device and not transmitted. Use backups to save data securely, and avoid sharing JSON backup files.



Contact
For support or feature requests, contact Santosh Phuyal via [insert contact method, e.g., email or GitHub issues]. Please include:

A description of the issue or request.
Browser and version used.
Any console errors or screenshots.

For detailed setup instructions, refer to README.md.
