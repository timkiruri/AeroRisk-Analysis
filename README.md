# Aircraft Risk Analysis: Understanding the Risks of an Aircraft Operation Enterprise 
![Aircraft Bottom Image](images/aircraft_bottom_in_air.jpg)
## Project Overview
This project looks at the National Transport and Safety Board's civil aviation accident data from 1962 to 2023 and selected in the United States.

The goal of this analysis is to determine the **safest aircraft** for MyCo to invest in.

## Busines Understanding
MyCo is expanding in order to diversify its business protfolio. MyCo is interested in the aviation industry and in specific the purchasing and operation of airplanes for commercial and private enterprises. 

MyCo has very little understanding about the potential risks of aircrafts and as such an analysis with the aim of determining the aircraft with the lowest risk will be comissioned. The resulting aircraft will be used to start this new business endeavour.

International data was dropped from the analysis for a number of reasons:

1. Compared to the United States data, international accident data had a small sample size i.e. United States (91%) and Others (9%).
2. To ensure consistency in reporting standards as it was noted that international data used differing reporting formats.

## Key Business Question & Stakeholders
The **primary stakeholder** of this analysis and presentation is the Head of the Aviation Division at MyCo. 

With him being the primary stakeholder, a balance of a technical as well as a business approach is appropriate. As such, this analysis will focus on the following business question:

> What is the aircraft with the lowest risk and as such suitable to start the new business endeavour?

We will answer the primary question by answering the following questions:

### Technical Questions
1. Which aircraft models have the lowest accident rates and the fewest fatal injuries? 
2. How does the number of engines correlate with accident severity?
3. How do accident rates vary by aircraft category across different weather conditions?
4. What are the most common causes of accidents based on the broad phase of the flight? 
    
### Business Questions
1. Which aircraft manufacturers have the best safety records based on accident severity and total injuries?
2. How do scheduled vs. non-scheduled flights compare in terms of frequency and severity of accidents?
3. What is the trend of aircraft accidents over time and what does this indicate for future investments?
4. Are amateur-built aircrafts significantly riskier compared to professionally built aircrafts.

## Data Understanding and Analysis
### Data Source
The data in this analysis has been sourced from [NTSB's Aviation Accidents from 1962 to 2023]('https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses/data?select=USState_Codes.csv') which is obtained from Kaggle.

The data contains details on details on aircraft type, weather conditions, accident severity, flight purpose and location.

### Key Features
| Column Name              | Description |
|--------------------------|------------|
| Event.Date            | Date of accident |
| Location            | City or region where the accident occurred |
| Country               | Country of the accident |
| Aircraft.Category     | Type of aircraft (e.g., commercial, private, etc.) |
| Make                  | Aircraft manufacturer (e.g., Boeing, Cessna, Airbus) |
| Model                 | Specific model of the aircraft |
| Number.of.Engines     | Number of engines on the aircraft |
| Engine.Type           | Type of engine (jet, piston, etc.) |
| Injury.Severity       | Severity of injuries (fatal, serious, minor, none) |
| Total.Fatal.Injuries  | Number of fatalities |
| Total.Serious.Injuries| Number of serious injuries |
| Weather.Condition     | Weather at the time of accident (VMC - Visual, IMC - Instrument) |
| Broad.phase.of.flight | Phase of flight when accident occurred (takeoff, cruise, landing, etc.) |
| Air.carrier           | Airline/operator of the aircraft |
| Schedule              | Whether the flight was scheduled or non-scheduled |

### Data Cleaning & Preprocessing
#### Data Preparation
Latitude and Longitude data was removed from the [subset]('notebooks/01_data_exploration.ipynb) as they were deemed not necessary in the analysis. It was perceived that these contained the latitude and longitude of the accident which would bear limited insights in answering the focus questions.
Aircraft carrier data was dropped in the [subsetting section]('notebooks/01_data_exploration.ipynb) since airlines often own and operate airplanes based on similar manufacturers which would make it a redundant column to have in the data frame.

#### Data Cleaning
To ensure data integrity and relevance, the dataset underwent the following preprocessing steps:

1. Column Name Standardization: 
    
    - I renamed all the column names by replacing all the "." that were used as separators to underscores. This was to maintain consistency in formating standards.

2. Duplicate Removal: 

    - I went through the data looking for duplicates that were in the data. It was great to note that there were no duplicates in the data.

3. Timeframe Adjustment: 
    - I changed the 'Event_Date' series to datetime and with this created a new series that hosted the 'Year' of the accidents.
    - When looking at accident distribution by year, I noted that there were very few accidents pre-1982 and as such I decided to drop all rows that were pre-1982.

4. Accident Severity Metric: 
    - I added a new column that would be used to assess accident severity. This column was formed by summing 'Total_Fatal_Injuries', 'Total_Serious_Injuries', 'Total_Minor_Injuries', 'Total_Uninjured' to find the 'People_Onboard'.

#### Handling Missing Values
In this section I took the following steps to ensure that I have all the data I need:

1. Removed records where 'Make' and 'Model' fields were missing to maintain aircraft classification accuracy.

2. Dropped entries with unknown or missing weather conditions, as weather is a critical factor in accident analysis.

#### Feature Engineering
1. Location refining:

    - I extracted state abbreviations from the 'Location' series with the aim of merging these with an external dataset containing all the US States and their abbreviations. This would help enhance location-based insights

### Exploratory Data Analysis & Visualisations

## Key Findings

## Business Recommendations