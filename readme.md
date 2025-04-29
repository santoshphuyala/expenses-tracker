Expense Tracker
A web-based application to manage personal finances by tracking income and expenses. Designed by Santosh Phuyal, this tool offers a user-friendly interface with features like dynamic categories, budgeting, data export/import, and browser notifications.
Features

Transaction Management: Add, edit, duplicate, or delete income and expense transactions with descriptions, amounts, categories, dates, currencies, notes, tags, and statuses.
Balance Tracking: Monitor total, bank, cash, and transaction balances with customizable opening balances.
Dynamic Categories and Currencies: Add custom categories and currencies on-the-fly.
Budgeting: Set budgets for expense categories with alerts for overspending.
Data Management: Export/import data in CSV/Excel, generate PDF reports, and backup/restore data in JSON format.
Summary Reports: View daily, weekly, monthly, or custom period summaries.
Notifications: Receive browser notifications at 8 A.M. and 8 P.M. to remind you to add transactions, with enable/disable options.
Dark Mode: Toggle between light and dark themes for better usability.
Responsive Design: Built with Bootstrap for a seamless experience on desktop and mobile.

Installation

Clone or Download:
Clone this repository: git clone <repository-url> or download the ZIP file.


Host Locally:
Place the project files in a web server directory (e.g., htdocs for XAMPP or www for WAMP).
Alternatively, use a simple HTTP server like Python’s: python -m http.server 8000 in the project directory.


Open in Browser:
Navigate to http://localhost:8000/index.html (adjust port if necessary).


Dependencies:
No installation required; all dependencies (Bootstrap, jsPDF, XLSX) are loaded via CDN.



Usage

Access the Application:
Open index.html in a modern browser (Chrome, Firefox, Edge recommended).


Add Transactions:
Fill out the "Add New Transaction" form with details like description, amount, type, and category.
Use optional fields for notes, tags, and status.


Manage Notifications:
Use the "Notifications" dropdown to enable/disable reminders (8 A.M. and 8 P.M.).
Confirm permission for browser notifications when prompted.


View Summaries:
Select a period (daily, weekly, etc.) and date to view financial summaries.


Export/Import Data:
Use buttons to export to CSV, Excel, or PDF, or backup/restore data.


Toggle Dark Mode:
Click "Dark Mode" to switch themes.



Requirements

Modern web browser with JavaScript enabled.
Internet connection for initial CDN loads (Bootstrap, jsPDF, XLSX).
Optional: Local web server for testing (e.g., Python’s HTTP server, XAMPP).

Troubleshooting

Notifications Not Working: Ensure browser notification permissions are granted. Check HELP.md for details.
Errors in Console: If you see Unchecked runtime.lastError or @import rules are not allowed here, disable browser extensions or test in incognito mode (see HELP.md).
Data Not Persisting: Ensure localStorage is not cleared by the browser.

Contributing
Contributions are welcome! Please:

Fork the repository.
Create a feature branch (git checkout -b feature-name).
Commit changes (git commit -m 'Add feature').
Push to the branch (git push origin feature-name).
Open a Pull Request.

License
This project is licensed under the MIT License. See LICENSE for details.
Author
Designed and developed by Santosh Phuyal.
For detailed usage and troubleshooting, refer to HELP.md.
