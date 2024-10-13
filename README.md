## Project: APS News Updates Notifier
### Project Overview:
The APS News Updates Notifier is a Python-based project that automates the task of monitoring a specific web page for updates. It utilizes web scraping techniques to extract update dates and content, compares new data with previously scraped data, and notifies users via email if any new updates are detected. This project is scheduled to run daily using PowerShell scripts and Windows Task Scheduler, ensuring that updates are regularly checked and reported without manual intervention.

### Key Features:
#### Web Scraping:

The project scrapes a web page to extract update dates and other relevant content.
It uses BeautifulSoup and lxml for parsing the HTML structure, specifically looking for certain tags (like strong, span) where updates are mentioned.
#### Data Comparison:

The scraped data is stored in a CSV file for historical reference.
On each run, the script compares the newly scraped content with the previously stored data to identify any new or updated entries.
#### Email Notifications:

If new content is detected, the project sends an automated email with the new updates and the link to the web page.
The email content includes a summary of the new updates and a URL for the full details.
#### Automated Scheduling:

The project runs daily, automated through a PowerShell script, which is triggered by Windows Task Scheduler.
This allows the script to execute the web scraping process and data comparison without requiring manual execution.
### Tools & Technologies:
#### Python Libraries:

BeautifulSoup: For web scraping and parsing HTML content.
Pandas: To handle data storage and comparison between old and new data in CSV format.
Yagmail: For sending email notifications.
OS: For managing environment variables and automating the process.
#### Automation:

PowerShell Scripts: Used to schedule the Jupyter notebook execution.
Windows Task Scheduler: Automates the daily run of the PowerShell script.
#### Data Storage:

CSV File: Stores historical scraped data for easy comparison and detection of changes.
Process Flow:
Initial Scrape:

The project scrapes the page and stores the update information (e.g., dates and content) into a CSV file.
#### Daily Checks:

On the next scheduled execution, the project scrapes the page again and compares the newly scraped data with the stored data.
If new updates are found, they are flagged for notification.
#### Email Alerts:

If changes or new updates are detected, an email is automatically sent to the recipient(s) with details of the updates and a link to the website.
Scheduling:

A PowerShell script schedules the execution of the Jupyter notebook daily via Windows Task Scheduler.
How it Works:
Web Scraping: BeautifulSoup scrapes the page and extracts update information (e.g., date and content).
Data Comparison: The scraped data is compared with the CSV file to detect new updates.
Email Notification: If new updates are found, an email is sent to a predefined recipient list with the updated content.
Automation: PowerShell script and Task Scheduler run the Jupyter notebook daily to automate the entire process.
Project Benefits:
Ensures that users are always informed about updates on the monitored web page.
Reduces the manual effort required to check for updates and send notifications.
The process is fully automated, running in the background with no manual intervention needed after setup.

#### Another Kind Note -  Please dont judge the code and the flow its just a fun project that me and my friend did :)) ALSO IT WORKS LOL
