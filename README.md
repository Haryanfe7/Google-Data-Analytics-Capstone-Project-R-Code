# Google-Data-Analytics-Capstone-Project-R-Code

## Statement of Problem
The case study is for Cyclistic, a bike-sharing company in Chicago. Cyclistic runs a bike-share program that features about 5828 bicycles and 692 docking stations. The company stand-out among its peers by availing hand tricycles, cargo bikes, and reclining bikes, ensuring the bike-share program is more inclusive to disabled people and users who can’t ride a standard two-wheeled motorcycle. Riders that buy that annual subscription are called Members, while those who use single-ride or full-day passes are known as casual riders. Most riders choose traditional bikes, and around 8% use the assistive options. While most users tend to ride for leisure, about 30% use bikes for transport to work every day.

## Key Stakeholders & Perspectives
The marketing director
The Executive team
The marketing director believes the company’s future success relies heavily on increasing the number of annual memberships. With a good marketing campaign, the company can convert casual riders to annual members.

## Scenario
I’m working as a junior data analyst in the marketing analyst team at Cyclistic, and my team is responsible for overseeing the aim of the study (see below)

## Aim of the Research
The brand financial analyst team has proven that annual members provide more profit than casual riders. The study aims to understand how annual members and casual riders use Cyclistic bikes differently. The marketing team will use the insights from the survey to design a new marketing approach to convert casual riders to annual members.

For this project, I’ll follow the data analysis process: Ask, Prepare, Process, Analyze, Share, and Act.

### Ask
We are identifying business tasks and problems to solve. What’s the business problem?

The project aims to understand how casual and annual riders use bikes so the marketing team can develop the best marketing scheme to convert casual riders to annual members. The goal is to answer these three questions:

--How do casual riders and annual members use Cyclistic bikes differently?
--Why would casual members opt for the annual memberships?
--How can the brand use digital media to encourage casual riders to buy annual memberships?
--The marketing director assigned the first question to be treated in this project.

As such, I divided the aim into the following objectives:

--Total number of riders between members and casual
--Average ride length between members and casual
--Total ride numbers and average ride length per daytime, day, and month for each category of users and bike types
### Prepare
The preparation stage features collecting and storing data. The data for the project is available here. It’s a public dataset with Cyclistic historical trip data to explore, analyze, and identify trends.

#### Data Integrity
The data is made available by Motivate International Inc under this license.

#### Data Organization
I extracted the previous 12 months of the historical trip data (January-December 2022). The information regarding the data organization is as follows:

File type — .csv
File naming convention — YYYY-MM-divvy-tripdata
Each file data contains 13 columns.
Column names are similar across all file data, but the number of rows varies.
#### Data Privacy and Security
The riders’ unique identifiable information is unavailable and hidden via tokenization. To ensure adequate data security, I ensure the original files are backed up in a separate folder.

#### Data Limitation
Since riders’ personally identifiable information isn’t available, connecting their pass purchases to credit card numbers is impossible, making it challenging to determine whether causal riders are within the Cyclistic service area or have bought numerous single passes.

### Process
The process stage involves the step taken to ensure data is cleaned and prepared for analysis. I wanted to use SQL for the data cleaning as it’s the most comfortable tool for me. However, the data files were too large, and merging them took almost forever. Also, Microsoft Excel cannot hold such an amount of data (5 mil rows). Hence, I had to use R programming language to clean the data. Below are the steps taken in R language for data cleaning:

· Install necessary packages and libraries.

Loaded all the CSV files separately and merged them using rbind
Ensured all columns had the correct data type format
Removed duplicate rows and null/blank values
Filtered out data where the ride_id is not 16.
Created new columns for ride length (time ended — time started)
Removed columns where the ride length is zero or negative
Formatted the date column to extract the year, month, day of the week, and time columns
Created new columns for the day of the week, month, day, and year.
Removed other unused or unwanted columns (start station_id, end station_id, start_lat, start_long, end_lat, end_lng).
Extracted the cleaned data as a CSV file.
You can find the full R programming code here.

### Analysis and Visualization
After cleaning the data in R, I sent the CSV file to Power Bi for analysis and visualization.

POWER BI

Below are the analysis and visualization I did on Power BI:

Total rides and average rides lengths for:

Member types- Annual Members vs. Casual riders
Bike type — Classic vs. Electric vs. Docked
Each month
Each day of the week
I also separated each category by member type and ride type. You can find the dashboard for the visualization here.

### SHARE
The session involves sharing the key findings obtained from the visualizations. Below are the insights I derived from the visualizations:

#### Figure 1

Figure 1: Visualizations for Total Rides and Average Ride Lengths for each Member Type
The visualization above shows each member type total rides and average ride lengths. From the diagram, we can deduce that most riders are member riders. However, while member riders have a higher number of rides, the average ride time of casual riders is significantly higher than annual member riders.

#### Figure 2:

Figure 2: Visualizations for Total Rides and Average Ride Lengths for each Member and Bike Type
Key findings from figure 2
Classic Bikes were the most used bike types (about 60% of customers use them), while docked bikes were used the least.
Users spent more time riding Docked Bikes than any other bikes.
Member Riders didn’t use Docked Bikes at all.
Member riders used classic bikes almost twice as much as casual riders, but casual riders have longer ride lengths.
More member riders use electric bikes than casual riders, but casual riders take longer trips on average.
#### Figure 3

Figure 3: Visualization for Total Rides and Average Ride Lengths For Each Member Type Per Weekday
Key Findings from Figure 3
Most users spent more time riding bikes on weekends than on weekdays.
Ridership often peaked on Saturdays.
The ride lengths for member riders were shorter than for casual riders on weekdays.
Member riders had the highest total rides every day except weekends, where casual riders peaked.
#### Figure 4

Figure 4: Visualization for Total Rides and Average Ride Lengths for each Member Type across the Year
Key Findings
Ridership started to pick up in January and peaked in July before massively declining till December for both rider categories.
May has the longest ride time across the year.
There were more Member riders than casual riders all through every month of the year.
Casual riders take longer trips than Member riders all year round.
#### Figure 5

Figure 5: Visualizations for Total Rides and Average Ride Lengths for each Member Type per daytime
Key Findings From Figure 5
The afternoon is the busiest ride time, and the night is the least active.
Riders ride longer in the afternoons compared to other ride days, with the least time in the morning.
While member riders have higher ride amounts than casual riders at every time of the day, casual riders have longer ride times.
### Act
In this final step, I provided recommendations to the marketing director on maximizing profits and converting casual riders to members based on the key findings.

#### Recommendations
1. Because casual riders took longer trips or rides than annual Members on average, it is possible that casual riders used Cyclistic bikes for recreational activities such as sightseeing on the weekends. Cyclistic bike-share should provide discounts to casual users to gain their loyalty. Membership subscription improvements, such as ride length-based tariffs that charge less as ride length grows, can benefit since it gives greater incentive for members to ride larger distances. With such a change, it may also entice casual riders to upgrade their memberships to benefit from ride time discounts.

2. Casual riders often ride on weekends, while annual members use the service more during the weekdays. This might imply that annual Members use the bikes to travel to work, whereas casual users are tourists or groups visiting the seaside for fun. A weekend-only membership that charges less than the present 7-day membership might be introduced as part of a Cyclistic bike-share promotional campaign to entice casual riders to join.

3. Ridership begins to increase in February and declines in August. That might be related to seasonal variations. When the weather starts to warm in February, more riders begin to cycle, and vice versa when the weather starts to cool in August. The marketing campaign should start between February and August when the number of trips cyclists take begins to increase.

4. Casual riders favored classic motorcycles over alternative ride types such as electric and docked bikes. Annual members preferred classic motorcycles over other varieties. A rebate program in the form of reimbursements to annual Members who utilize a specific ride type more than others should be implemented. That might be a minor portion of the total cost.

Many riders are members, demonstrating that the firm has already established a degree of fidelity among its bike users. As a result, the firm has a better chance of converting more casual riders into subscribers. Following the suggestions above will help casual riders upgrade to a yearly membership, increasing revenue and profitability at Cyclistic bike-share.

Thanks for reading…
