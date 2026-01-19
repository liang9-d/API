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
