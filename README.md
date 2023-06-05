# Food-Business-Distribution-NY

Utilizing the power of data visualization, this project aims to convey the message of the influence educational institutes have on the food industry in New York State.

There are two main visualizations in this project. The first one is titled “Food Establishments with respect to universities and tourist places” and the second one is titled “Food establishments types and their ratings”. While the first one is the face of the project, the second one supports the claim by proving that the quality of food produced is, in fact, not unhealthy and hence, exposes the popular myth that “outside food is unhygienic”. As it is further explained in the file Design Document - Neh Majmudar.pdf, we will see with most food establishments being given an ‘A’ grade, it stands to reason that college-going students and professors do not face adverse effects after eating from the food place. This holds a consequence in the reasoning that the more the number of ‘A’ grades, the better the business.

The project in its entirety was implemented in Altair, which is a visualization tool that is built on top of Vega-Lite. Each and every single aspect of both the visuals had a voluntary choice behind them, taking into account the significance it has on the overall theme.

### Datasets used:-

<b>1. Food Inspection Rating:-</b> This dataset was taken from the Open New York data website, [Food Safety Inspections – Current Ratings | State of New York (ny.gov)](https://data.ny.gov/Economic-Development/Food-Safety-Inspections-Current-Ratings/d6dy-3h7r), and later on exported into CSV. This dataset was updated on March 13, 2023. It consists of 13 columns and 183481 rows. We won’t go into much detail about all the columns, however, an explanation of some columns is pivotal to understanding the visuals:-
- <i>County</i> - County of the food establishment
- <i>Inspection Grade</i> - This dataset was created based on the ratings given by the Department of Agriculture and Markets and any food business is given one of the three grades:- A: when the food business doesn’t have any critical deficiency; B: when some deficiencies were found but rectified at the time of inspection; C: when there are critical deficiencies that could not be corrected at the time of inspection.
- <i>Establishment Type</i> - A food establishment can have one, two, or many types depending on the business operations conducted at the geographic location. A: Store; B: Bakery; C: Food Manufacturer; D: Food Warehouse; E: Beverage Plant; F: Feed Mill/Non-Medicated; G: Processing Plant; H: Wholesale Manufacturer; I: Refrigerated Warehouse; K: Vehicle; L: Produce Refrigerated Warehouse; N: Wholesale Produce Packer; O: Produce Grower/Packer/Broker, Storage; P: Controlled Atmosphere Room; Q: Feed Mill/Medicated; R: Pet Food Manufacturer; S: Feed Warehouse and/or Distributor; T: Disposal Plant; V: Slaughterhouse; W: Farm Winery. It is important to note that the primary focus was to display food businesses that were manufacturing food, C.
- <i>Trade Name</i> - The name of the food business.
- <i>Georeference</i> - The geographical location of the establishment.

<b>2. Educational institutions:-</b> This dataset consisted of the name of the college, along with their geographical coordinates. This dataset did not have the latitudes and longitudes of the places but had to be extrapolated by an external Python library called GeoPy. There were a total of 196 universities, extracted from the website [New York Universities and Colleges](https://college.ai/Colleges/New-York-Colleges.html).

<b>3. Tourist places:-</b> The dataset of the 15 most famous tourist destinations across the New York state, and its geographical coordinates.

<b>4. New York State geographical specifications(topoJSON):-</b> In order to create a geospatial representation with any visualization tool, we need a JSON file that encodes the topology of the structure. From here, we can plot the state of New York, and also, get the coordinates of counties, that would be visualized by encoding the geoshape. The data in https://raw.githubusercontent.com/deldersveld/topojson/master/countries/us-states/NY-36-new-york-counties.json was used. From this data, the centroids of each county were calculated, which would be used to label the county names.

### Files info:-
- Project notebook.ipynb:- Source code that outputs and saves the visuals, from the datasets described above.
- Design Document - Neh Majmudar.pdf:- The design document of this entire visualization project that illustrates the choices made for creating the visuals, along with the design specifications, visual encodings, and interactivity employed.
