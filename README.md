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
Question 1: 
How does the time of year influence crime frequency? Analyze trends by season (Spring, Summer, Fall, Winter) and determine whether certain seasons show statistically higher concentrations of violent incidents.
Columns used: date, offense category
Relevance? The police and the city need to understand how crime fluctuates seasonally for both operational efficiency and public safety. Law enforcement and city officials have to be able to anticipate periods of increased crime to allocate resources effectively for both internal and external factors. This question is non-trivial because the relationship between season and crime is not uniform across cities or crime types. There are a range of factors affecting the crime rate, which makes it vary significantly and requires data-driven analysis. 

Question 2: 
What are the most frequently reported crime types within each city?
columns used: city, offense category 
Relevance? Understanding what crimes are most prevalent in different cities is important to understand for public safety and operational efficiency. Depending on what kind of crime it is, more violent or less, it changes how citizens view an area and what precautions must be taken. The focus on the city changes how we view things and eliminates a one-size-fits-all approach. Also, how we would approach something like burglary would be different then assualt or drug-related crimes. This question is non-trivial because the relationship between crime type and city is not correlated, and many different factors go into why these different crimes are more related in one area vs another. 

## Data Manipulations
Question 1:
<img width="549" height="449" alt="Screenshot 2026-04-27 at 11 59 43 AM" src="https://github.com/user-attachments/assets/5099ba7b-2a30-4a54-9f87-e65d45abe3b9" />


Question 2:
<img width="932" height="262" alt="image" src="https://github.com/user-attachments/assets/da08b065-20ce-40c8-89b2-d56061268ee4" />
The count (*) query is to count the occurrence of incidents to then be able to group them by offense_category to be able to compare each category of crime presented in each city. Group by city is used so that the crimes can be compared by each city.

## Analysis and Results
Question 1:
<img width="1052" height="258" alt="Screenshot 2026-04-27 at 11 56 03 AM" src="https://github.com/user-attachments/assets/e5f4791b-f85f-4276-a940-350767aba443" />

Question 2:
<img width="1382" height="623" alt="image" src="https://github.com/user-attachments/assets/2a1f89c1-f66d-49a7-87f2-e4550ae4da54" />
<img width="1373" height="625" alt="image" src="https://github.com/user-attachments/assets/d640975a-9a0d-46df-8cf8-e43a8be7c17e" />

The results show 

## Streamlit App
