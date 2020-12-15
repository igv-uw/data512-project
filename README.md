# Who is being left out by public transport?
**An analysis of accessibility and public transport quality in Santiago, Chile**  

**[Iacopo Garizio](https://iacopogarizio.com), University of Washington**

## Abstract  
The city of Santiago, Chile, is highly segregated in terms of income and its
car usage is unequal across the city, making the need for public transport also
unequally distributed. The objective of this analysis is to discover what parts
of the city are being underserved in terms of public transport. The analysis
uses two different types of metrics (accessibility and quality) to answer this
question. The study shows that in some areas of the city the type of metric 
used can change who is considered to be "left out," however, for the most part,
it shows consistently that the outskirts of the city are the most underserved.

## Data sources
- [Microdatos Censo 2017 (Manzana)](https://geoine-ine-chile.opendata.arcgis.com/datasets/54e0c40680054efaabeb9d53b09e1e7a_0):
  This shapefile contains the number of people who live in each city block. It is licensed under a custom license, which categorizes the dataset as "public use" (license details available in the same link). 
  The data has the following structure:
    
| Field      | type     | Description                         |
|------------|----------|-------------------------------------|
| FID        | int      | Unique identifier of the city block |
| REGION     | str      | Name of the region                  |
| PROVINCIAL | str      | Name of the province                |
| COMUNA     | str      | Name of the county/commune          |
| TOTAL_PERS | int      | Total number of people              |
| geometry   | geometry | Shape of the city block             |
|            |          |                                     |

- [Santiago GTFS data](https://datos.gob.cl/dataset/33245): Dataset with bus stops, routes, times, among many others. This is licensed under Creative Commons Attribution (license details available in the same link).  
    The dataset follows the [standard GTFS structure](https://developers.google.com/transit/gtfs). Here is a summary of the fields used:
    
| File           | Field      | Type      | Description                                                                 |
|----------------|------------|-----------|-----------------------------------------------------------------------------|
| trips.txt      | service_id | int       | Identifies a set of dates when service is available for one or more routes  |
| stop_times.txt | trip_id    | int       | Identifies a trip                                                           |
| stops.txt      | stop_id    | int       | Identifies a stop                                                           |
| stops.txt      | stop_lat   | Latitude  | WGS84 latitude in decimal degrees                                           |
| stops.txt      | stop_lon   | Longitude | WGS84 longitude in decimal degrees                                          |


## License
This repository is licensed under [MIT License](LICENSE)
