#--------------
Migros branch optimisation exercise
#---------------
This project uses ML and GàIS data to identify optimal location for Migros Supermarkets in the Canton of Zurich (Switzerland)

Made by dr Matteo Jucker Riva, data scientist and location specialist, matteo.jriva@gmail.com

*Disclaimer: I have no affiliation with Migros and this analysis was not requested by Migros AG. All the data used is publicly available*

## Introduction

Location intelligence  is the process of deriving meaningful insight from geospatial data relationships to solve a particular business problem.

This projects addresses a particular problem for retail stores, called _"Branch Network optimisation"_. In this type of analysis, geospatial data are used to determine optimal location for retail branches in order to improve spatial coverage and fill gaps in the branch network. 

Here we will try to identify geospatial features that drive the loication of Migros Supermarket locations within the canton of Zurich, and feed this information to a machine learning model in order to identify additional promising locations for addtional branches


##0 Input Data

List of existing Migros branches was downloaded from :https://filialen.migros.ch/

The following additional data was used to define geospatial relationships (predictors of supermarket locations):
- Main urban and suburban roads (vector format, source:http://maps.zh.ch/ )
- Location of bus stops (vector format, source: https://www.openstreetmap.org )
- Location of train stations (vector format, source:https://www.openstreetmap.org )
- Population density per municipality (vector format, source:www.bfs.admin.ch  )
- Location of other supermarkets (source: Google Maps)

##1 Feature engineering

*Point and lines*

Vector data such as the supermarkets or the roads in the maps above are discrete representation of information. As such, the number of operations that can be done on them is limited. To obtain a more useful format, we have to translate the information of the points and lines into a raster grid. This means creating a square grid on top of the area of interest and assigning a value to each square based on the distance from the points of interest. This operation is often called cost/distance analysis where the cost is directly proportional to the euclidean distance from a point p , and 


###### ----- Notes
# Hyperparameters
Raster size: 100 m

# Doubts
-how to translate points to density map?
Heatmap (triangular) vs r.grow.distance

# Other notes
dims utm
451627.1061999999801628,5222689.1189000001177192 : 498627.1061999999801628,5284689.1189000001177192

dims wgs84
8.3576793670654297,47.1594314575195028 : 8.9849405288696307,47.7151947021484020

pixel num
X: 47 Y: 62 

pixelsize wgs84
0.01333616312765957893,-0.009026717870967796223


