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
Columns used: date, value, and variable
Relevance? The police and the city need to understand how crime fluctuates seasonally for both operational efficiency and public safety. Law enforcement and city officials have to be able to anticipate periods of increased crime to allocate resources effectively for both internal and external factors. This question is non-trivial because the relationship between season and crime is not uniform across cities or crime types. There are a range of factors affecting the crime rate, which makes it vary significantly and requires data-driven analysis. 

Question 2: 
What are the most frequently reported crime types within each city?
columns used: city, offense category, count(*) as incident_count
Relevance? Understanding what crimes are most prevalent in different cities is important to understand for public safety and operational efficiency. Depending on what kind of crime it is, more violent or less, it changes how citizens view an area and what precautions must be taken. The focus on the city changes how we view things and eliminates a one-size-fits-all approach. Also, how we would approach something like burglary would be different then assualt or drug-related crimes. This question is non-trivial because the relationship between crime type and city is not correlated, and many different factors go into why these different crimes are more related in one area vs another. 

## Data Manipulations
Question 1:
<img width="549" height="449" alt="Screenshot 2026-04-27 at 11 59 43 AM" src="https://github.com/user-attachments/assets/5099ba7b-2a30-4a54-9f87-e65d45abe3b9" />
The first case when statements is used to categorize the months by their seasons. The sum adds the total number of crimes incidents within each season. The last formula is used to average the daily crime rate by season. The where clause narrows down the crime into violent crimes. The final case when statement is used to chronologically order the season.,

Question 2:
<img width="932" height="262" alt="image" src="https://github.com/user-attachments/assets/da08b065-20ce-40c8-89b2-d56061268ee4" />
The count (*) query is to count the occurrence of incidents to then be able to group them by offense_category to be able to compare each category of crime presented in each city. Group by city is used so that the crimes can be compared by each city.

## Analysis and Results
Question 1:
<img width="1052" height="258" alt="Screenshot 2026-04-27 at 11 56 03 AM" src="https://github.com/user-attachments/assets/e5f4791b-f85f-4276-a940-350767aba443" />
<img width="767" height="259" alt="Screenshot 2026-04-27 at 12 12 42 PM" src="https://github.com/user-attachments/assets/23b23367-55b6-4dcc-92c8-e8acf8b27701" />
This chart shows the amount of violent crime per season and the average daily crime rate per season. The results show that the amount of violent crime committed peaks during the summer time, then decreases as it gets colder, with the lowest amount being in winter. This means in terms of resource allocation, staffing, overtime budget, and proactive policing should be increased during the warmer seasons and decreased for the colder seasons. 

Question 2:
<img width="1382" height="623" alt="image" src="https://github.com/user-attachments/assets/2a1f89c1-f66d-49a7-87f2-e4550ae4da54" />
<img width="1373" height="625" alt="image" src="https://github.com/user-attachments/assets/d640975a-9a0d-46df-8cf8-e43a8be7c17e" />

The results show indicate the rate at which specific crimes occur in each of the cities within our data. The chart shows specifically which crimes occur in the highest numbers in each city. Theft is bar far the most common type of crime according to the graph. The bar graph then allows local police departments to prioritize resource allocation to curb the occurrences of the highest counts of crimes. The charts also allow the general public to get a broader idea of what crimes may affect them in their daily lives. The chart also shows that a larger population does not always indicate a higher amount of crime incidents. 


## Streamlit App
Question 1:
<img width="1656" height="621" alt="image" src="https://github.com/user-attachments/assets/f771d1f6-7790-469f-b331-342ca22e2994" />
<img width="1706" height="752" alt="image" src="https://github.com/user-attachments/assets/3e407e2e-050a-4e16-b5c1-727a5879c531" />

The "Violent Incidents by Season" feature provides a clear breakdown of crime frequency across all four seasons, displaying the total incident count and the percentage change between seasons .This can help departments quickly gauge whether crime is trending upward or downward as the year progresses. The app also offers full customization of the crime database, enabling users to select which crime types to include and distinguish them by color.

Question 2:
<img width="1381" height="634" alt="image" src="https://github.com/user-attachments/assets/46ed3f91-00a1-400f-8811-aa9098579c93" />
<img width="1723" height="859" alt="image" src="https://github.com/user-attachments/assets/e4489aec-cda9-4bef-a8dd-faf2eb6f9648" />

The "Urban Crime Incident Dashboard" leverages a dropdown function to group incident counts by city, providing departments with a comprehensive view of all crime categories spanning the past 15 years. This tool proves valuable insight  for tracking future crime trends and helping departments identify recurring patterns among the most popular crimes based on each city.

AI was used  in the stream report to offer key insight at the bottom of the charts
