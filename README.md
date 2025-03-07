# Analysis of Wildlife Strikes to Aircraft

## Project Overview
This project analyzes wildlife strikes to aircraft using FAA data. The analysis examines patterns in wildlife strikes across different airlines, airports, and years to identify trends and potential risk factors.

## Database Structure
The project uses a MySQL database with the following tables:
- **airports**: Contains airport information (ID, name, state, code)
- **flights**: Records flight details (ID, date, origin airport, airline, aircraft type)
- **conditions**: Stores weather conditions during incidents
- **incidents**: Documents wildlife strike incidents (ID, flight ID, wildlife size, impact, altitude)

## Database Connection
The database connection is no longer active to save on AWS costs. To run this project with your own database:

1. Set up an RDS MySQL instance on AWS or use your own MySQL server
2. Update the database connection parameters in the R Markdown file:
   ```r
   db_user <- 'your_username' 
   db_password <- 'your_password'
   db_host <- 'your-db-instance.region.rds.amazonaws.com'
   db_name <- 'your_database_name'
   db_port <- 3306
   ```
3. Run the R Markdown file to create tables and perform the analysis

## Key Findings

### Top Airlines with Wildlife Strikes
Analysis of the most affected airlines by wildlife strikes.

### Analysis by Airport
Identification of airports with above-average wildlife strike incidents.

### Analysis by Year
The data shows a clear upward trend in wildlife strikes from 2000 to 2011:

### Trend Visualization
The project includes visualizations of wildlife strikes over time, showing the increasing frequency of incidents.

## Technical Implementation
- **Data Processing**: R with RMySQL for database operations
- **Data Cleaning**: Custom functions for handling dates, altitudes, and missing values
- **Analysis**: SQL queries for aggregation and statistical analysis
- **Visualization**: R plotting functions for trend analysis
- **Stored Procedures**: Custom procedures for data updates and logging

## Author
Rishi Patel  
Northeastern University  
Email: patel.rishi3@northeastern.edu  

This project was completed as part of the course Database Design and Management (CS5200) at Northeastern University.