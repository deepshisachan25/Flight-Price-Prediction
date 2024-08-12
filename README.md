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
This dataset was originally gathered from "Ease My Trip" website. The data was collected in two batches: one for Economy class tickets and another for Business class tickets. In total, we extracted 300,261 unique flight booking options over a period of 50 days, from February 11th to March 31st, 2022. 

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

## Exploratory Data Analysis
Exploratory data analysis is the process of exploration of data using tools like visualization and statistics to understand your data better, test statistical hypothesis, identify patterns, look for outliers and find opportunities for feature engineering. These findings can then be further used for explanatory analysis where the data is presented to the concerned audience to showcase our findings
Findings from Data Exploration:
There are total 3,00,153 records and 12 columns.
There are no duplicates and null values present in the given dataset. Each record is an unique flight plan of its own without the key as well, maybe flight codes are making them unqiue. 
Statistical summary was recorded for each numerical variables:
![image](https://github.com/user-attachments/assets/dd854fab-1be8-40b5-9bcc-ea430800ff76)

Below plot shows there are more records of Vistara airline flight.
![image](https://github.com/user-attachments/assets/610457f0-9b20-4958-9e86-4b05336e9122)
![image](https://github.com/user-attachments/assets/51b1c5d0-9456-4c06-952b-15d63a6cf8ef)
Most of the flight in this dataset takes 1 stop to reach their destination.
Distribution of Destination cities are shown below:
![image](https://github.com/user-attachments/assets/69fd61c5-d668-4aa4-a95f-6a29a53214ea)

![image](https://github.com/user-attachments/assets/44e40e02-8649-406c-ad81-9853b6f98918)
This plot shows that most of the flight starts from Delhi and Mumbai.

Price of each airline by class of the flight is shown:
![image](https://github.com/user-attachments/assets/f01abb35-0bac-4247-be66-8ef8868d854e)

![image](https://github.com/user-attachments/assets/9699b36d-c937-44f7-8aa6-295e10e80748)
Price of the flight with respect to days left in booking the flight shows that earlier the flight is booked from start date prices are cheaper.

## Data Preparation
Data was prepared before building linear regression model to predict the price of the flight. Categorical variables were changed into numerical using dummies and converting into 0, 1.
Input variables (Independent variable) are: days_left, class, stops, duration, Airlines. Airlines were converted into binary dummy variables: AirAsia, Air_India, GO_FIRST, Indigo, SpiceJet, Vistara.
Target Variable (Dependent variable) is Price.
The data is splitted into Training and Test dataset. Linear regression model was fitted on training dataset and performance of model was tested on Test dataset.
![image](https://github.com/user-attachments/assets/6db0e1ff-6c55-4677-92b9-670491921850)

![image](https://github.com/user-attachments/assets/1e28065f-2a6c-47ef-af09-647de3d967c8)
Model gave an accuracy of 90.64% in predicting the price of flight.

Then prediction was done on new data:
![image](https://github.com/user-attachments/assets/1e418e00-4f6f-4d0c-ba1a-88f6aea24b9a)



