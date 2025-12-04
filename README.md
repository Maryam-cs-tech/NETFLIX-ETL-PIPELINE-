Netflix ETL & Visualization Project
Project Overview

This project demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline using Python, MySQL, and Tableau.
The dataset used contains Netflix shows and movies with attributes like title, type, release year, country, duration, rating, and genres.

The main objective is to clean, process, and visualize Netflix data to gain insights on shows distribution, type, duration, country, and genres.

Technologies Used

Python (Pandas, PyMySQL) – Data cleaning and loading into MySQL

MySQL (XAMPP) – Storing the cleaned dataset

Tableau – Creating interactive dashboards for visualization

CSV – Original Netflix dataset

Project Workflow (ETL Pipeline)
1. Extract

Downloaded the Netflix dataset CSV from Kaggle.

Loaded it into Python using pandas.read_csv().

2. Transform

Handled Missing Values: Replaced NaN with None for MySQL compatibility.

Converted Dates: Converted date_added to datetime.date.

Extracted Duration: Split duration into numeric (duration_int) and type (duration_type) parts.

Filtered & Cleaned Data: Removed duplicates and ensured all columns match MySQL table schema.

3. Load

Connected to MySQL via pymysql.

Created table netflix_shows if it didn’t exist.

Inserted cleaned data using INSERT statements.

Database Schema
Column Name	Data Type	Description
show_id	VARCHAR	Unique identifier for each show
type	VARCHAR	Movie or TV Show
title	VARCHAR	Show title
director	VARCHAR	Director name
cast	TEXT	Cast names
country	VARCHAR	Country of origin
date_added	DATE	Date show was added to Netflix
release_year	INT	Year of release
rating	VARCHAR	Show rating (e.g., PG, TV-MA)
duration_int	INT	Numeric duration (minutes or seasons)
duration_type	VARCHAR	Unit of duration (min or Seasons)
listed_in	TEXT	Genre/categories
description	TEXT	Show description
Tableau Dashboard

Connected Tableau to the MySQL database (or cleaned CSV).

Created multiple interactive sheets:

Movies vs TV Shows

Shows by Country

Shows per Year

Duration Analysis

Top Genres

Combined sheets into a single dashboard.

Added interactive filters: Year, Country, Type.

Added titles and tooltips for clarity.
