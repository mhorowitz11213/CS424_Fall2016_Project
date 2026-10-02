SECTION ONE: RESEARCH TOPIC, AREAS OF INTEREST, AND DATA EXPLORATION:
	The Chicago Transit Authority is the leading agency for public transportation in the Chicago metropolitan region. The agency, which is comprised of an elevated train system, known as the CTA ‘L’, and bus system serves over 1,000,000 riders per weekday, with the bus alone accounting for approximately 620,000 of those clients.[^1]  Given the importance public transit plays in the City of Chicago, reliable services, especially bus service, which accounts for two thirds of all riders, is essential. However, in the past few years, bus arrivals have become erratic. Buses frequently arrive late, arrive one after another in a bunched-up manner—thereby resulting in long wait times—, or at times don’t arrive at all. Many times, passenger have come to look at the Ventra app, the official app of CTA, Pace, and Metra, for arrival times and have found the “next bus arriving” information displayed on the app to be incorrect. This condition is known as ghost buses, and is something that has vexed riders, CTA officials, business leaders, and other government officials. The CTA has promised to fix this with a new program called the "Frequent Network Initiative" with a promise of 10 minute headways during peak travel times 20 minutes during non peak times, and waitimes to not exceed 30 mins on other lines, with buses expected to arrive no more than 1 minute before and 5 minutes after a scheduled Ventra time. [^3]  As such, the visualization proposed in this research will help Chicagoans better understand bus reliability throughout the city. At this preliminary stage, it is anticipated that the visualization will show average arrival times, wait times, ghost buses, and more. 

SECTION TWO: OBSERVATION AND DATA COLLECTION PLAN:
	To create a visualization necessary to convey bus reliability, data was collected in the field. First, the team met to discuss the general framework they thought would be best for obtaining the data needed to create the visualization. The three team members decided that the best way to collect data would employ direct in the field collection. In person data collection was determined to be the best approach since the only way to compare actual arrival times to Ventra scheduled arrivals is by observing first hand. The rough idea the group had would be for each member to stand in front of a bus stop and observe how long it took for the next bus to arrive, while also recording “the next bus information” displayed on the official Ventra app. This process would then be repeated over and over again. 
	However, before data could be collected, the group had to decide what variables, features and measures needed in order to capture bus frequencies and reliability. These attributes would be decided in a two step process: first decide in general what features the group thinks could be important and necessary to collect, and second to conduct a pilot data collection and then based on the experience, refine the features and data types necessary, as well as methods for collecting data.
	
	Pre-Pilot Features:
	Before codifying the specific variables needed, the group began by creating thinking through what features would be necessary for this type of visualization. Certain variables were obvious: bus arrival times, ventra times, route and stop numbers were the first to come to mind. Next, the group decided that capturing the time when the previous bus arrived (excluding buses that arrived before observations began) would also be important.

	First, a rough idea of multiple domain questions was proposed:
	1. Are buses reliable in the city of Chicago? For this group reliable means do they arrive within 1 minute before, 5 minutes after Ventra time?
	2. Are there variations in bus dependability across the city? What are the variations in bus service across differing socio-economic communities?
	3. The CTA is committed to making changes. Has service gotten better (comparing the final data collection points to the earliest to see if service is improving)?
	4. If certain lines are heavily affected by poor bus service, what other factors might be causing this? Here we plan to overlay demographic data to help visualize and in turn answer this.

	At this point, an initial data dictionary was created (in subsequent sections of this report, a refined data dictionary is presented).

	Attribute                  Type                 Description
	Observation Number         Numeric              Keeps track of observations
	Date                       Date/Temporal        Date of Observation
	Time                       Date/Temporal        Time of Observation
	Stop Location              Text                 Helps define location of stop
	Stop ID                    Numeric              Helps define location of stop using CTA numeric system
	Next-Bus Arrival           Numeric              Number of Minutes until next bus arrives
	Comments                   Text                 Additional Comments

	This pre-pilot data dictionary was a rough sketch. The group decided this data could be used as good starting point for what data would be necessary to create a visualization modeling CTA bus dependability. It should be noted that the group only saw the above features as a basic starting point, and that they were not exhaustive. In order to ensure that the final dataset was a complete as possible, group members decided to capture any further attributes they felt were important during the pilot and to relay these to each other via the group Discord channel. This enabled the group to test determine the sufficiency of the data--using the pilot as an opportunity to evaluate suppositions--while ensuring that all team members agreed and could also test these additional attributes during their pilot.

	Pre-Pilot Data Collection Process:
	With this rough idea of what features would be necessary for this visualization, the data collection process was then discussed. In particular, the group posed these questions first, and then sought to answer them:
	1. If we want to better understand bus arrivals, what routes and areas of the city should we observe?
	2. How should we observe buses, should we stand in front of bus stops during rush hour, the average middle of a workday, evening, night, etc.?
	3. Is this process workable? Knowing that every stop and every route cannot be observed during the semester by a small group of students, what can be accomplished, and will this be enough to carry out a visualization? How long will it take to get just a few observations?

	Final Pre-Pilot Steps:
	With these questions in mind, the group was almost ready to conduct a small pilot data collection.	However, before collecting data, census data was quickly reviewed. Even in the pilot collection, the group wanted to try and cover different demographic regions. These regions needed to be different not just in terms of income and household wealth, but also in terms of lifestyle--vibrant downtown, walkable residential, suburban/bunglow belt, etc. neighborhoods--to ensure that the visualization captures CTA reliability as felt by all Chicago residents. For this part of the research, the group turned to the American Community Survey to look at demographic and lifestyle data to help determine the different socio-economic neighborhoods in the city, allowing the group to select neighborhoods, that even in the pilot, represent the city's population as a whole [^4]. Finally, it is important to note that it will be impossible to cover every bus stop, route, line, neighborhood, or community district in the city. This was acknowledged by the group, and is something we will keep in mind. However, it was decided that a sample that does its best to cover as much variation in the city's socio-economic and demographic makeup is the best we can hope for.

SECTION THREE: PILOT AND DATA COLLECTION:
	Pilot Data Collection Locations and General Description of Process:
	With the initial data dictionary, domain questions, and demographic data in hand, the following data collection was conducted for the pilot study:
	1. Matt covered both the Fulton Market and River North submarkets, representing the downtown region, whose population consists of workers in offices, downtown vistors, downtown residents, and tourists. In this part of the process, Matt observed buses arriving on September 21 at around 9:45 AM in Fulton Market (Halsted and Fulton Market) in the West Loop during morning rush, and again on September 26 at around 5:20 PM in River North (Kingsbury and Grand) in River North, observing weekend traffic into the entertainment and shopping district.
	2. Kaya (Shambhawi) covered Edgewater and Rogers Park residential districts, whose population consists of families and students from the nearby Loyola University (Lakeshore Campus). In this part of the process, Kaya observed buses arriving on September 23 at around 5:45 PM in Rogers Park (Clark and Devon) during evening rush hours (residents returning from work in downtown and work districts), and again on September 28 at around 8:45 AM in Edgewater (Sheridan and Granville) during morning rush hours (residents traveling to work in downtown and work districts).

	Overall, the data collection went fairly smoothly. Buses were easy to observe and to compare to the Ventra App. However there were some difficulties that did become apparent, especially after Matt, who collected data first, reported back his experience. Some of those difficulties were:
	1. Defining the correct time to capture Ventra arrival times--should the anticipated elapsed time be recorded right after a bus left, before it arrived, when? The group discussed this and noted that since the CTA defines on time arrival based on headways--the time from when the previous bus left to the next bus-- Ventra times would be recorded for the next bus at the time when the previous bus left.
	2. Weather conditions. Standing outside in inclement weather is difficult, but necessary. The team decided that as long as the weather holds up sufficiently (such as not downpours), each team member would still attempt to collect data.
	3. Neighborhood coverage. Not all neighborhoods can be covered. Some are to far away, some may have safety issues, and simply in as noted before, there are just too many stops and neighborhoods. Since the team is using the Census Bureau data to analyze neighborhoods that are each distinct and whose observations when compiled together best approximate the city, this method is the best we can do and will be further utilized throughout the assignment.
	4. It is also important to note that this is a timely process. Only 5 to 6 buses on average arrive per hour. This means data collection is timely. Since many team members are flexible schedules this shouldn't be too much of an impediment, however it is important to note that this could become a bigger problem as the group continues to collect data.

SECTION FOUR: DATA DESCRIPTION, CURRENT DATA DICTONARY, AND DOMAIN QUESTIONS
	Our pilot and initial data collection resulted in a small observational dataset consisting of 10 bus-arrival observations across at least three CTA routes and three geographically/demographically distinct areas per group member. The observations currently cover Route 147 at Sheridan and Granville in Edgewater, Route 22 at Clark and Devon in Rogers Park, Route 8 at Halsted and Fulton in Fulton Market and Route 66 at Grand and Kingsbury in River North. Each observation records the date, day of the week, route, stop, stop id, direction of travel, the arrival time predicted by the Ventra application, the actual bus arrival time, the time elapsed since the previous observed bus, the next-arrival time predicted by Ventra, and the actual time until the next bus when it could be observed. We also recorded qualitative comments describing events such as buses arriving early or late, buses appearing to bunch together, and buses being added to the Ventra application after the previous bus had already arrived. The observations therefore contain variation across route, geographic location, date, time of day, direction, predicted arrival, and actual arrival behavior. The pilot dataset provides observations from downtown and near-downtown areas as well as residential areas and college neighborhoods, allowing us to begin thinking about the differences each of the environments. However, the current dataset is still limited in both size and geographic and temporal coverage. The observations were collected during relatively short observation periods and primarily during morning or evening commuting periods, so they do not represent all times of day or all days of the week. The selected locations were also chosen deliberately to represent different types of neighborhoods rather than through a random sample of all CTA stops. Consequently, our observations cannot be used to claim that a particular route or neighborhood is generally more or less reliable across the entire CTA system. There may also be observer-related differences in recording times, particularly when buses arrive very close together or when the Ventra application updates while an observation is taking place.
	The process of turning bus service into structured data required us to make several decisions about what constitutes an observation. We defined an observation around the arrival of a bus at a particular stop, while also recording information about the previous and subsequent buses when possible. This allowed us to represent the phenomenon not simply as whether a bus was "on time," but as a sequence of bus arrivals and intervals between them. The "Ventra Time" and "Real Time" attributes capture the difference between what the passenger-facing application predicts and what actually occurs, while "Observation Previous" and "Actual Next" allow us to study the spacing between buses. The qualitative "Comments" field was retained because some events could not be adequately represented using numerical values alone. For example, a sequence of buses arriving close together may indicate bunching, while a bus appearing in the Ventra application only after a previous bus has arrived may suggest an update or prediction problem.
	At the same time, converting the observations into rows necessarily removed information from the original phenomenon. We did not record the exact location of every bus along its route before arrival, the number of passengers waiting, the number of passengers boarding, traffic conditions, the bus's position before it reached the stop, or the reasons for a delay. We also did not initially record every bus that was expected but failed to arrive, which makes it difficult to distinguish a true "ghost bus" from a prediction that was simply updated or removed by the application. The decision to use the bus arrival as the unit of observation also means that our dataset emphasizes individual arrival events rather than the experience of a passenger waiting continuously at a stop. These limitations became important as we began thinking about the questions our data could actually support.
	Finally, the data we did collect should support a variety of questions. These include direct questions like, "what is the average time between buses on a route?" or "did the CTA meet its frequent bus targets?" as well as future questions that might require deriving data such as "compare the probability between two lines that a bus arrives with 15 minutes?". The goal of our pilot was to not only test the data collection, but also to ensure that we have features necessary to visualize and in turn answer any questions a user might have about CTA bus service. At this time, the group has codified the following data dictionary, which we believe will enable maximum flexibility and support a visualization that allows for the greatest number of research questions.

	After conducting the pilot, the group refined the data dictionary to the following:

	Attribute	 Type	        Description	                                Example
	ID	         Categorical	Keep Track of Records, Unique 
                                identifier	                                1, 2, 3
	Date	     Temporal	    Date of Observation	                        9/21/26
	Day of Week	 Temporal	    Day of the Week	                            M, T, W, R, F, S, Su
	Route	     Categorical	CTA Route Number	                        8
	Stop—Street	 Categorical	CTA Bus Stop	                            Fulton Market & Halsted
	Stop—CTA ID	 Categorical	CTA Bus Stop—CTA unique ID Code	            878
	Direction	 Categorical	Direction of Bus	                        N, S, E, W
	Ventra Time  Temporal       Time Ventra says next bus will arrive
	                            Taken when previous bus leaves or when
								Observations begin                          9:45 AM
	Real Time    Temporal       Actual Time Bus Arrives                     9:50 AM
	Obs Previous Quantitative	Number of minutes between 
                                current bus arrival and previous 
							    bus arrival
							    taken when previous bus leaves or 
								observations begin	                        12
	Obs Next	 Quantitative	Number of minutes until next 
                                bus is expected, when current bus 
							    is leaving.
							    Taken from Ventra app	                    15
	Actual Next	 Quantitative	Number of elapsed minutes between buses	    2
	Comments	 Descriptive	Any additional information, Textual.        Buses bunched. 
                                                                            Bus arrived far later than expected.



	Revised Domain Questions:

	With a working data dictionary, and a pilot data set now created, the group then met to decide what domain questions should be created, and which questions would most likely be asked by a user of a visualization interested in studying, questioning, and exploring CTA bus reliablity.

	So far, the group formulated the following 5 questions:

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

SECTION FIVE: TASK ABSTRACTIONS
	The questions above are domain-specific because they refer directly to CTA buses, Ventra, routes, and bus stops. For visualization design, we need to translate them into more general user tasks. This helps us to avoid tunnel vision, in which the group as a whole decides on a particular chart or map before determining what a user actually needs to accomplish. Furthermore, creating such abstractions will ensure that the visualization is able to answer some of the most pertinent questions, by mapping specific domain level questions to abstract level actions, ensuring that the visualization can support the types of queries and exploration a user will require when exploring a visualization of CTA usablity.

	Below are some of the domain to task mappings the group has created. 

	Domain Question 1: How accurately does Ventra predict the arrival of the next bus?
	Abstract Action: Compare
	Target: Predicted and actual arrival intervals
	Purpose: Determine the magnitude and direction of discrepancies between expected and observed service.

	Domain Question 2: Where and when do buses bunch together?
	Abstract Action: Identify
	Target: Unusually short headways and subsequent long gaps
	Purpose: Recognize individual observations or sequences that indicate irregular service patterns.

	Domain Question 3: Which routes or locations show larger differences between expected and observed service?
	Abstract Action: Compare
	Target: Service reliability measures across routes and stops
	Purpose: Compare reliability across geographic locations and routes.

	Domain Question 4: How does bus reliability vary across time of day and day of week?
	Abstract Action: Compare
	Target: Reliability measures across temporal periods
	Purpose: Determine whether service patterns differ across different times.

	Domain Question 5: Which routes or locations have the greatest variation in bus spacing?
	Abstract Action: Summarize/Compare
	Target: Distribution and variation of bus headways
	Purpose: Understand both typical service frequency and unusual gaps or bunching.

	The first domain question concerns the accuracy of passenger-facing arrival predictions. The primary abstract task is compare, with the target being the predicted and actual arrival intervals. The viewer should be able to compare two related quantitative values and determine whether the prediction was early, late, or substantially different from the observed arrival. For example, if Ventra indicates that the next bus is 15 minutes away but another bus arrives two minutes later, the important task is not simply to identify that bus as a “ghost bus.” Rather, the viewer needs to compare the expected and observed intervals and recognize the magnitude of the discrepancy. This abstraction also allows the same task to be applied to cases where Ventra's prediction is relatively accurate.

	The second domain question concerns the identification of irregular arrival sequences. The primary abstract task is identify, with the target being unusually short headways and the subsequent long gaps that can occur after buses bunch together. This is particularly important for Route 157 in our observations. Three buses may arrive within only a few minutes of one another, followed by a substantially longer period without a bus. The visualization should allow a viewer to recognize this sequence rather than treating each bus arrival as an independent event. The target is therefore not simply “buses that are late.” Instead, it is the pattern of intervals between consecutive observations. This distinction is important because a bus arriving two minutes after another bus may be on time relative to its own schedule while still contributing to an irregular passenger experience.

	The third domain question asks whether observed service patterns differ between routes and locations. The abstract task is compare, with the target being service reliability measures associated with different routes and stops. Relevant measures include actual headways, predicted headways, prediction error, and unusually long or short intervals. For example, the observations from Route 96 show much longer intervals between buses than those observed for Route 157. A viewer should be able to compare these different service patterns without needing to inspect every individual observation. This task is intentionally stated without specifying a map or chart. The comparison could potentially be supported through geographic position, aligned route views, small multiples, or another visual representation.

	The fourth domain question concerns temporal variation in service. The abstract task is again compare, with the target being reliability measures across different temporal periods. Our observations were collected at different times of day, including early morning, morning rush, evening rush, and midday. The viewer should be able to compare characteristics such as headway, prediction error, and service gaps across these periods. This task is especially relevant because the meaning of a long headway depends partly on the normal frequency of a route. A 30-minute interval may be relatively normal for Route 96 but would represent a substantially different service pattern on a route where buses normally arrive every few minutes. The visualization therefore needs to support comparison while retaining the temporal context of each observation.

	The fifth domain question asks which routes or locations have the greatest variation in bus spacing. This involves both summarizing and comparing. The target is the distribution of headways, rather than a single average headway. This distinction is important because an average can conceal irregular service. For example, a route could have an average headway of approximately 10 minutes while actually alternating between buses arriving two minutes apart and gaps of nearly 20 minutes. The average alone would not communicate this pattern. A useful visualization should therefore allow viewers to understand both the typical spacing of buses and the extent to which individual observations deviate from that pattern.

	These tasks are related but address different aspects of bus reliability:

	1. Compare predicted and actual values to understand prediction accuracy.
	2. Identify unusual sequences of short and long headways to detect bunching and service gaps.
	3. Compare service characteristics across routes and locations.
	4. Compare service characteristics across different temporal periods.
	5.Summarize and compare the variation in headways rather than relying only on averages.

	Together, these abstractions shifted our project away from treating “ghost buses” as the single outcome of interest. The field observations showed that reliability is better understood as a collection of related phenomena: prediction discrepancies, irregular spacing, bunching, long service gaps, and differences in service frequency.

SECTION SIX: VISUALIZATION SKETCHES

--SCRATCH NOTES: map to enable direct comparisons across neighborhoods, socio economic regions, and even bus lines. Map for this is essential because we want referential comparisons.

SECTION SEVEN: SUMMARIZING
	This project has been a iterative work in progress. As a group, we really wanted to visualize a major issue affecting the lives of Chicagoans on a daily basis. Bus reliability has been in the news over the past few years, and with over 600,000 daily rides taken on the bus system, it's worth exploring this topic through visual analysis.
	But with that noted, we as a group really did not know how to tackle this topic. So we decided to follow the iterative approach, starting with the broadest goals, testing suppositions--including data collection--and then refining our research.
	This process entailed:
	1. Deciding on what data sources are necessary: could this research be done with simple API calls to Ventra or was in the field data collection necessary.
	Here, we as a group realized that simply put if we wanted to see how accurate and reliable both the bus system and the Ventra Bus Tracker really are, then deploying a team to the field became essential.
	2. Deciding on the features and data types necessary: what features really are essential, how should we time buses, are there aspects of this research they the group hasn't accounted for. 
	As noted in Section Two of this report, we had a rough idea of what features and data we needed to collect. But like all research, until one starts collecting data--in our case going out to individual bus stops-- it is impossible to know exactly what is necessary, what can be captured, and how it should be captured. Initially, the group thought that having route number, date and time, and the number of minutes until the next bus would be enough. But as we continued to work on our dataset, we began to realize that there were attributes and factors we did not account for. These include:
	-When should Ventra times be captured. Initially we did not realize how important having standardized processes would be to ensure that the data captured by members of the group would remained standardized and as such could be unified. It might seem trivial, but without a unified manner of recording this time, making direct comparisions between Ventra predicted, and actual arrival times could not be made across the entire data set, unless this issue was accounted for. The group was ultimately able to agree that the best way to capture elapsed time--as predicted by Ventra app--was to record one reading, when the previous bus departed. But, this still left the question of what to do with the Ventra time corresponding to the first bus set to arrive when members of the team  arrive at a stop, and begin recording observations. In an ideal world, the group members would exclude any observations related to the first bus to arrive during each data collection cycle, and begin all observations starting with the second bus, to ensure uniformity, across all observations. But because of the length of time it takes to record arrivals at a stop, this correction is simply not feasable. For now, all members of the team record the predicted Ventra time and expected elapsed minutes as soon as they arrive at a stop, but as we work through this project we might need to adjust this approach.
	-Weather, anticipated construction, or other advisories. There are many factors that can affect bus performance, and these are supposedly accounted for in the real time updates that go into calcuating Ventra's predicted arrival time. [^5] Right now, the CTA and Ventra account for long term construction projects in their prognostications, for example the Chicago/Halsted rebuild affecting the 8 and 66 Bus lines. But weather delays and travel advisories can affect arrivals. As now the group is unsure how to account for these, and will need to further discuss. As of this point in time, the group has decided to record such anomalies--which appear to affect a minority of bus arrivals we've encountered--by making note of such in the comments variable (noted in the data dictionary). In the future, we may need to either compute a variable based on the comments, or create an entirely new feature(s) to account for these instances.



[^1] CTA (2026), “Facts at a Glance”, Chicago Transit Authority, Available at: CTA Facts at a Glance - CTA, Accessed on: 27 September 2026. 
[^2] Stanton, Liam (2026), “CTA has long road ahead to regain riders’ trust”, Chicago Sun Times, Available at: CTA has long road ahead to regain riders' trust - Chicago Sun-Times, Accessed on: 27 September 2026
[^3] CTA (2026), "CTA Launches New Frequent Network For Buses", Chicago Transit Authority, Available at: https://www.transitchicago.com/cta-launches-new-frequent-network-for-buses/, Accessed on: 2 October 2026, Smentkowski, Elena (2026), "The CTA Is Expanding Bus Service Citywide--Here's What It Means For You", Secret Chicago, Avaliable at: https://secretchicago.com/cta-expanded-bus-service-chicago-2026/, Accessed on: 2 October, 2026, CTA (2023), "Chicago Transit Authority Service Standards and Policies", Chicago Transit Authority, Available at: https://www.transitchicago.com/assets/1/6/Chicago_Transit_Authority_Service_Standards.pdf, Accessed on: 2 October 2026. 
[^4] Census.gov (2026), "Search: Chicago, Illinois", United States Census Bureau, Available at: https://data.census.gov/all?q=Chicago+city,+Illinois, Accessed on: 2 October 2026
[^5] CTA (2026), CTA Bus Tracker, Chicago Transit Authority, Available at: https://ctabustracker.com/home, Accessed on: 2 October 2026.