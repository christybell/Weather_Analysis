# World Weather Analysis: Using APIs to Visualize Weather Data

## Project Overview
PlanMyTrip is a top travel technology company specializing in internet-related services in the hotel and lodging industry. My supervisor, Jack, is the head of the User Interface Team, and so he has tasked me with helping to collect and present data for customers via the search page, which they will then filter on their preferred criteria in order to find their ideal hotel anywhere in the world. To perform this task, I've used a Jupyter Notebook in the citypy module to get the cities for more than 500 random latitudes and longitudes. Then, I performed requests on the OpenWeatherMap API and retrieved the JSON data from these cities. This weather data was added to a Pandas DataFrame where I used Matplotlib to create a series of scatter plots to show the relationship between latitude and a variety of weather parameters for over 500 cities around the world. As part of my analysis, I've performed statistical calculations on the data using linear regression on the weather parameters in the northern and southern hemispheres. This data will help my team predict the best time of year for people to plan their vacation. Finally, I have exported the data, cleaned it, and used the weather data to choose the best cities for a vacation based on certain weather criteria and then mapped these cities using Jupyter Gmaps and Google Places API. I am ready to help travelers find their ideal vacation spot!

Here is the basic outline for the project:

- **Task**: Collect and analyze weather data across cities worldwide.
- **Purpose**: PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
- **Method**: Create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data.
	
## Resources
- **Data Sources**: 
- **Software**: Python 3.7.6, Anaconda 4.9.2, Git Bash 2.29.2
- **Tools**: Jupyter Notebook, Pandas, Matplotlib 3.3.2 

## Challenge Overview
In my next assignment, I was tasked to use my Python skills and knowledge of Pandas to create a summary DataFrame of the ride-sharing data by city type. Then, using Pandas and Matplotlib, I created a multiple-line graph that shows the total weekly fares for each city type. Lastly, I summarized how the data differs by city type and how those differences can be used by decision-makers at PyBer.

## Challenge Deliverables

### Deliverable 1: A ride-sharing summary DataFrame by city type
- First, I retrieved the total number of rides for each city type:

	<img src="analysis/Delv 1_step 1_rides by type.PNG">

- Then I retrieved the total number of drivers for each city type:

	<img src="analysis/Delv 1_step 2_drivers by type.PNG">

- Next, I retrieved the sum of the fares for each city type:

	<img src="analysis/Delv 1_step 3_fares by type.PNG">

- Then I calculated the average fare per ride for each city type:

	<img src="analysis/Delv 1_step 4_avg fare per ride.PNG">

- Next, I calculated the average fare per driver for each city type:

	<img src="analysis/Delv 1_step 5_avg fare per driver.PNG">

- Then I created a PyBer summary DataFrame:

	<img src="analysis/Delv 1_step 6_pyber summary.PNG">

- Finally, I formatted the PyBer summary DataFrame as shown in the example:

	<img src="analysis/Delv 1_step 8_pyber format.PNG">

### Deliverable 2: A multiple-line chart of total fares for each city type
- First, I created a DataFrame using the `groupby()` function on the "type" and "date" columns, and applied the `sum()` method on the "fare" column to show the total fare amount for each date and time:

	<img src="analysis/Delv 2_step 1_fares groupby.PNG">

- Then I created a DataFrame using the `pivot()` function where the index is the "date," the columns are the city "type," and the values are the "fare":

	<img src="analysis/Delv 2_step 3_fares pivot.PNG">
	
- Next, I created a DataFrame using the `loc` method on the date range: 2019-01-01 through 2019-04-29:

	<img src="analysis/Delv 2_step 4_new fares data.PNG">
	
- Then I created a DataFrame using the `resample()` function in weekly bins that shows the sum of the fares for each week:

	<img src="analysis/Delv 2_step 7_Fares by week.PNG">
	
- Finally, I created an annotated chart showing the total fares by city type and saved it to the "analysis" folder:
	
	<img src="analysis/PyBer_fare_summary.png">
	
## Challenge Results
My analysis revealed several differences in ride-sharing data among the different city types, as noted below: 
- **total rides** - The urban city type accounted for the largest amount of total rides by far, totaling 1,625, while suburban totaled 625 and rural totaled 125 rides.
- **total drivers** - The urban city type had the highest number of total drivers at 2,405, while the suburban type had 490 and rural had 78.
- **average fare per ride** - The average fare per ride was lowest for urban cities at $24.53, the suburban average was $30.97, and the rural average was highest at $34.62.
- **average fare per driver** - The average fare per driver was lowest for urban cities at $16.57, the suburban average was $39.50, and the rural average was highest at $55.49.
- **total fare by city type** - The urban city type had the largest sum of total fares, coming in at almost $40,000. The suburban total was close to $20,000 and the rural total was just over $4,000.

## Challenge Summary
In summary, based on these results, I would make three recommendations to the CEO for addressing the disparities among the city types and improve the overall business economics:

1. To encourage and attract a broader population to use ridesharing, I'd recommend the company offer special promotions and discounts for rural and suburban rides for a limited time. 

2. I'd suggest the company recruit more rural drivers to increase convenience for riders in those city types. If the company hasn't already, I'd also propose it consider adopting policies to retain its current pool of drivers so as not to put strains on margins for driver quality and customer loyalty.

3. For continued growth, I'd suggest the company consider offering a loyalty program to encourage its existing population to use ridesharing in a wider range of circumstances.

