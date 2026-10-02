Research Topic: Areas of Interest and Data Exploration:
	The Chicago Transit Authority is the leading agency for public transportation in the Chicago metropolitan region. The agency, which is comprised of an elevated train system, known as the CTA ‘L’, and bus system serves over 1,000,000 riders per weekday, with the bus alone accounting for approximately 620,000 of those clients.[^1]  Given the importance public transit plays in the City of Chicago, reliable services, especially bus service, which accounts for two thirds of all riders, is essential. However, in the past few years, bus arrivals have become erratic. Buses frequently arrive late, arrive one after another in a bunched-up manner—thereby resulting in long wait times—, or at times don’t arrive at all. Many times, passenger have come to look at the Ventra app, the official app of CTA, Pace, and Metra, for arrival times and have found the “next bus arriving” information displayed on the app to be incorrect. This condition is known as ghost buses, and is something that has vexed riders, CTA officials, business leaders, and other government officials. As such, the visualization proposed in this research will help Chicagoans better understand bus reliability throughout the city. At this preliminary stage, it is anticipated that the visualization will show average arrival times, wait times, ghost buses, and more. 

Observation and Data Collection Plan:
	To create a visualization necessary to convey bus reliability, data was collected in the field. First, the team met to discuss the general framework they thought would be best for obtaining the data needed to create the visualization. The three team members decided that the best way to collect data would employ direct in the field collection. The rough idea the group had would be for each member to stand in front of a bus stop and observe how long it took for the next bus to arrive, while also recording “the next bus information” displayed on the official Ventra app. This process would then be repeated over and over again. 
	However, before data could be collected, the group had to decide what variables, features and measures needed in order to capture bus frequencies and reliability. These attributes would be decided in a two step process: first decide in general what features the group thinks could be important and necessary to collect, and second to conduct a pilot data collection and then based on the experience, refine the features and data types necessary, as well as methods for collecting data.
	
	Pre-Pilot Features:
	Before codifying the specific variables needed, the group began by creating thinking through what features would be necessary for this type of visualization. Certain variables were obvious: bus arrival times, ventra times, route and stop numbers were the first to come to mind. Next, the group decided that capturing the time when the previous bus arrived (excluding buses that arrived before observations began) would also be important.

	At this point, an initial data dictionary was created (in subsequent sections of this report, a refined data dictionary is presented).

	Attribute                  Type                 Description
	Observation Number         Numeric              Keeps track of observations
	Stop Location              Text                 Helps define location of stop
	Stop ID                    Numeric              Helps define location of stop using CTA numeric system
	

	Pre-Pilot Data Collection:
	With this rough idea of what features would be necessary for this visualization, the data collection process was then discussed. In particular, the group posed these questions first, and then sought to answer them:
	1. If we want to better understand bus arrivals, what routes and areas of the city should we observe?
	2. How should we observe buses, should we stand in front of bus stops during rush hour, the average middle of a workday, evening, night, etc.?
	3. Is this process workable? Knowing that every stop and every route cannot be observed during the semester by a small group of students, what can be accomplished, and will this be enough to carry out a visualization? How long will it take to get just a few observations?

	Final Pre-Pilot Steps:
	With these questions in mind, the group was almost ready to conduct a small pilot data collection.	However, before collecting data, census data was quickly reviewed. Even in the pilot collection, the group wanted to try and cover different demographic regions. These regions needed to be different not just in terms of income and household wealth, but also in terms of lifestyle--vibrant downtown, walkable residential, suburban/bunglow belt, etc. neighborhoods--to ensure that the visualization captures CTA reliability as felt by all Chicago residents. For this part of the research, the group turned to the American Community Survey to look at demographic and lifestyle data to help determine the different socio-economic neighborhoods in the city, allowing the group to select neighborhoods, that even in the pilot, represent the city's population as a whole [^3].

	Pilot Data Collection, Locations, and Brief Description:
	With this in mind, the following data collection was conducted for the pilot study:
	1. Matt covered both the Fulton Market and River North submarkets, representing the downtown region, whose population consists of workers in offices, downtown vistors, downtown residents, and tourists. In this part of the process, Matt observed buses arriving on September 21 at around 9:45 AM in Fulton Market (Halsted and Fulton Market) in the West Loop during morning rush, and again on September 26 at around 5:20 PM in River North (Kingsbury and Grand) in River North, observing weekend traffic into the entertainment and shopping district.
	2. Kaya (Shambhawi) covered Edgewater and Rogers Park residential districts, whose population consists of families and students from the nearby Loyola University (Lakeshore Campus). In this part of the process, Kaya observed buses arriving on September 23 at around 5:45 PM in Rogers Park (Clark and Devon) during evening rush hours (residents returning from work in downtown and work districts), and again on September 28 at around 8:45 AM in Edgewater (Sheridan and Granville) during morning rush hours (residents traveling to work in downtown and work districts).



Data description, discussion of preliminary data dictionary, and Domain Questions:
	Our pilot and initial data collection resulted in a small observational dataset consisting of 10 bus-arrival observations across at least three CTA routes and three geographically/demographically distinct areas per group member. The observations currently cover Route 147 at Sheridan and Granville in Edgewater, Route 22 at Clark and Devon in Rogers Park, Route 8 at Halsted and Fulton in Fulton Market and Route 66 at Grand and Kingsbury in River North. Each observation records the date, day of the week, route, stop, stop id, direction of travel, the arrival time predicted by the Ventra application, the actual bus arrival time, the time elapsed since the previous observed bus, the next-arrival time predicted by Ventra, and the actual time until the next bus when it could be observed. We also recorded qualitative comments describing events such as buses arriving early or late, buses appearing to bunch together, and buses being added to the Ventra application after the previous bus had already arrived. The observations therefore contain variation across route, geographic location, date, time of day, direction, predicted arrival, and actual arrival behavior. The pilot dataset provides observations from downtown and near-downtown areas as well as residential areas and college neighborhoods, allowing us to begin thinking about the differences each of the environments. However, the current dataset is still limited in both size and geographic and temporal coverage. The observations were collected during relatively short observation periods and primarily during morning or evening commuting periods, so they do not represent all times of day or all days of the week. The selected locations were also chosen deliberately to represent different types of neighborhoods rather than through a random sample of all CTA stops. Consequently, our observations cannot be used to claim that a particular route or neighborhood is generally more or less reliable across the entire CTA system. There may also be observer-related differences in recording times, particularly when buses arrive very close together or when the Ventra application updates while an observation is taking place.
	The process of turning bus service into structured data required us to make several decisions about what constitutes an observation. We defined an observation around the arrival of a bus at a particular stop, while also recording information about the previous and subsequent buses when possible. This allowed us to represent the phenomenon not simply as whether a bus was "on time," but as a sequence of bus arrivals and intervals between them. The "Ventra Time" and "Real Time" attributes capture the difference between what the passenger-facing application predicts and what actually occurs, while "Observation Previous" and "Actual Next" allow us to study the spacing between buses. The qualitative "Comments" field was retained because some events could not be adequately represented using numerical values alone. For example, a sequence of buses arriving close together may indicate bunching, while a bus appearing in the Ventra application only after a previous bus has arrived may suggest an update or prediction problem.
	At the same time, converting the observations into rows necessarily removed information from the original phenomenon. We did not record the exact location of every bus along its route before arrival, the number of passengers waiting, the number of passengers boarding, traffic conditions, the bus's position before it reached the stop, or the reasons for a delay. We also did not initially record every bus that was expected but failed to arrive, which makes it difficult to distinguish a true "ghost bus" from a prediction that was simply updated or removed by the application. The decision to use the bus arrival as the unit of observation also means that our dataset emphasizes individual arrival events rather than the experience of a passenger waiting continuously at a stop. These limitations became important as we began thinking about the questions our data could actually support.

	After conducting the pilot, the group refined the data dictionary to the following:

	

	

	Attribute	 Type	        Description	                                Example
	ID	         Categorical	Keep Track of Records, Unique 
                            identifier	                                    1, 2, 3
	Date	     Temporal	    Date of Observation	                        9/21/26
	Day of Week	 Temporal	    Day of the Week	                            M, T, W, R, F, S, Su
	Route	     Categorical	CTA Route Number	                        8
	Stop—Street	 Categorical	CTA Bus Stop	                            Fulton Market & Halsted
	Stop—CTA ID	 Categorical	CTA Bus Stop—CTA unique ID Code	            878
	Direction	 Categorical	Direction of Bus	                        N, S, E, W
	Obs Previous Quantitative	Number of minutes between 
                                current bus arrival and previous 
							    bus arrival	                                12
	Obs Next	 Quantitative	Number of minutes until next 
                                bus is expected, when current bus 
							    is leaving.
							    Taken from Ventra app	                    15
	Actual Next	 Quantitative	Number of elapsed minutes between buses	    2
	Comments	 Descriptive	Any additional information, Textual.        Buses bunched. 
                                                                            Bus arrived far later than expected.


The above data dictionary captures all of the item data type and attributes needed to visualize bus arrival times, and the nature of schedule dependability. In addition, the data encapsulated in the above data dictionary accomplishes some of the most imporant aspects of visual analytic system: answering domain questions through data questions, and allowing futher exploration.





Revised Domain Questions:
	Question 1 -- How accurately does Ventra predict the arrival of the next CTA bus?
	One question that emerged directly from our observations is whether the arrival information presented to passengers corresponds closely to what actually happens. This can be investigated by comparing "Observation Next", which represents the predicted time until the next bus, with "Actual Next", which represents the observed time until the next bus. The difference between these two values provides a measure of prediction error. For example, an observation where Ventra predicts 12 minutes but the bus arrives 8 minutes later represents a substantially different passenger experience from one where Ventra predicts 12 minutes and the bus arrives after 11 minutes. We are particularly interested in whether prediction errors are isolated events or whether they appear repeatedly at particular routes, stops, or times.

	Question 2 -- Where and when do buses appear to bunch together?
	Our pilot observations also revealed that bus spacing may be as important as individual arrival punctuality. At some observations, buses arrived only a few minutes after a previous bus even though Ventra had predicted a substantially longer interval. The "Observation Previous" and "Actual Next" attributes allow us to investigate these patterns. We want to determine whether closely spaced arrivals occur at particular locations, routes, or times of day. This question is useful because a route may appear to have adequate service when measured simply by the number of buses operating, while passengers may nevertheless experience long waits followed by multiple buses arriving together.

	Question 3 -- Which locations and routes show larger differences between expected and observed service?
	Our initial collection was deliberately distributed across different neighborhood contexts, including downtown/commercial areas and residential areas. We therefore want to investigate whether the relationship between expected and observed bus arrivals varies across the locations we sampled. This question can use "Route", "Stop", "Direction", "Ventra Time", "Real Time", and the predicted and actual next-arrival intervals. Rather than interpreting a particular neighborhood as inherently having better or worse transit service based on a small sample, the visualization would help us identify locations where our observations show larger or more frequent discrepancies. If we expand the dataset, these observations could subsequently be compared with neighborhood-level demographic or geographic information.

	Question 4 -- How does bus reliability vary across different times of day and days?
	The observations were collected at different times, including morning and evening periods, and across different dates and days of the week. This allows us to investigate whether the relationship between predicted and actual arrivals changes depending on when observations are made. We are particularly interested in whether rush-hour observations show more bunching, larger prediction errors, or longer gaps between buses. This question connects the "Date", "Day of Week", and arrival-time attributes to the service-reliability measures in the dataset. It also helps us determine whether our initial emphasis on rush-hour observations was appropriate or whether we need to collect additional observations during midday, late evening, or weekends.

	Question 5 -- Which routes or locations have the greatest observed variation in bus spacing?
	A fifth question emerged from thinking about the difference between average service and consistent service. Two routes could have similar average arrival intervals while producing very different passenger experiences if one route has relatively regular intervals and the other alternates between very long gaps and very short intervals. Using "Observation Previous", "Actual Next", and the predicted intervals, we can investigate the variability of bus spacing rather than only its average. This question may ultimately be more informative for our visualization than simply counting "ghost buses," because it captures both long waits and subsequent bunching.



[^1] CTA (2026), “Facts at a Glance”, Chicago Transit Authority, Available at: CTA Facts at a Glance - CTA, Accessed on: 27 September 2026. 
[^2] Stanton, Liam (2026), “CTA has long road ahead to regain riders’ trust”, Chicago Sun Times, Available at: CTA has long road ahead to regain riders' trust - Chicago Sun-Times, Accessed on: 27 September 2026
[^3] Census.gov (2026), "Search: Chicago, Illinois", United States Census Bureau, Available at: https://data.census.gov/all?q=Chicago+city,+Illinois, Accessed on: 2 October 2026