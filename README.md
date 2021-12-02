# Placing WTWY Street Teams 
Project duration: September 13-24, 2021 

The goal of the project is to find locations of maximum passenger movement in the MTA subway system. WomenTechWomenYes would like to get emails of New York locals to invite attendees to their annual summer gala. They aim to deploy street teams at the MTA turnstiles to reach maximum participants supportive of "increasing participation of women in technology, and to build awareness and reach". They are interested in knowing the locations of the busiest turnstiles.

I conducted exploratory analysis of publicly available MTA turnstile data. Initial data cleaning is followed by data descriptives and visuals. I analyze the data from March through May of 2021 to suggest optimal turnstile locations for placing the street teams. Number of exiting passengers are counted as patrons exiting the subway are more likely to have time to respond compared to patrons entering to catch a train. We report findings for a typical weekday, and a Saturday. 

**Data Analysis**

The data source is the publicly available MTA turnstile data, which has records of entry and exits of passengers at all MTA turnstiles in four hourly bins for the last twenty years. Information on spatial distribution of the turnstiles, and covid and vaccination situation in New York is good supplementary data to add to this analysis.

The MTA turnstile data was cleaned, aggregated, and visualized to obtain the optimal placement for Wednesdays, as a typical weekday, and Saturdays, based on median values of exits. As the stations are large and often span many blocks, to specify locations of maximum throughput for street team placement we chose the turnstile as the spatial unit of analysis. 

**Data Issues**

Some of the turnstiles had reverse counters due to which later cumulative counts were smaller than earlier ones. Also, the counters were reset on occasions following which counts were smaller than those before. While regular four hourly audits took place, sometimes they were missed and replaced with a recover audit. All recover audit values were disposed for this analysis as they were found too large when compared to the regular audit values. Values obtained after correcting for the reverse and reset counters were compared against a max-counter. The value for this was set at 43200, corresponding to maximum possible passenger exit in a day assuming 2 seconds per person with no swiping at the exit gates.

**Tools**

 - SQLite & DB Browser as database for ingested data

 - SQLAlchemy for initial queries

 - Pandas for data cleaning and exploratory data analysis

 - Matplotlib for visualization
