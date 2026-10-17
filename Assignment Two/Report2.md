Matthew Horowitz Mahd Rai Shambawi Sharma

SECTION ONE: REFLECTION AND COMMENTS ON ITERATIONS SINCE REPORT ONE

    After completing assignment one, the group began to reflect on the scope and potential of the project. It was determined that, more data would be needed, and thus more collection should occur, and that the scope of research would have to be tightened. As noted in assignment one, having data samples that affectively represent bus reliability across the entire city, and during multiple time periods, would require a large team and endless hours to visit most (if not all) the neighborhoods in Chicago at all times of the day. Thus, the scope of the project changed.

    Reflection on Data:
    
        Given that data on all bus routes, at all different times of day and days of the week cannot be collected by just three team members, the scope of the data collected had to be refined, in tandem with the data questions--as noted in the next section--. Due to the size of Chicago, the group decided to eliminate most of the bus routes and stops from this project. Given that the most important feature of the CTA is routing passengers from neighborhoods into the downtown core--The Loop, Eastern West Loop/West Loop Gate, Southern River North, and Northern South Loop--, the research was rescaled to focus on North/South, East/West (including NW to SE) routes that feed directly into the Downtown Region.
        Thus, at this point, after consulting the CTA bus route map, the team decided to focus their data collection on the following routes:

            North/South-- 8 (Halsted)
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

SECTION TWO: PREPARE THE DATA

    Before even attempting to prepare the data for analysis, visual inspection was conducted on the data collected so far. Visual inspection was done in two stages:

    1. Pre-python inspection. At this point, all data collected has been entered into an Excel Spreadsheet saved with .xlsx extentension. Each team member maintained their own data set, thus necessitating this first step. During this process:

        1. Each column (attribute) was examined to ensure consistency across the differing datasets. The sets will have to be merged. Missing attributes will cause problems.
        2. Visually check for missing data. Note: missing data will once again be inspected once all files are read into Python, but at this point, a quick visual inspection was done to see if there were any issues before any coding was attempted, and if issues arised, they could be flagged early.
        3. Attribute types. Prior to reading any data into Python, its important that all attributes are stored as the same type of data. Dates and times are particularly attributes that if stored differently can cause issues. Ensuring that days of the weeks are characters was another that needed to be similar. Before reading the data into Python, attributes will also be visual inspected for these types of issues.

    Below is a comment on the visual pre-inspection:

        1. At the start of the visual pre-inspection, the data was organized into multiple files. These were:

            a. 