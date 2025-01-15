# Dynamic Movie Booking Insights Platform

## Overview

The Dynamic Movie Booking Insights Platform is a robust solution designed to process real-time movie ticket booking data and provide actionable insights. By leveraging Snowflake’s Dynamic Tables, Streams, Tasks, and integrated Streamlit, the platform delivers a seamless analytics experience. The interactive dashboard allows businesses to track revenue, ticket sales, and booking trends with ease.

## Features
1) CDC Processing with Snowflake:
	
 	•	Uses Snowflake Streams and Tasks to process changes in booking data dynamically.
	
 	•	Captures event types like INSERT, UPDATE, and DELETE for granular insights.
 
2) Dynamic Tables:
	
 	•	Real-time aggregation and filtering of booking data.
	
	 •	Supports analytics like total revenue, tickets sold, and cancellations.
 
3) Interactive Streamlit Dashboard:
	
 	•	Visualizes insights with metrics, charts, and tables.
	
 	•	Filters bookings by date range and status.
	
 	•	Provides detailed analysis on revenue, ticket count, and booking trends.
 
4) Scheduled Refresh:
	
 	•	Automated data refreshes ensure the dashboard reflects the latest booking data.

## Technology Stack

### Backend
	
• Snowflake:

   Database, Streams, Tasks, and Dynamic Tables for real-time data processing.

### Frontend
	
 • Streamlit:
   
   For creating an interactive, user-friendly dashboard.

### Installation Guide

#### Prerequisites

1. Snowflake account with appropriate permissions.
   
2. Python 3.8+ installed locally or on a server.
   
3. pip installed for managing Python packages.

##### Step 1: Clone the Repository

```  git clone https://github.com/your-repo/dynamic-movie-booking-platform.git ``` 

```  cd dynamic-movie-booking-platform ```

##### Step 2: Configure Snowflake Environment

1. Create a Snowflake database and warehouse.
   
2.  Run the SQL script snowflake_dynamic_tables.sql in Snowflake:
   
	• This script sets up the database, tables, streams, and tasks required for the project.

##### Step 3: Install Dependencies

Install the required Python libraries:

``` pip install streamlit snowflake-snowpark-python pandas ```

##### Step 4: Launch the Streamlit Dashboard

1. Start the Streamlit app:

``` streamlit run streamlit_app.py ```

2. 
