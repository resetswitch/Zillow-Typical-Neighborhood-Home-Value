# Zillow-Typical-Neighborhood-Home-Value

## Overview

To visualize neighborhood typical home values from across the US over time (dataset courtesy of Zillow). The visualization is done via Plotly-Dash on my website : http://www.chase-g.com/portfolio-Zillow.

## Process

Download the csv from https://www.zillow.com/research/data/ using:
- Data Type: ZHVI Single-Family Homes Time Series
- Geography: Neighborhood

Call the Google API for each location to retrieve latitude and longitude. 16096 locations as of writing this.
```py
    place = '{}, {}, {}, USA'.format(row['RegionName'], row['City'],row['State'])
    try:
        location = GoogleV3(api_key=API_KEY).geocode(place)
```
For more information see the `.ipynb` file.
