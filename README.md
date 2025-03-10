Netflix Data Analysis with PostgreSQL (Windows 11): Project Documentation

1. Introduction
This document provides a detailed guide for setting up a PostgreSQL database on a Windows 11 system, importing a Netflix dataset from Kaggle, and performing basic data analysis.

2. Prerequisites
Operating System: Windows 11.
Internet Connection: For downloading PostgreSQL and the dataset.
Kaggle Account: To download the Netflix dataset.

3. Installing PostgreSQL on Windows 11
Download the Installer: Visit the official PostgreSQL website: https://www.postgresql.org/download/windows/
Download the latest installer for Windows (x86-64).
Run the Installer:
Double-click the downloaded .exe file.
User Account Control (UAC): If prompted, click "Yes" to allow the installer to make changes.
Installation Directory: Choose an installation directory (e.g., C:\Program Files\PostgreSQL\<version>) or accept the default.
Components: Select the components to install. It's recommended to include:
PostgreSQL Server
pgAdmin 4
Stack Builder
Command Line Tools
Data Directory: Choose a data directory or accept the default.
Password: Set a strong password for the postgres superuser. Remember this password!
Port: Accept the default port (5432).
Locale: Accept the default locale.
Click "Next" through the remaining steps.
Add PostgreSQL to PATH (Environment Variables):
In the Windows 11 search bar, type "environment variables" and select "Edit the system environment variables."
Click "Environment Variables..."
In the "System variables" section, select "Path" and click "Edit..."
Click "New" and add the path to the PostgreSQL bin directory (e.g., C:\Program Files\PostgreSQL\<version>\bin).
Click "OK" on all open windows.
Verify Installation:
Open Windows Terminal or Command Prompt.
Type psql -U postgres -p 5432 and press Enter.
Enter the password you set during installation.
If you see the postgres=# prompt, PostgreSQL is installed correctly.
Type \q and enter to exit the psql prompt.

5. Downloading the Netflix Dataset from Kaggle
Access Kaggle:
Open a web browser and go to www.kaggle.com.
Search for "Netflix Movies and TV Shows."
Download the Dataset:
Download the netflix_titles.csv file.
Place the file in a convenient directory (e.g., C:\Users\<YourUsername>\Downloads).

6.Launch pgAdmin 4:
Find pgAdmin 4 in your Start menu and launch it.
The first time you launch it, it may ask you to set a master password.
Connect to the PostgreSQL Server:
In the "Servers" pane, right-click on "Servers" and select "Create" -> "Server...".
In the "General" tab, give your server a name (e.g., "Local PostgreSQL").
In the "Connection" tab:
Host name/address: localhost or 127.0.0.1
Port: 5432 (default)
Username: postgres
Password: Enter the password you set during installation.
Click "Save."

7.Create the Netflix Database:

8.Import the CSV Data:
Right-click on the netflix_titles table and select "Import/Export...".
In the "General" tab:
Format: CSV
Operation: Import
File name: Browse to your netflix_titles.csv file.
Header: Yes
In the "Columns" tab, verify that the columns match the CSV file.
Click "OK."
Verify Import:
Right-click on the netflix_titles table and select "View/Edit Data" -> "All Rows."
You should see the data from the CSV file.

9. Further Analysis
Use SQL to explore the dataset further.
Consider using pgAdmin 4 for visual data exploration.
Export data to other tools for advanced analysis or visualization.
Consider using python and the psycopg2 library to connect to the database, and do more complex analysis.









