## [Reaching the most patrons supportive of their cause: Analyzing MTA turnstile data to suggest optimal placement for WTWY street teams]

### [A Proposal]
#### September 8, 2021

Technology has hitherto been the stronghold of men. Men have, and continue to dominate in fields relating to science, technology, and engineering. Studies prove social conditioning and lack of opportunities are the reasons due to which women feel inadequate in those areas. 

WomenTechWomenYes is a non-profit that addresses this gap by building awareness and creating resources that empower women to join and succeed in technical fields. To advertise and raise funds to this end, they work with their street teams to obtain signatures from supporters and potential contributors to their cause. 

The following proposal outlines how Metis Data Scientists could leverage the publicly available MTA turnstile data to predict the most optimal placement of the WomenTechWomenYes street team to reach the maximum number of supporters and potential contributors to their effort. 

#### Question/need:
The framing question is: How could WomenTechWomenYes (WTWY) place their street teams at entrances to New York subway stations, so they could collect email addresses and signatures of most patrons for sending tickets to their gala? In order to answer that, we will look at **hourly locations of highest passenger activity**. It would be ideal to reach patrons who are likely to be supportive of WTWY's cause and be able to contribute to it. We will hypothesize that office commuters, especially **those who are in tech jobs, and those in higher education**, are likely to be supporters who will contribute to the cause and validate this with some literature search. We will then isolate this demographic among all patrons of the subway system. 
WTWY will benefit from exploring this question as they will be able to then place their street teams, most optimally to reach the most people who are likely to support their cause. 

#### Data/Description:
We will use the publicly available MTA turnstile data that provides daily information of all entries and exits at turnstiles by location, date, and time. As a pilot, we will provide the ideal street-team placement locations by time for **a typical weekday and a typical Saturday in mid-September to mid-October timeframe** for immediate use, and provide suggestions for **days that would be outliers**, like a game day. Based on the success of that effort, we will continue to provide weekly or monthly plans for street team placements. 
Since data for last year was skewed due to covid, and that for this year is still in a comeback mode, we will look at data for the following durations:
* mid-August to mid-October (2019) for pre-covid data for the target period and one month prior
* mid-August to mid-October (2020) for during covid data for the target period and one month prior
* mid-August to mid-September (2021) for comeback mode data for the month prior

An individual sample/unit of analysis would be **one turnstile by station**. A more aggregate unit would be a station or a group of stations along a line, however, knowing specific turnstiles to position street teams at, at a station, will help estimate the number of personnel to be deployed at different station. We will work with the number of entries and exits at each station by date and time of day. 
We will study extent of station activity before covid (daily fluctuations such as peak/off-peak, and weekly fluctuations such as weekday and weekend activity), so it is possible to predict accurately for each hour during each day. Our model could be trained on the mid-August to mid-October of 2019 and 2020, to predict for mid-August to mid-October 2021. We could validate our prediction for mid-August to mid-September with the actual data for that period and accordingly fine-tune our model for predicting for October. 

#### Tools
SQL will be used for aggregating and extracting the relevant periods of data into Python via SQLAlchemy. Pandas will be used to clean the data and matplotlib to visualize the data. Visualization would be a geographical heat map for a typical weekday and a typical Saturday by hours of day. 

#### MVP Goal
The MVP goal would be a plot of passenger movement at a station over the study duration (mid-September to mid-October), and two other plots of the same station showing hourly variations over a weekday and a Saturday. A third plot would show passenger variations across all of the stations for the evening peak, assuming office commuters returning home from work would be supporters of this cause and would have the ability to contribute. Additionally, they would not be in a rush to catch the train in the evening, and would have more time to respond. 



