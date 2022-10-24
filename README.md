# SparkFit Wellness Community Inc.

## Abstract	

SparkFit Inc. is looking to open a location for a certified StrongFirst training studio and wants to know what area of New York City they should consider based on high volume subway commuters and an area that is not in close proximity to another certified gym. The [MTA turnstile data](http://web.mta.info/developers/turnstile.html) was used to identify high volume traffic commuter locations and the [registry of certified StrongFirst gyms](https://www.strongfirst.com/gyms/) for nearby competitors. Results indicate that the top 10 busiest subway stations are in close proximity to one another and there are four gyms nearby. Given findings, there are areas within a close proximity to the high volume subway stations for SparkFit to consider.

To dig deeper into this project, please see the final jupyter notebooks and presentation slides within this repository.

### Design
This project aims to use the movement of subway flow traffic to guide SparkFit Inc. in choosing an optimal location to open up another StrongFirst certified personal training studio in New York. The location and proximity of other certified gyms is an additional factor to consider.

### Data
The primary data source is the MTA turnstile data. Data from May 2021-Apr 2022 was selected, which resulted in 40,049,393 rows of data across 11 features. The most recent data was selected because due to the pandemic, SparkFit Inc. wants to be sure they have the most current data to assess the movement of people in the city. Zip codes of the top ten busiest subway stations were downloaded via the Google Maps API. Zip codes of each of the gyms was acquired from the StrongFirst gym registry.

### Algorithms
**Data Cleaning:** The date variable was transformed into a datetime type. Duplicate rows of data were assessed and removed.

**Feature Engineering:** The calculation of the daily entries and exits for each subway station was computed. The sum of daily entries and exits was calculated for each station over the specified time period.

**Exploratory Data Analysis:** Based on the total traffic for each station over the year, the top ten most trafficked stations were plotted visually. These top ten stations were compared against the top ten stations from Feb 2022-Apr 2022 and the same rank order of stations were found. The total traffic on weekdays versus weekends was assessed and results indicate a steep decrease in traffic on Saturdays across the year. This same analysis was also grouped by station and revealed that the top ten busiest stations stayed the same across the days of the week, with a steep decrease in traffic on Saturdays. The average distance between each gym and the top ten stations was plotted and revealed that there are four gyms within a 50 mi radius. [Google Maps was used to provide a visual assessment of the subway stations in relation to the gyms](https://www.google.com/maps/d/edit?mid=1luz-YpjC_9yySAGswIVeOk3S2JnKtuE&usp=sharing).

Below is the average distance between gyms and top 10 busiest stations
![Screen Shot 2022-10-24 at 22 13 30](https://user-images.githubusercontent.com/80511410/197533899-c127e100-4859-4e71-bc88-2fa673002f97.png)

Below the stars designate the ideal locations for SparkFit to consider.
![Screen Shot 2022-10-24 at 22 14 04](https://user-images.githubusercontent.com/80511410/197534046-afa83722-e092-4e7f-a017-3f537ff5ec00.png)

### Tools
1) Numpy and Pandas for data cleaning, manipulation, and exploratory data analysis
2) Matplotlib and Seaborn for plotting
3) Google Maps for geographical visualizations
4) Google Maps API for zip code extraction of each subway station
5) SQLAlchemy for data import
6) [zip code distance calculator](https://www.freemaptools.com/distance-between-usa-zip-codes.htm) used between each station and gym

### Communication
I completed a 5-minute presentation of my findings; slides and visuals for this project are included in this repository.


