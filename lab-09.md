# Lab 09: Interactive web mapping with multiple layers

**Mapping Scenario (6pts)**:

A client has recently moved to Denver, CO and wants to buy a home within **1 km of a fire station, a food store, and an after school program**. You've been hired to make an interactive web map allowing the user to click on locations within Denver to see which of these amenities fall within the 1 km range. The map will additionally allow the user to toggle on and off the layers, as well as retrieve specific information about each amenity.

The completed map should look and behave like this:

![Lab 09 Solution](graphics/lab-09-solution.gif)
**Figure 01.** Lab 09 Solution

Begin by opening and editing the *lab-09/index.html* file. You'll notice that a Leaflet map is drawn, centered on Denver, CO. Also, note that there are three data files within the *lab-09/data/* directory (data downloaded from the [Denver Open Data Catalog](https://www.denvergov.org/opendata/)):

* [after-school-programs.js](data/after-school-programs.js)
* [denver-fire-stations.js](data/denver-fire-stations.js)
* [denver-food-stores.js](data/denver-food-stores.js)

You should open these files (Atom or another text editor) to inspect their contents. Note that each contains a GeoJSON structure. Furthermore, each GeoJSONS has been assigned to a JavaScript variable (`programs`, `stations`, and `stores`).

You should begin by loading these files into your *index.html* document. Once the data are loaded into the document, you should begin scripting your solution on line 76.

**Specific map requirements**:

* Map should draw the three GeoJSON datasets as separate layers, each with their own color
* Map should allow the user to toggle off/on each layers with a Leaflet layer control
* Text within the layer control should double as a legend and indicate which color circles symbolize what
* Circles should have a diameter of 10 pixels, no stroke, and a fill opacity level of 1
* When the user clicks on the map, the circles within 1 km of the click point should remain full opacity. All other circles will fade to a fill opacity of .1.
* When the user mouses over an amenity, a tooltip will provide the following information (hint, you'll need to know the property names encoded within the GeoJSON):
    * the station number for fire stations
    * the name of the store for food stores
    * the name of the organization for the after school programs
* Page should have updated title and metadata information

You will use and adapt the code examples presented in Lessons 08 and 09 to complete the map. Commit your work as you go and push to your repository and submit the link within Canvas by the due date.
