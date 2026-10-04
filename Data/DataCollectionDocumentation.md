This file describes the data collected for this project--building on from what was discussed in the report--, and outlines the sub folders in the Data Folder of this GitHub repository.

This file is a supplement to the information presented in the report. For the full detailed information on data collection, see the report.

Data Collection Overview: The primary data collected for this project was conducted in person. Members of the group stood in front of bus stops recording when buses arrived and compared them to Ventra times, which were recorded when previous bus departed.

Data Collection Locations: Data was collected across a variety of neighborhoods representing different geographic locations. Downtown, northside residential areas, and entertainment districts were all selected to best model the diverse city of Chicago.

The group initially worked off an initial data dictionary that consisted of the following items and attributes:

Attribute                  Type                 Description
	Observation Number         Numeric              Keeps track of observations
	Date                       Date/Temporal        Date of Observation
	Time                       Date/Temporal        Time of Observation
	Stop Location              Text                 Helps define location of stop
	Stop ID                    Numeric              Helps define location of stop using CTA numeric system
	Next-Bus Arrival           Numeric              Number of Minutes until next bus arrives
	Comments                   Text                 Additional Comments

As data collection began, we realized that further attributes needed to be included, and thus a final data dictionary was yielded.

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

                                                                    

A full version of this data dictionary can be found in the sub-folder: Data->Pilot Data--Excel->DATA DICTIONARY FOR PILOT

As of now, the pilot files found in Data->Pilot Data--Excel contain a total of 28 observations corresponding to observations in the West Loop, River North, and North sides of Chicago. Further data will be captured. Also as of now, we will need to revist the stops to get the CTA IDs. All other direct--non computed-- attributes are accounted for in these pilot data files.

Organization of the Data Folder:
There are 2 subfolders:
--Pilot Data--Excel, which contains the two pilot Excel files and the current working Data Dictionary
--Pilot Data--Ventra Photos, which contains supplemental photos from the Ventra app, plus other additional photos.

