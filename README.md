# Group Project 2
## Team Name
Group 8- City Police Departments
## Team Members
1. Jason Bui [@jasonbui](https://github.com/jjayyan)
2. Angel Chen [@angelchen](https://github.com/ac32197-create)
3. Henry Joiner[@hankjoiner](https://github.com/HankJoiner)
4. Faaris Rana [@faarisrana](https://github.com/Faariscodes)
5. Matthew Watson[@matthewwatson](https://github.com/mattwaa)

## Data Description
Chosen Database: City Police Departments (Snowflake Public Data Set)

We selected the Snowflake Public Data Set due to the variety of options present in the entire dataset. Narrowing in on the City Police Departments, this dataset immediately sparked our eye. We thought it would be very interesting to compare different crime rates both across different cities and within different zip codes of cities themselves. The data set provides descriptions of crime, their frequency, and their specific location across the cities of New York, Los Angeles, San Francisco, Houston, Chicago, and Seattle.

Tables Count: 6

Table Row Counts
- Urban Crime Attributes: 26
- Urban Crime Attributes Point-in-Time History: 26
- Urban Crime Incident Log: 18,930,573
- Urban Crime Incident Log Point-in-Time History: 80,648,291
- Urban Crime Timeseries: 11,877,422
- Urban Crime Timeseries Point-in-Time History: 31,995,035

Table Key Columns
- Urban Crime Attributes: Offense Category (VARCHAR), Measure (VARCHAR), Unit (VARCHAR), Frequency (VARCHAR)
- Urban Crime Attributes Point-in-Time History: Offense Category (VARCHAR), Measure (VARCHAR), Unit (VARCHAR), Frequency (VARCHAR), Effective Start Timestamp (DATETIME), Effective End Timestamp (DATETIME)
- Urban Crime Incident Log: Geo ID (VARCHAR), Incident ID (VARCHAR), Reporting Level (VARCHAR), Offense Category (VARCHAR), Original Description (VARCHAR), Code (VARCHAR), City (VARCHAR), Date (DATETIME)
- Urban Crime Incident Log Point-in-Time History: Geo ID (VARCHAR), Incident ID (VARCHAR), Reporting Level (VARCHAR), Offense Category (VARCHAR), Original Description (VARCHAR), Code (VARCHAR), City (VARCHAR), Date (DATETIME), Effective Start Timestamp (DATETIME), Effective End Timestamp (DATETIME)
- Urban Crime Timeseries: Date (DATETIME), Geo ID (VARCHAR), City (VARCHAR), Variable (VARCHAR), Variable Name (VARCHAR), Value (INT)
- Urban Crime Timeseries Point-in-Time History: Date (DATETIME), Geo ID (VARCHAR), City (VARCHAR), Variable (VARCHAR), Variable Name (VARCHAR), Value (INT), Effective Start Timestamp (DATETIME), Effective End Timestamp (DATETIME)


## Questions and Justification

## Data Manipulations

## Analysis and Results

## Streamlit App
