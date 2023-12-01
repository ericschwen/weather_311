# weather_311
Weather and 311 calls data science case study

This project eplores two public datasets: 311 calls in New York City and NOAA weather reports from across New York state. The main goals are
to explore and characterize these datasets and then build a model to predict daily 311 calls for the next week.

My main aim in completing this project is to show my thought process and methodology in working though this style of project involving
large, messy datasets. The jupyter notebooks in this project therefore include the intermediate steps I took in exploring, analyzing,
and modeling the data.

I had a timeframe of a couple of days to work on this case study, so the data exploration and modeling is largely restricted to
relatively quick analysis. There are a number of locations where I have noted ideas that I would further explore if I were to
work on this project further.

The full datasets used for this project are not included in this repository, but they are publicly available. The 311 call data can be found
at https://nycopendata.socrata.com/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9. The weather data can be found at
https://www.weather.gov (and many other locations using the same public data).

### Project organization

**311_exploration.ipynb** includes my exploratory data analysis for 311 calls in NYC. This exploration produces 311_daily_counts.csv for use in
daily call count modeling.

**weather_exploration.ipynb** includes my exploratory data analysis for the NOAA weather reports. This exploration produces weather_daily_avg.csv
for use in daily call count modeling.

**311_weather_modeling.ipynb** combines the two datasets and builds a linear regression model (with some polynomial terms) to predict
daily call counts for the next week. I chose to use linear regression because it is a powerful tool which produces interpretable models and
interpretability was a key consideration for this demonstration project. An autoregressive model could certainly also make sense for predicting
daily call counts, though it would be more appropriate for shorter timescale predictions and an applicable model would have to be chosen to
include the exogenous weather data.

**weather_311_presentation_final.pdf** is my presentation slides explaining the results of this project.

**311_weather_decision_tree.ipynb** is some exploration into applying a gradient boosting decision tree modeling aproach. I didn't have time to
finish the decision tree modeling, but I may return to it at a later point.
