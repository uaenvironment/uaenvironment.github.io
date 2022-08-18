# Overview
## Who we are
We are the technical research applications group found within the [Arizona Institute for Resilient Environments and Societies (AIRES)](environment.arizona.edu). We are a group of published technology professionals and students who provide a variety of technical services and collaborations to the [Centers, Institutes and Programs](https://environment.arizona.edu/our-institute/centers-institutes-programs) found within AIRES. Our project collaborations span the globe and make meaningful impacts from the desert southwestern United States, Africa, the Middle East, and places between. AIRES explores and develops solutions with campus and community partners that serve human and natural communities on a global scale by engaging a full array of disciplines, professional schools, international capacity, and entrepreneurial opportunities.

## How we do it
### Development Process
By developing and combining technologies, we incorporate novel technical solutions into new and existing research. Using a collaborative model, versus the typical service model found most in Information Technology, we can better understand project data, the research questions being asked, and provide a higher quality collaboration for the life of a research project. Having that greater understanding has led us to find correlations in data that were not previously realized which have led to new research project ideas and proposals. We collaborate with researchers during the proposal process and can sometimes provide a proof-of-concept application or tool showing what is technically feasible if project funding is awarded. Upon project completion, we aid with the technical writing portions of publications which outline our findings and technical solutions that were implemented.

### Student Support
We rely on student support and participation across all research projects. Student participation ranges from software development, technical hardware implementation, database architecture design and implementation, ML/AI research, and publication writing. To support these efforts, AIRES has established a student research computing working group that primarily meets during the Fall and Spring semesters. This working group is a forum where we discuss new research technologies, ask questions, and where students can report on their current research activities. The intention is to create research focussed critical thinking processes that can generate new ideas and concepts across various projects and collaborations.

<br />

# Projects

### **Carbon-Econ Plotter**
Methane emissions have an outsized impact on climate, and are increasingly receiving attention from policymakers and the scientific community. We map methane plume emission rates measured by [Carbon Mapper](carbonmapper.org) onto tract-level demographics from the U.S. Census Bureau to explore environmental justice issues associated with the methane emissions. Carbon Mapper collects methane emission data through their airborne pilot projects with advanced remote sensing technology. Census tract-level demographics are obtained from the 2009-2012 five-year moving average [American Community Survey](https://www.census.gov/programs-surveys/acs).

![Carbon Plotter Map Image](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/carbonplotter.png?raw=true)

<br />

### **LoRaWAN Remote Sensing Network**
LoRaWAN is a Low Power Wide Area Networking (LPWAN) open communications protocol used in a variety of remote sensing and Internet of Things (IoT) applications. AIRES supports the [Desert Laboratory on Tumamoc Hill](https://tumamoc.arizona.edu/) which is an 860-acre preserve located west of downtown Tucson. AIRES has a number of LoRaWAN Gateways and is using Tumamoc as our current testbed for future remote sensing projects.

![Tumamoc LoRaWAN image](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/lorawan_tumamoc.jpg?raw=true)

<br />

### **Monsoon Fantasy Game**
In Monsoon Fantasy, players estimate the total monthly precipitation at each of the five major cities in the U.S. Southwest Monsoon region: Tucson, Phoenix, Flagstaff, Albuquerque, and El Paso. Points are awarded each month depending on the accuracy of the estimate compared to the actual observed rainfall. The goal is to accumulate the most points over the July, August, September period.

| | |
|---|---|
|![Monsoon Game Forecast](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/monsoon-game-forecast.png?raw=true)| ![Monsoon Game Leaderboard](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/monsoon-game-leaderboard.png?raw=true)|
|||

<br />

### **Monsoon Game Scoring Method**
<u>Contributors</u>

<a href="https://github.com/uaenvironment/monsoon-game-scoring-method/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=uaenvironment/monsoon-game-scoring-method" width="150px"/>
</a>

<br />

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6878318.svg)](https://doi.org/10.5281/zenodo.6878318)

This repository contains a description of the scoring system used in the Monsoon Fantasy game and a simulation that was created to compare different scoring methods before the final scoring method was decided upon. The final scoring method takes into account both the risk and accuracy of a players guess. First, a potential maximum points value is determined for a guess. This value is higher the further a guess is from the historical rainfall average. Then, the player gets a percentage of their potential maximum points value depending on how close their guess is to the actual rainfall. Visit our [public GitHub repository](https://github.com/uaenvironment/monsoon-game-scoring-method) for more detailed information.

![Monsoon Game Scoring Graph](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/monsoon_game_scoring.png?raw=true)

<br />

### **Monsoon Post Game Analysis**
When signing up to play Monsoon Fantasy, players had the option to fill out profile questions. These questions asked things such as
- How many monsoon seasons have you experienced while living in the southwest?
- How would you rate your understanding of the monsoon system?
- During monsoon season how often do you consult different types of weather forecasts?

All of the questions were optional and the responses were made anonymous before analysis. This data combined with the users' forecasts and points earned were used in this analysis which will be performed and the end of every monsoon season.

![Monsoon Game Post Analysis](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/monsoon_game_post.png?raw=true)

<br />

### **Monsoon Scraper**
This project centralizes public data from several different flood control district (FCD) networks across the state of Arizona. This data is stored in a cloud based data warehouse and serves as the central data source for a number of monsoon related projects and research. To gather this data we have written a number of applications that run at different intervals dependent on the different FCD network implementations. These applications run on 15 minute to 1 hour intervals. These time intervals are required in order to obtain incremental precipitation data readings which are not available if  gathering data on an hour or day interval. In addition to precipitation data, some FCD sensors also report temperature, pressure, humidity, and stream flow intensity in washes.

The result of this work can be found in a Frontiers in Climate publication titled [Curating and Visualizing Dense Networks of Monsoon Precipitation Data: Integrating Computer Science Into Forward Looking Climate Services Development](https://www.frontiersin.org/articles/10.3389/fclim.2021.602573/full).

<br />

### **Monsoon Plotter**
Monsoon Plotter is used to visually represent the data gathered via the Monsoon Scraper project which collects data from the state of Arizona flood control district (FCD) remote sensing networks. There are a handful of networks that can be plotted and more will be added as we expand our Monsoon Scraper project to gather more data. There is also a limited CSV export feature available of the specific data points chosen to be plotted. For full exports of data an API key is required to make programmatic calls to the Monsoon API.

![Monsoon Plotter](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/monsoon_plotter.png?raw=true)

<br />

### **Monsoon API Package/CLI Tool**
This Python package serves as a wrapper to simplify REST API calls to the monsoon scraper data warehouse. This is the same dataset that is visually represented in our monsoon plotter found at [monsoon.environment.arizona.edu](https://monsoon.environment.arizona.edu). The plotter allows a limited export of the data dependent on the date range and sensor network being plotted. This package allows you to incorporate our monsoon dataset into a local codebase for processing. The dataset consist of the following remote sensing precipitation networks along with their programmatic names:

- Pima County FCD - pima_fcd
- Maricopa County FCD - maricopa_fcd
- RainLog.org - rainlog
- MesoWest - mesowest
- Mohave County FCD - mohave_fcd (data beginning 2021)

Data from the networks above are updated at different frequencies and in some cases multiple times per day or hour. This is variable across networks based on their configuration and if precipitation sensors are experiencing rainfall.

There is also a command line interface (CLI) tool available for those who prefer to work within a CLI instead of the Python package.

Currently, API keys are only issued to researchers working with this dataset. There are plans to expand this audience.

<br />

### **Monsoon Machine Learning**
This repository contains code in R and Python that demonstrates how to create basic machine learning algorithms. It then takes historical weather data from the Tucson International Airport, precipitation data from our Monsoon API, and storm data from NOAA and applies these machine learning algorithms in an attempt to accurately predict flooding using historic data and a database of notable flood and rainfall events. 

![Monsoon Machine Learning](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/gradientBoosting.png?raw=true)

<br />

### **Regenerate Lebanon**
This project stemmed from a UN funding award through the Japanese Embassy to provide a mapping service of recycle centers across Lebanon. The project then branched out to include sustainable businesses and other environmentally friendly organizations.

This was a collaboration between a technology company in Lebanon called Imperium Code and other Lebanon non-profits. Our role in the overall project was to provide the mapping solution for the data set. This included mapping the points, portraying their categorizations, as well as implementing a tooltip/popup to display information about each data point. This work can be found on the [Regenerate Hub](https://regeneratehub.org) site.

![Regenerate Lebanon Map](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/regenerate_lebanon.png?raw=true)

<br />

### **Jamaica Coffee Leaf Rust**
This was a proof-of-concept application that was built using Google's Vision AI to detect Coffee Leaf Rust which is a fungus that disseminates coffee plant crop fields. The idea was to detect this fungus via photos taken by farmers in Jamaica. We would then process those photos through the Vision AI algorithm we created to return the probability of positive coffee rust detection. In turn, this would help government officials to focus remediation efforts.

We developed this proof-of-concept model using plant life located in UArizona's ENR2 building. We trained this model by feeding it various images of different plant life to show how the image analysis would function and the different probability results.

<br />

### **Project Visualizations**
This project was developed for the [Agnese Nelms Haury Program in Environment and Social Justice](https://haury.arizona.edu) proposal submission process for research funding. The idea was to use models and algorithms in Natural Language Processing (NLP) to find similarities or potential collaboration opportunities across proposal submission abstracts. We incorporated a number of models/algorithms in this process to determine which is best suited for the particular set of research themes.

![Project Visualization Graphic](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/proj_visualizer.png?raw=true)

<br />

### **Zambia Invasive Species Tracking**
This invasive species tracking application was designed to plot the detection of the Fall Army Worm (FAW) across farms in Zambia. The result of which would help governmental agriculture decision makers in focussing remediation efforts of FAW. To achieve this we worked with data aggregated via analog phone text messaging that was collected by an company in Africa called TextIt. We were not able to successfully work with their API but we were able to export data in a format that allowed us to store responses in a relational way to more easily work with this data. This data was gathered every 2 weeks during their grow season and plotted via the text campaign date. More information about this project can be found on our [FAW environment](http://faw.environment.arizona.edu) site.

![Zambia FAW Distribution](https://github.com/uaenvironment/uaenvironment.github.io/blob/master/images/zambia_faw.png?raw=true)

<br />

# Publications
Guido Z, McMahan B, Hoy D, Larsen C, Delgado B, Granillo RL III and Crimmins MA (2022) Public Engagement on Weather and Climate with a Monsoon Forecasting Game. Bulletin of the American Meteorological Society (IN REVIEW)

Dharma Hoy, Calvin Larsen, Rey Granillo III, UA's Arizona Institute for Resilient Environments and Societies. (2022). uaenvironment/monsoon-game-scoring-method: v1.0.1 (v1.0.1). Zenodo. https://doi.org/10.5281/zenodo.6878318

McMahan B, Granillo RL III, Delgado B, Herrera M and Crimmins MA (2021) [Curating and Visualizing Dense Networks of Monsoon Precipitation Data: Integrating Computer Science Into Forward Looking Climate Services Development](https://www.frontiersin.org/articles/10.3389/fclim.2021.602573/full). Front. Clim. 3:602573. doi: 10.3389/fclim.2021.602573

<br />

# Students
GitHub links / student names