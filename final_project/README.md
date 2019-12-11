# Analysis of Brazil's major cities, differences and similarities

This project has the objective to analyze Brazil's State Capitals (27 cities), and using the Foursquare API, compare all cities and find clusters (cities that can be considered similar).

## Problem description

Cities are complex structures, then comparisons can be made by several means. For example, we can define similar cities by their GDP (gross domestic product), or by their HDI (human development index), but these comparisons have a high bias towards economic parameters. Therefore, to have a more "social" analysis of how similar cities are, we will use the Foursquare API, where we can get the information of the most popular venues in each city. Hopefully, this analysis will provide us information of which cities have the most similar structure in terms of popular places, then giving us an interesting point of view of city similarity.

## Methodology

* Gather geospatial information for each 27 capital cities in Brazil
* Create a DataFrame containing information of each city (with columns like: city, region, latitude, longitude)
* Use the Foursquare API to retrieve the 1 000 most popular venues in each city.
* Store the popular venue information in a DataFrame.
* One-hot encode the popular venue DataFrame, allowing numerical analysis to be made.
* Use K-means, with different number of clusters (3, 5, 8) and analyze which cluster parameters have the best metric (i.e. silhouette)
* Create a iterative map (using folium), showing the best calculated cluster analysis.
