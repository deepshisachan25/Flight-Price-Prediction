# Flight-Price-Prediction
The objective of the study is to analyse the flight booking dataset obtained from Kaggle website in order to get meaningful information from it. The 'Linear Regression' statistical algorithm is used to train the dataset and predict a continuous target variable i.e. Price of the flight based on different variables. A thorough study of the data will aid in the discovery of valuable insights that will be of enormous value to passengers.

## Research Questions
Our study focuses on answering the following key questions:
a) Does the ticket price vary by airline?
I want to explore if different airlines charge different prices for similar routes.
b) How is the price affected when tickets are purchased just 1 or 2 days before departure?
Our aim to determine if booking tickets closer to the departure date significantly impacts the price.
c) Does the ticket price change based on the time of day at which flights depart or arrive?
This question explores whether the time of day at which flights depart or arrive affects the cost of tickets.
d) How does the price change with different source and destination cities?
We will examine if ticket prices vary depending on the cities between which the flights operate.
e) How does the ticket price differ between Economy and Business classes?
The study will compare prices between Economy and Business class tickets to understand the pricing structure.

## Data Collection
To gather the necessary data, went to the "Ease My Trip" website. The data was collected in two batches: one for Economy class tickets and another for Business class tickets. In total, we extracted 300,261 unique flight booking options over a period of 50 days, from February 11th to March 31st, 2022. 

The dataset provides detailed information on flight booking options between the top 6 metro cities in India. It consists of 300,261 entries and 11 features, each contributing to the analysis.
### Features
The key features of the cleaned dataset are outlined below:
•	Airline: This feature stores the name of the airline company. It's a categorical feature with 6 different airlines represented.
•	Flight: This categorical feature contains the flight code information, unique to each plane.
•	Source City: This feature indicates the city from which the flight departs and includes 6 unique metro cities.
•	Departure Time: A derived categorical feature that groups departure times into 6 distinct time intervals.
•	Stops: A categorical feature representing the number of stops a flight makes between the source and destination cities, with 3 possible values.
•	Arrival Time: Similar to the departure time, this feature groups arrival times into 6 different time intervals.
•	Destination City: This feature represents the city where the flight lands and includes 6 unique metro cities.
•	Class: A categorical feature that indicates whether the ticket is for Business or Economy class.
•	Duration: A continuous feature showing the total travel time between cities, measured in hours.
•	Days Left: This feature is derived by subtracting the booking date from the travel date, indicating how many days are left until the flight.
•	Price: The target variable of our study, representing the cost of the flight ticket.

