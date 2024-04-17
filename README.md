![Alt text](/images/project_banner.png)


---

# Project Title:  Statistical Modeling with Python

## Project Overview

This repository contains a data analysis project that integrates data from CityBike sharing systems and Points of Interest (POIs) from services like Foursquare and Yelp. The project aims to uncover the relationship between bike-sharing usage and urban amenities.

## Repository Structure

### `/data`

- `CityBike_Longlat.csv`: This CSV file includes the longitude and latitude information of CityBike stations.
- `CityBikeCoordWithBikeNum.csv`: Contains detailed data about the bike stations, including the number of available bikes.
- `Foursquare_Biz_Data.csv`: Business data retrieved from Foursquare API centered around the bike stations.
- `JoinedData.csv`: The combined dataset that merges CityBike data with POIs data from Foursquare and Yelp.
- `Yelp_Restaurant_Data.csv`: Information about restaurants in the vicinity of bike stations sourced from the Yelp API.
- `yelpRestBikeData.db`: An SQLite database containing the compiled data for easy query and analysis.

### `/images`

- `heatmap_viz_02.png` & `heatmap_viz.png`: Heatmaps visualizing different aspects of the data.
- `project_banner.png`: The banner image for the project, useful for documentation and presentations.
- `relplot.png`: A relational plot that demonstrates correlations within the data.

### `/notebooks`

- `city_bikes.ipynb`: Jupyter notebook containing the exploratory analysis of CityBike data.
- `joining_data.ipynb`: Notebook documenting the process of combining datasets from different sources.
- `model_building.ipynb`: Contains the regression model and its evaluation.
- `yelp_foursquare_EDA.ipynb`: Dedicated notebook for exploratory data analysis of Foursquare and Yelp data.

### Miscellaneous Files

- `assignment.md`: Assignment text detailing the project requirements and steps.
- `README.md`: The file you're reading, providing an overview and guide to the repository.

## Getting Started

To get started with this analysis:

1. Clone the repository to your local machine.
2. Install required dependencies listed in `requirements.txt`.
3. Explore the datasets in the `/data` directory.
4. Run the Jupyter notebooks in the `/notebooks` directory to follow the analysis.

## Requirements

This project requires Python 3 and the following Python libraries installed:

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Statsmodels
- SQLite

Note: You can install these libraries using `pip`


---
## An overview of my approach

### Part 1: Connecting to CityBikes API

I began by delving into the CityBikes API documentation to understand its structure. I queried the API to familiarize myself with the data returned. I selected a city from the CityBikes network and retrieved detailed information about all available bike stations in that city, focusing on latitude, longitude, and the number of bikes at each station. The JSON responses were parsed and loaded into a Pandas DataFrame. I completed the entire process and documented my steps and findings in a Jupyter notebook titled `city_bikes.ipynb`.

### Part 2: Connecting to Foursquare and Yelp APIs

I set up and authenticated my connections with the Foursquare and Yelp APIs, securely storing the authentication tokens as environment variables to ensure the security of my keys when committing code to GitHub. For each of the bike stations identified in Part 1, I used these APIs to retrieve information on nearby restaurants, bars, and other POIs. I created two separate DataFrames to organize the data from Yelp and Foursquare and conducted a thorough comparative analysis to evaluate the quality of data provided by each service. I defined my own criteria for 'coverage' and documented the entire exploratory process in a Jupyter notebook called `yelp_foursquare_EDA.ipynb`.

### Part 3: Joining Data

I joined the data from the CityBikes bike stations with the POI data from Foursquare and Yelp into a new DataFrame. Exploratory data analysis was carried out using various visualization techniques to uncover patterns. I also created my own SQLite database, thoughtfully considering the structure to store the collected data, and took measures to validate the data integrity. The entire process was meticulously detailed in a Jupyter notebook, `joining_data.ipynb`.

### Part 4: Building a Model

I built a regression model using Python’s statsmodels module, which showcased the relationship between the number of bikes at each station and the characteristics of nearby POIs. I interpreted the results of the model to derive meaningful insights. Furthermore, I spent time conceptualizing how this regression problem could be transformed into a classification problem, outlining potential approaches without coding. The steps taken and insights gained were all documented in the Jupyter notebook `model_building.ipynb`.

Throughout each stage, I made sure to conduct a thorough exploratory analysis of the API documentation and structures and to take steps such as storing authentication tokens securely as environment variables to maintain the integrity and security of the project.

## Results

(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)

## Challenges

(discuss challenges you faced in the project)

## Future Goals

(what would you do if you had more time?)

---

