Matthew Horowitz Mahd Rai Shambawi Sharma

SECTION ONE: REFLECTION AND COMMENTS ON ITERATIONS SINCE REPORT ONE

    After completing assignment one, the group began to reflect on the scope and potential of the project. It was determined that, more data would be needed, and thus more collection should occur, and that the scope of research would have to be tightened. As noted in assignment one, having data samples that affectively represent bus reliability across the entire city, and during multiple time periods, would require a large team and endless hours to visit most (if not all) the neighborhoods in Chicago at all times of the day. Thus, the scope of the project changed.

    Reflection on Data:
    
        Given that data on all bus routes, at all different times of day and days of the week cannot be collected by just three team members, the scope of the data collected had to be refined, in tandem with the data questions--as noted in the next section--. Due to the size of Chicago, the group decided to eliminate most of the bus routes and stops from this project. Given that the most important feature of the CTA is routing passengers from neighborhoods into the downtown core--The Loop, Eastern West Loop/West Loop Gate, Southern River North, and Northern South Loop--, the research was rescaled to focus on North/South, East/West (including NW to SE) routes that feed directly into the Downtown Region.
        Thus, at this point, after consulting the CTA bus route map, the team decided to focus their data collection on the following routes:

            North/South-- 8 (Halsted), 157, 146 (Inner Lakeshore), 147 (Outer Lakeshore), 36 (Broadway), 22 (Clark)
            East/West-- 20 (Madison), 65 (Grand), 66 (Chicago), 56 (Milwaukee) [Note the Milwaukee bus is officially listed as a N-S bus, but travels on a NW-SE heading, thus it has been included in the E/W section]

    Reflection on Questions:

       Prior to this report, the group identified the following domain questions:

            Question 1 -- How accurately does Ventra predict the arrival of the next CTA bus?

            Question 2 -- Where and when do buses appear to bunch together?

            Question 3 -- Which locations and routes show larger differences between expected and observed service?

            Question 4 -- How does bus reliability vary across different times of day and days?

            Question 5 -- Which routes or locations have the greatest observed variation in bus spacing?



        Given the inability to visit all neighborhoods of Chicago, many of the original research questions had to either be eliminated or refined, while others can be retained. Questions 1 and 2 are general, and when applied to specific routes, can still be properly examined and thus will be retained.
    
    Further Reflections on Data Collection:

        As of now, the general method of collecting data--observing buses and comparing to Ventra app--will continue. However, upon discussing the progress the team was making, it became apparent that redunant variables--including the delta bus times (time elapsed from previous bus arrival) was redundant, as this attribute can be calculated later when creating the visualization. As a result, all attributes will be retained in the final data set, but many of these attributes will be calculated by the computer during the data cleaning process and stored, rather than being computed at the time of observation.

SECTION TWO: PREPARE THE DATA--PRIMARY DATA

    Before even attempting to prepare the data for analysis, visual inspection was conducted on the data collected so far. Visual inspection was done in two stages:

    1. Pre-python inspection. At this point, all data collected has been entered into an Excel Spreadsheet saved with .xlsx extentension. Each team member maintained their own data set, thus necessitating this first step. During this process:

        1. Each column (attribute) was examined to ensure consistency across the differing datasets. The sets will have to be merged. Missing attributes will cause problems.
        2. Visually check for missing data. Note: missing data will once again be inspected once all files are read into Python, but at this point, a quick visual inspection was done to see if there were any issues before any coding was attempted, and if issues arised, they could be flagged early.
        3. Attribute types. Prior to reading any data into Python, its important that all attributes are stored as the same type of data. Dates and times are particularly attributes that if stored differently can cause issues. Ensuring that days of the weeks are characters was another that needed to be similar. Before reading the data into Python, attributes will also be visual inspected for these types of issues.
    
    This pre-Python exploratory search was conducted in Excel first to minimize any conflicts that may arise once the data is read into a Python environment. Ordinarily, this step would be deemed inefficient if working with a very large data set. However, at this time, the data set contained a little more than 100 observations, and as such, conducting exploratory and cursory data checks first in Excel is manageable. It should also be noted that the group is still collecting data, and will continue to do so throughout the semester.

    Below is a comment on the visual pre-inspection:

        1. At the start of the visual pre-inspection, the data was organized into multiple files. These were:

            a. Data--DataPhase2Horowitz
                     DataPhase2Sharma
                     DataPhase2Rai
        2. Next, each attribute was inspected. To do this a new excel file was created:
            a. The column names from each of the three excel files were pasted in one on top of another. This ensures that there are no missing attributes and that the attributes in the data set perfectly align. Note, in regards to column name changes, the group plans on reading these Excel files in without headers and then manually adding in column names using Pandas functions.
            b. Next, the data from each of the three above files was pasted in, one on top of the other in order to check that there is consistency in data types and to quickly see if any observations are missing data.

        In this step, the following should be noted:
            a. The columns were first pasted one on top of the other to be inspected. All columns matched, though some of the exact column names differed:
            -DataPhase2Horowitz used "Observation ID","Stop" and "StopID", while DataPhase2Rai and DataPhase2Sharma used "ID", "Stop-Street", and "Stop-CTA ID", but the attributes themselves were the same and all columns aligned. 
            b. After pasting the data, and excluding the Observation ID column--this was an value internal to each group member--, the data was inspected:
                -First, there appeared to be a quite a few missing values for "Observation Previous (in mins)" in DataPhase2Rai excel sheet. This is not a major issue since this is a calculated field, and as noted earlier in this report, a variable that can easily be calculated from the other data held in this excel file.
                -Second, in the DataPhase2Horowitz file, 20 stops carry the number 0 for bus stop id. This is because Loop Link stops do not display their stop number. This will be fixed in later steps when the group downloads the CTA GTFS data (see next section).
            c. Next, the data was read into a Python and placed into a Pandas dataframe. To simplify this process, theses steps were conducted using Google Colab.
                -A quick visual inspection was done again to make sure that all attributes are present and aligned and that there was no missing data. Each dataframes shape was also calculated and a list of column names returned to ensure data consistency.
                -Next, column names often had different spacing. White spaces were stripped from the end of column names to make it easier to work with and to ensure that data could be compared.
                -Next, the data types were inspected. To ensure that data types can easily be merged, all data types need to be the same. During this step, it should be noted that there were some discrepencies found. In particular, the variables corresponding to minutes were often found to be either float64 or int64. Whenever this discrepency arrived, the data was converted to int64 since the attributes where this discrepancy arised dealt with minutes, a discrete integer value. However, because some of the data in these attribute fields had values like NA, the group decided to replace any values of this kind with 999--since 999 minutes was not a real value this gibberish value was used in lieu of NA--.
                -Next, all columns were given the same name to ensure data consistency
                -Columns were then checked to make sure they had the same name and data type
                -Finally all three datasets were combined to form temp_df2, the combined dataset.
            d. Once the combined dataframe temp_df2 was created, each variable was inspected to make sure that there were no missing or incorrect attributes.
            e. Next, the stops with CTA-Stop ID 0 (the Loop Link stops), were correctly coded by adding in the codes stored in the CTA masterfile (see Secondary Sources folder in GitHub). 
            f. Finally, the geo coordinates for each stop latitude and logitude were appended. These were checked against Google Maps to ensure correctness.
            g. All N/A were handled, except in the comments section. This is an attribute that the group plans on using to help determine if certain Booleans, like reliability, should be created, and if so, how they should be handled. As of now, having missing attributes in this field is not an issue.
            h. The data was written out to a CSV file so that it can be used. Note, at this stage all columns were included, though some of these attributes are redunant and can be calculated on the fly.

SECTION THREE: EXPLORE THE DATA AND DISCUSS SECONDARY DATA
        After preparing the primary data, cleaning and inspecting data quality, the group then turned to exploring both the data collected and any secondary data needed to answer the domain questions. Census and City of Chicago produced data was inspected to help add demographic data allowing the group to create visualizations that depict differences in socio-economics between the West and North sides of the city. In this section, the group analyzed some interesting patterns found in the primary data we collected, plus interesting features in the secondary data downloaded from the City of Chicago portal.

        Primary Data:

        After cleaning up the data, and producing a finalized dataset on October 18, 2026--note data collection will continue throughout this project, as of now this is the data set the group will use for submission two to ensure consistency--, exploratory research on the data was conducted.

                1. Basic distributions were generated. This was done to ensure that the data is fairly balanced. While the group will collect more data throughout this research, ensuring the data is fairly balanced will allow the group to check for interesting statistical anomalies, like bus bunching, or frequent delays. Such statistical measures will require calculating standard deviations or t-tests. This can only be done if data is fairly balanced. This step was conducted in two ways. First, basic counts by lines were generated, and then second, the frequencies by bus line were plotted into a bar chart to allow the group to see the distribution in a more visual way.
                
                Below is the output for the bar chart:

                <INSERT BAR CHART HERE>

                Here we can see that with the exception of Route 66 Bus (more of which will be collected in the subsequent week), the data looks fairly balanced, with most routes having anywhere from 8-12 observations. As such, provided Route 66 is excluded from statistical analysis, all other lines can be examined for insights.

                2. 

SECTION FOUR: IMPLEMENT VISUALIZATION ALTERNATIVES

    Figure 10:
        What question or task it supports.
            	1. Compare observed bus reliability across different geographic locations.
	            2. Identify locations with unusual bunching or long service gaps.
	            3. Compare predicted and actual bus arrivals at selected locations.
	            4. Locate routes or stops where service patterns warrant further investigation.
        Which data attributes it uses.
                1. Route
                2. Stop location and CTA stop ID
                3. Direction
                4. Date and time
                5. Real Time
                6. Ventra Time
                7. Observation Previous
                8. Observation Next
                9. Actual Next
        The main marks and visual channels.
                1. Map: route lines and stop points
                2. Map position: geographic location
                3. Timeline points: individual bus arrivals
                4. Horizontal position: arrival time
                5. Distance between points: actual headway
                6. Secondary predicted marks: Ventra arrival predictions
                7. Distance between predicted and actual marks: prediction error
                8. Selection/highlighting: selected route or stop
        Why you tried this approach.
                The map-based visualization was chosen to provide geographic context for bus reliability across Chicago. By displaying bus routes spatially, the visualization allows users to identify where delays and irregular headways occur and whether certain areas experience more reliability issues than others. This approach supports targeted analysis by connecting bus performance data to real-world locations.
        What worked and what did not.
                What worked:
                - The map provided a familiar geographic reference, making it easier to understand where bus routes operate across the city.
                - Displaying multiple routes together helped users compare their geographic coverage and identify areas of potential interest.
                - The spatial approach offered a useful way to explore bus reliability in relation to specific routes and locations.
                What did not work:
                - Displaying multiple routes and observations on the same map could make it difficult to distinguish individual patterns, especially when routes overlapped.
                - The map did not communicate the magnitude of headway differences as directly as a quantitative chart.
                - Technical issues with rendering the map and displaying the route data made it difficult to achieve the intended visualization reliably.
                - Design decisions regarding keeping the map static versus allowing for zooming and panning affected the usability of the visualization.
                - Design decisions regarding keeping the rectangular view at the bottom confined to a strict one hour window limited the ability to see longer-term patterns in bus reliability.
        Whether you decided to keep, modify, combine, or abandon it.
                I decided to modify and retain the map-based visualization as a complementary view of bus reliability. It is useful for understanding the geographic distribution of routes and identifying where further investigation may be needed. However, rather than relying on the map alone, I would combine it with a quantitative visualization that makes headway deviations easier to compare. This allows the map to provide spatial context while another view communicates the underlying data more precisely. I abandoned the zooming and panning functionality in favor of a static map to reduce complexity and improve usability, while still allowing users to explore the data through other linked visualizations. I also abandoned the strict one-hour window in favor of a more flexible time range to allow users to explore longer-term patterns in bus reliability.

    Figure 11:
        What question or task it supports.
                1. Identify buses associated with unusually uneven service spacing.
                2. Compare headway patterns across routes.
                3. Determine whether short headways are followed by long service gaps.
                4. Determine whether long gaps are followed by closely spaced buses.
                5. Identify routes with the strongest evidence of bunching.
        Which data attributes it uses.
                1. Observation Previous
                2. Actual Next
                3. Route
                4. Stop
                5. Direction
                6. Date
        The main marks and visual channels.
                1. Point: individual bus observation
                2. X-position: actual headway from previous bus
                3. Y-position: actual headway to next bus
                4. Diagonal reference line (y = x): balanced service
                5. Distance from diagonal: degree of headway imbalance
                6. Position above/below diagonal: direction of the imbalance
                7. Grouping/selection: route
        Why you tried this approach.
                The scatterplot was chosen to compare the previous bus headway with the actual time until the next bus arrived. Each point represents an observation, with the previous headway on the x-axis and the actual next headway on the y-axis. A reference line representing \(y=x\) provides a baseline for comparison: points near the line indicate similar consecutive headways, while points above or below it indicate differences between the two intervals. Color distinguishes bus routes, and filled versus hollow points distinguish travel directions.
                This approach provides a direct way to examine headway balance, compare observations across routes, and identify unusually large differences.
        What worked and what did not.
                What worked:
                - The scatterplot made it easier to compare previous and actual next headways quantitatively.
                - The \(y=x\) reference line provided an intuitive baseline for identifying observations where consecutive headways differed.
                - Using different colors for routes and different point fills for directions helped distinguish observations within the same chart.
                - Excluding invalid observations with a headway value of 999 helped prevent those values from distorting the displayed patterns.
                - The chart supported comparisons across routes without requiring users to interpret the geographic layout of the city.
                What did not work:
                - When many observations were plotted together, overlapping points could make dense areas difficult to interpret.
                - Distinguishing several routes through color could become challenging as the number of categories increased.
                - The scatterplot did not show where the observations occurred geographically, so it could not independently explain the locations of reliability issues.
                - The visualization required appropriate filtering and legend or dropdown controls to make comparisons between individual routes and directions manageable.
        Whether you decided to keep, modify, combine, or abandon it.
                I decided to retain and refine the scatterplot because it provides a clearer quantitative comparison of consecutive bus headways than the map alone. The reference line helps users interpret differences, while route colors and direction markers provide additional context. I would improve the visualization by refining the filtering controls and reducing visual clutter when many observations overlap. I would also combine it with the map-based visualization so that users can first identify geographic patterns and then use the scatterplot to investigate the magnitude and distribution of headway differences.

SECTION FIVE: INTERACTION AND MULTIPLE VIEWS