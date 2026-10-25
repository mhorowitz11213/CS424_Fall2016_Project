# This is the ReadMe for Assignment Two:

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
        1. Figure_1.json --this is the Vega Lite code for Figure 1 from our visualization sketches
        2. Figure_10.json --this is the Vega Lite code for Figure 10 from our visualization sketches
        3. Figure_11.json --this is the Vega Lite code for Figure 11 from our visualization sketches
        4. Final_vis.json --this is the Vega Lite code for the final visualization that will be used in Assignment Three
        5. Figure_1.txt --a text file containing the comments and citations for Figure_1.json
        6. Figure_10.txt --a text file containing the comments and citations for Figure_10.json
        7. Figure_11.txt --a text file containing the comments and citations for Figure_11.json
        8. Final_vis.txt --a text file containing the comments and citations for Final_vis.json
        9. Final_vis.html --this is the HTML version of the final visualization that will be used in Assignment Three

    7. Report2.md --this is the report

    In terms of flow the group suggests that in order:
    1. DataPreparationandExplorations.xlsx is examined first
    2. CS424DataCleaning.ipynb is run 
    3. CS_424_Exploratory_Research_on_Primary_Data.ipynb is run
    4. CS_424_Secondary_Data_Explore.ipynb is run
    5. All Vega Lite code is run-- in order: Figure 1, Figure 10, Figure 11, and Final_vis in order to best understand the workflow
   

## How to Run and View the Visualizations

You can explore our visualizations in two ways: **using the Vega-Lite Online Editor** or **opening the standalone HTML version** in your browser.

### Option 1: Run a Visualization in the Vega-Lite Online Editor

Use this option if you want to view the visualization directly in the editor or inspect its Vega-Lite specification.

1. **Open the Vega-Lite Online Editor:**  
   Visit [https://vega.github.io/editor/](https://vega.github.io/editor/).

2. **Choose a visualization:**  
   Navigate to the visualization you want to explore in this repository. Each visualization has its own Vega-Lite specification file (`.json`).

3. **Open the specification file:**  
   Open the corresponding `.json` file in your preferred code editor or IDE, such as VS Code.

4. **Copy the specification:**  
   Select the entire contents of the JSON file:
   - Windows/Linux: `Ctrl + A`, then `Ctrl + C`
   - macOS: `Cmd + A`, then `Cmd + C`

5. **Paste the specification into the online editor:**  
   Return to the Vega-Lite Online Editor. Select the existing specification in the editor's code panel, replace it with the copied JSON, and paste your code.

6. **Run the visualization:**  
   Click **Run** in the editor to render the visualization. If the visualization does not update immediately, make sure the entire specification was copied and pasted correctly, then run it again.

7. **Interact with the visualization:**  
   Depending on the visualization, you may be able to hover over marks to view tooltips, select bus routes, change filter options, or explore other interactive elements.

**Note:** Some visualizations load external datasets, geographic boundaries, or other resources from online sources. An internet connection is required for these resources to load. If a visualization does not render correctly, check the editor's error panel for details.

### Option 2: Open the Standalone HTML Version

For the quickest way to explore the final visualization designs, use the HTML versions included in this repository.

1. **Locate the HTML file:**  
   Find the `.html` file corresponding to the visualization you want to view.

2. **Open the file:**  
   Download or clone the repository if you have not already done so. Then double-click the HTML file, or right-click it and select your preferred web browser.

3. **Explore the visualization:**  
   Once the page loads, use the available interactive controls to explore the data. Depending on the visualization, these may include route selection, filters, hover tooltips, and other interactive features.

4. **Troubleshoot loading issues:**  
   If the visualization or its data does not load, make sure you have an active internet connection. If opening the file directly does not work as expected, try serving the HTML file through a local development server.

**Recommended:** If you simply want to view and interact with the final designs, start with the standalone HTML version. If you want to inspect or modify a visualization's Vega-Lite specification, use the online editor.