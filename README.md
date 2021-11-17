# Placing WTWY Street Teams 

## Abstract 

The goal of the project is to find locations of maximum passenger movement in the MTA subway system. I conduct exploratory analysis of publicly available MTA turnstile data. Initial data cleaning is followed by data descriptives and visuals. I analyze the data from March through May of 2021 to suggest optimal turnstile locations for placing the street teams. Number of exiting passenger are counted instead of those entering the system, as patrons on their return trips are more likely to have time to respond. We report findings for a typical weekday, and a Saturday.

## Design 

The project is initiated by WomenTechWomenYes who would like to get emails for attendees to their annual summer gala. They aim to deploy street teams at the MTA turnstiles to reach maximum participants supportive of "increasing the participation of women in technology, and to build awareness and reach". They are interested in knowing the locations of the busiest turnstiles and those where the patrons are more likely to be locals and supportive of their cause.

## Data

The data source is the publicly available MTA turnstile data which has records of entry and exits of passengers at all MTA turnstiles in four hourly bins for the last twenty years. Information on spatial distribution of the turnstiles, and covid and vaccination situation in New York is a good supplement.

## Algorithms

A thorough exploratory data analysis of the MTA turnstile data was done, in which the data was cleaned, explored, aggregated, and visualized to obtain the optimal placement on Wednesdays, as a typical weekday, and Saturdays, based on median values of exits.

As the MTA stations are large and often span many blocks, the spatial unit of analysis was the turnstile. Some of the turnstiles had reverse counters due to which later cumulative counts were smaller than earlier ones. Also, the counters were reset on occasions, which led to the same issue. While regular four hourly audits took place, sometimes they were missed and replaced with a recover audit. All recover audit values were disposed for this analysis as they were found too large when compared to the regular audit values. Values obtained after correcting for the reverse and reset counters were compared against a max-counter. The value for this was set at 43200, representing maximum possible passenger exit in a day assuming 2 seconds per person with no swiping at the exit gates.

## Tools
 - SQLite & DB Browser as database for ingested data

 - SQLAlchemy for initial queries

 - Pandas for data cleaning and exploratory data analysis

 - Matplotlib for visualization
