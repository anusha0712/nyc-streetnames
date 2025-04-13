# Visualizing School Book Bans in America

## Introduction

Hello! My name is Anusha Subramanian and I'm a Data Journalist at Columbia Journalism School. I'm primarily interested in anything that provides critical commentary on the human condition and specifically interested in public health, culture with a South Asian focus, books, poetry and lots and lots of food. You can find my work [here](https://anusha0712.github.io) and this project's completed story [here](https://anusha0712.github.io/nyc-streetnames/).

The way that we structure our urban landscape has always intrigued me. Who we choose to memoralize or celebrate is often telling of the culture we amplify. Street names are urban markers that often slip under the radar but hold years of histories and methodological decisions within themselves. For this project, I was interested in untangling the nunances of who is celebrated in the very bones of New York City, and who is not. 

For this, I am using the dataset put together by NYC Department of Records and Information Services (DORIS). You can find that [here](https://data.cityofnewyork.us/City-Government/NYC-Honorary-Street-Names-Map-Street-Line-/xesp-yqsx/about_data)

## Goals

My goal is to analyze the patterns in of honorific street names in New York City . 

Some questions that guided my exploratory data analysis were:

1. Is there a gender gap in the people being commemorated? 
    - If yes, how vast is it?

2. Are there boroughs where such disparity shows up more? 
    - What are the demographics of the boroughs compared to representation?


Personally, I believe that this is a story that has a lot of public value since commemorative street names are bestowed by the City Council. For this project, the main aim is to focus on narrative structure in my storytelling and writing about data with clarity and simplicity. 


## Frameworks Used

**Code**
- Python (pandas, geopy)
- HTML 
- Excel
- QGIS for initial exploration

**Data Visualization**
- [Datawrapper](https://www.datawrapper.de)
- Adobe Illustrator


## Quick Guide To The Files FIGURE THIS OUT AFTER

1. `data_analysis` directory: Contains all the main files required for analysis 
    - `nyc_honorary_streetnames.csv` : raw data files
    - `nyc_honorary_stnames.ipynb` : main ipynb for analysis 
    - `mapping` directory: contains everything relevant for the maps in the project     
        - geojson files per category (male, female etc.) and overall
        - files with point coordinates for the midpoints of all the honorfic streets
        - `mapping_streetnames_nyc.ipynb` : code for generating the coordinates and geometries required for mapping


2. `visuals` directory:
    - contains all the main visuals used in the main project


## Methodology 

Here is the framework that I followed for my analysis. The code notebook contains more detailed commentary for the individual steps.

1. Download NYC Honorary Street names dataset. It has close to 900 rows

2. Go row by row and manually classify whether the honorific street names honors men, women or groups.

3. Clean and Standardise Data. Few of the steps include:
    - The data is generally in good shape but required transformations for mapping purposes

    - For example, I toyed with the idea of mapping entire streets but ultimately went with visualizing the midpoint of every street as a point on the map of NYC. This required using geopy to find the centroid of the geometry already present in the dataset.

    
4. Grouping, Counting and Pivoting data for analysis and visualization

5. Visualization:
    
    - Datawrapper graphs were embedded directly into the HTML

    - Made a symbol map on Datawrapper using the centroid points of all the streets. 

6. Coded a narrative "stacks" storytelling template that is a mix of static and scrollytelling (HTML framework) to bring the visualizations together into a story.


## Limitations - "Wants" vs "Needs"

I was able to accomplish everything I "needed", which includes a contextual analysis and visualizations on the gender disparity apparent in the way we celebrate people by honoring them in the street names of New York City. 

Given the time, I would have categorized the dataset into two more segments: What are people being honored for and what is the racial representation inherent in our co-named streets?

I did not have the time for the research required to responsibly categorize the race of individuals but I believe it will show up some interesting patterns, particularly when compared with the demographics of the particular boroughs or census tracts.


### Limitation

The dataset is in very good shape. 

The "Biographical Information" column is really useful in getting a sense of who the street is named after. However, when you download it from OpenData NYC, the information for that column is often incomplete - sometimes even abruptly cut off mid-sentence in some rows. Therefore, I constantly referred to DORIS' [visualization](https://www.arcgis.com/apps/instant/basic/index.html?appid=7c667aa2fa224684962cac5fa10ec0fd) of the data. It was updated recently to improve the search functionality. You can look up additional information about a particular street easily, using this tool.


## Note on AI use

Claude AI was used in this project, primarily to help design small elements of the webpage.

**No tasks or data cleaning were performed using ChatGPT or Claude AI.**


## Questions

I would love to chat more about my work, including this project! If you have any questions, please [email me!](mailto:as7500@columbia.edu)


    



