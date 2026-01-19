# API

## Project Overview

This project uses the Yelp Fusion API to analyze milk tea shops in San Gabriel, California. The goal is to combine API data retrieval, data transformation, exploratory analysis, and visualization to uncover insights about ratings, reviews, pricing tiers, and geographic distribution.

The analysis is performed in Python (Google Colab) use pandas, matplotlib/seaborn, and folium.

## Data Collection

Queried the Yelp API to retrieve all milk tea shops within the San Gabriel, CA area

Extracted business information including:

  - Name
  - Rating
  - Review count
  - Price level
  - Latitude & longitude

Loaded the results into a pandas DataFrame for analysis
## Analysis

Identified the top 10 milk tea shops based on:

  - Rating
  - Review count
  - A weighted score using logarithmic scaling
    (score = rating × log1p(review_count))

Applied log transformation to review counts to reduce skewness and improve comparison

Created a price tier mapping:

  - Low
  - Medium
  - High
  - Missing values filled as "Unknown"

## Visualizations

- Scatter plots
  - Review count vs. rating (original scale)
  - Review count vs. rating (log-transformed scale)
- Bar chart
  - Average rating by price tier
- Box plot
  - Price distribution by price tier
- Scatter plot
  - Price level vs. rating for overall comparison
- Interactive map (Folium)
  - Visualizes all milk tea shop locations in San Gabriel
  - Color-coded by price tier
  - Movable and zoomable for geographic exploration

## Key Insights

- Log-scaled review counts provide a more balanced comparison between popular and less-reviewed shops
- Higher-priced shops do not always correspond to higher ratings
- Most milk tea shops fall within the low to medium price tiers
- Geographic clustering highlights popular commercial areas in San Gabriel

## Tools & Technologies

  - Python
  - Yelp Fusion API
  - pandas, numpy
  - matplotlib, seaborn
  - folium
  - Google Colab

## Core Business Question
  “Where should I open a new milk tea shop in San Gabriel to maximize success?”
### Business Objective
  Identify geographic gaps and price–quality opportunities where customer demand exists but competition or saturation is lower.
