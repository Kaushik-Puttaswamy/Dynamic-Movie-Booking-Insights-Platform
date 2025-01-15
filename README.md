# Dynamic Movie Booking Insights Platform

## Overview

The Dynamic Movie Booking Insights Platform is a robust solution designed to process real-time movie ticket booking data and provide actionable insights. By leveraging Snowflake’s Dynamic Tables, Streams, Tasks, and integrated Streamlit, the platform delivers a seamless analytics experience. The interactive dashboard allows businesses to track revenue, ticket sales, and booking trends with ease.

## Features

1)	Real-Time Data Processing:

    •	Tracks changes in booking data using Snowflake Streams and Tasks.

    •	Handles CDC (Change Data Capture) events like INSERT, UPDATE, and DELETE.

2)	Dynamic Insights:

    •	Aggregates data in real-time using Snowflake’s Dynamic Tables.

    •	Provides metrics such as revenue, tickets sold, cancellations, and more.

3) Integrated Streamlit Dashboard:

    •	Hosted directly in Snowflake for a zero-setup experience.
 
    •	Offers filters for date range and booking status.

    •	Visualizes data through tables, metrics, and charts.

## Technology Stack

### Snowflake

• Streams: For capturing changes in booking data.


• Tasks: To automate processing and aggregation of data.


• Dynamic Tables: To enable real-time analytics.


• Python Worksheets: For developing and running Python-based logic.


### Streamlit (Built into Snowflake)

	
• For creating the interactive and responsive dashboard.

## Setup Guide

### Step 1: Set Up Database in Snowflake

1.	Log in to your Snowflake account.

2.	Create a new worksheet.

3.	Copy the content of the snowflake_dynamic_tables.sql file into the worksheet and execute it.
	
     •	This script creates:
	
     •	The database movies and required tables.
	
     •	Streams and tasks for processing CDC events.
	
     •	Dynamic tables for analytics.

4.	Activate the tasks:

``` ALTER TASK ingest_cdc_events_task RESUME; ```


``` ALTER TASK refresh_movie_booking_insights RESUME; ```

### Step 2: Launch the Streamlit Dashboard
	
 1.	Open a Python Worksheet in Snowflake.
	
 2.	Copy the contents of the streamlit_app.py file into the worksheet.
	
 3.	Click the Run button in the worksheet to ensure no errors occur.
	
 4.	Click the Streamlit button (usually located in the top-right corner of the worksheet) to launch the interactive dashboard.

## Using the Dashboard

### Filters
	
 • Date Range: Filter booking data by selecting a specific date range.
	
 • Booking Status: Filter bookings by status (BOOKED, CANCELLED, COMPLETED, or all).

### Insights

#### Metrics:

   • Total Bookings
 
   • Total Tickets Sold
 
   • Total Revenue
 
#### Charts:
  
   • Revenue by Booking Status
 
   • Tickets Sold by Status
 
   • Bookings and Revenue by Movie
 
#### Tables:

   • Detailed revenue and booking data by movie or status.

## Folder Structure

dynamic-movie-booking-platform/

│

├── snowflake_dynamic_tables.sql  # Snowflake SQL script for database setup

├── streamlit_app.py              # Streamlit app for the interactive dashboard

├── README.md                     # Project documentation

└── requirements.txt              # Python dependencies 

