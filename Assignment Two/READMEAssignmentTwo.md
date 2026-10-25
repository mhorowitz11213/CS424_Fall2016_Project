#This is the ReadMe for Assignment Two:

The Assignment Two folder contains all the information needed to run the Assignment Two Submissions. In this folder, you will find:

1. Data Preparation Folder--containing:
    1. CS424DataCleaning.ipynb--this Jupyter notebook file was used to clean the data.
        To run this file you will need:
        DataPhase2Sharma.xlsx
        DataPhase2Rai.xlsx
        DataPhase2Horowitz.xlsx
        stops.txt
        Files (see below for their location)
        The Jupyter notebook file is optimized to run in Google Colab. Simply upload the file to a Colab enviroment and load the four above files into the console to run.
    2. DataPreparationsAndExplorations.xlsx--this excel file was used for the Excel based visual inspection

2. Data Second Assignment Folder--containing:
    1. CleanedData-10-18-26.csv -- this is the file output from CS424DataCleaning.ipynb
    2. DataPhase2Horowitz.xlsx
    3. DataPhase2Rai.xlsx
    4. DataPhase2Sharma.xlsx

        -The above three datasets contain data collected by the three members of the team, including the data collected during Assignment One, plus subsequent collections up until 10/18/2026

    3. Exploratory Data Folder--containing:
        1. CS_424_Exploratory_Research_on_Primary_Data.ipynb--this Jupyter notebook file was used to do exploratory analysis on the data collected by the team members.
        To run this file you will need: CleanedData-10-18-26.csv
        The Jupyter notedbook file is optimized to run in Google Colab. To run this file, load it into the Colab enviroment and then upload the file: CleanedData-10-18-26.csv into the console.

        2. CS_424_Secondary_Data_Explore.ipynb--this Jupyter notebook file was used to do exploratory analysis on the secondary census data used to augment bus information in the visualizations.
        To run this file you will need: Census_Data_-_Selected_socioeconomic_indicators_in_Chicago,_2008_–_2012_20261023.csv
         The Jupyter notedbook file is optimized to run in Google Colab. To run this file, load it into the Colab enviroment and then upload the file: Census_Data_-_Selected_socioeconomic_indicators_in_Chicago,_2008_–_2012_20261023.csv into the console.

    4. Screenshots Folder--containing:
        1. Primary_Data_Analysis: Figures 1-10. PNG files that are all of the figures generated in the above CS_424_Exploratory_Research_on_Primary_Data.ipynb file that were placed into the report.
        2. Secondary_Data_Analysis: Figure 21: The figure generated from CS_424_Secondary_Data_Explore.ipynb and placed into the report
        3. Vega_Lite: The Screenshots of the Visualizations created in PNG format
            -Figure 1
            -Figure 10
            -Figure 11
            are the first three iterations of the Assignment
            -Final Vis is the screenshot of the final visualization that will be used in Assignment Three

    5. Secondary Data Folder-- containing:
        1. Census_Data_-_Selected_socioeconomic_indicators_in_Chicago,_2008_–_2012_20261023.csv this is Census Data supplied by the City of Chicago
        2. mdb-389-202609160157.zip a zip file from the Mobility Database of infomration supplied from the CTA
        -note stops.txt file is located inside this zip folder
        3. Sources.md a markdown file that gives the websites to the secondary data was aquired.

    6. Vega Lite Folder-- containing:
        1. 

    7. Report2.md --this is the report

    In terms of flow the group suggests that in order:
    1. DataPreparationandExplorations.xlsx is examined first
    2. CS424DataCleaning.ipynb is run 
    3. CS_424_Exploratory_Research_on_Primary_Data.ipynb is run
    4. CS_424_Secondary_Data_Explore.ipynb is run
    5. All Vega Lite code is run-- in order: Figure 1, Figure 10, Figure 11, and Final_vis in order to best understand the workflow
   

