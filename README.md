# Netflix Data Analysis with PostgreSQL (Windows 11)

This project demonstrates how to set up a PostgreSQL database on Windows 11, import a Netflix dataset from Kaggle, and perform basic data analysis using pgAdmin 4.

## Table of Contents

-   [Introduction](#introduction)
-   [Prerequisites](#prerequisites)
-   [Installation](#installation)
    -   [PostgreSQL](#postgresql)
-   [Dataset](#dataset)
    -   [Downloading from Kaggle](#downloading-from-kaggle)
-   [Database Setup](#database-setup)
    -   [Using pgAdmin 4](#using-pgadmin-4)
        -   [Connecting to the Server](#connecting-to-the-server)
        -   [Creating the Database](#creating-the-database)
        -   [Creating the Table](#creating-the-table)
        -   [Importing the Data](#importing-the-data)
-   [Schema Overview](#schema-overview)
-   [Example Queries](#example-queries)
-   [Further Analysis](#further-analysis)

## Introduction

This project aims to provide a clear and concise guide for setting up a PostgreSQL database for Netflix data analysis on a Windows 11 system. It utilizes pgAdmin 4 for database management and querying.

## Prerequisites

-   Windows 11
-   Internet connection
-   Kaggle account

## Installation

### PostgreSQL

1.  Download the PostgreSQL installer from [www.postgresql.org/download/windows/](www.postgresql.org/download/windows/).
2.  Run the installer and follow the on-screen instructions.
3.  Remember the password you set for the `postgres` user.
4.  Add the PostgreSQL `bin` directory to your system's `PATH` environment variable.

## Dataset

### Downloading from Kaggle

1.  Go to [www.kaggle.com](www.kaggle.com) and search for "Netflix Movies and TV Shows."
2.  Download the `netflix_titles.csv` file.

## Database Setup

### Using pgAdmin 4

1.  Launch pgAdmin 4.

#### Connecting to the Server

1.  Right-click "Servers" and select "Create" -> "Server...".
2.  Enter connection details (hostname, port, username, password).

#### Creating the Database

1.  Right-click "Databases" and select "Create" -> "Database...".
2.  Name the database "netflix".

#### Creating the Table

1.  Right-click "Tables" and select "Create" -> "Table...".
2.  Create columns:
    -   `show_id` VARCHAR(10) (Primary Key)
    -   `type` VARCHAR(10)
    -   `title` VARCHAR(255)
    -   `director` VARCHAR(255)
    -   `cast` TEXT
    -   `country` VARCHAR(255)
    -   `date_added` VARCHAR(50)
    -   `release_year` INTEGER
    -   `rating` VARCHAR(10)
    -   `duration` VARCHAR(20)
    -   `listed_in` TEXT
    -   `description` TEXT

#### Importing the Data

1.  Right-click the table and select "Import/Export...".
2.  Select CSV format and the `netflix_titles.csv` file.
3.  Verify column mapping and import.

## Schema Overview

-   `show_id`: Unique show identifier.
-   `type`: Movie or TV Show.
-   `title`: Title.
-   `director`: Director(s).
-   `cast`: Cast members.
-   `country`: Country(ies).
-   `date_added`: Date added to Netflix.
-   `release_year`: Release year.
-   `rating`: TV rating.
-   `duration`: Duration.
-   `listed_in`: Genres.
-   `description`: Description.


## Further Analysis

-   Explore the data using SQL queries in pgAdmin 4.
-   Export data for further analysis in other tools.
-   Consider using Python and `psycopg2` for more complex analysis.
