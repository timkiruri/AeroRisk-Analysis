# Aircraft Risk Analysis: Understanding the Risks of an Aircraft Operation Enterprise 
![Aircraft Bottom Image](images/aircraft_bottom_in_air.jpg)
## Project Overview
This project looks at the National Transport and Safety Board's civil aviation accident data from 1962 to 2023 and selected in the United States and international waters.

## Busines Understanding
MyCo is expanding in order to diversifu its business protfolio. MyCo is interested in the aviation industry and in specific the purchasing and operation of airplanes for commercial and private enterprises. 

MyCo has very little understanding about the potential risks of aircrafts and as such an analysis with the aim of determining the aircraft with the lowest risk has been comissioned. The resulting aircraft will be used to start this new business endeavour.

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
#### Handling Missing Values

#### Feature Engineering

### Exploratory Data Analysis & Visualisations

## Key Findings

## Business Recommendations