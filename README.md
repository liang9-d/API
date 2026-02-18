# API

## Project Overview

This project leverages the Yelp Fusion API to analyze milk tea shops in San Gabriel, California. The goal is to integrate API data retrieval, data transformation, exploratory analysis, and visualization to uncover insights about ratings, reviews, pricing tiers, and geographic distribution.

The analysis is conducted in Python (Google Colab) using pandas for data manipulation, matplotlib and seaborn for visualizations, and folium for interactive maps. SQL is used to determine the ranking of specific stores within a location as well as overall rankings.

Create a Power BI dashboard to present store ratings, locations, and rankings in a clear and interactive format, enabling actionable insights at a glance.

# Non-Technical Report: 






## All stores location graph:
![Descriptive Alt Text](https://github.com/liang9-d/API/blob/main/sgMTMap.jpeg)

# Technical Report: 

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

## Business practice: Core Business Question
  “Where should I open a new milk tea shop in San Gabriel to maximize success?”
### Business Objective
  Identify geographic gaps and price–quality opportunities where customer demand exists but competition or saturation is lower.

 - high competition area:  
   - Pasadena area
   - Santa Anita shops
   - Alhambra main street
   - Las Tunas Drive(from Alhambra main street to Temple City)
   - Vally Boulevard(from South Garifield Avenue to Rosemaead Boulevard) 
  ### Business insight: 
  - Insight: Opening in less-saturated areas near high-demand zones reduces competition and captures unmet customer demand. Pairing a medium-price strategy with strong quality may maximize adoption and success.


## Next Steps and Considerations:
  - Conduct a comparative analysis of rental prices by location to identify the most cost-effective areas
  - Evaluate local population characteristics to assess their impact on market pricing and customer ratings
