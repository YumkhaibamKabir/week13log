# week13log


Technical Steps


**Dowloading Java for geoserver and downloading geoserver through window installer**
• Firstly, I went to geoserver.org and find the documentation part, in it we have to go user manual and then go the installation and there will find description saying in order to download geoserver you need to have java environment on your device.
• In order to download the java environment, you need to check your device compatibility, so in my case I’m using java version 11.
• I downloaded the java version 11 and installed it to my computer.
• The next thing after installation of java environment, we need to download the geoserver application through zip file or window installer, so in my case I downloaded through window installer and installed the geo server application into my computer successfully.
• Finally, I opened my geoserver with a login id and password for first time.



**Uploading the shapefile to my geoserver**
• Firstly, I opened my geoserver from the start option and then I went to my server ID which is localhost:8080/geoserver.
• I then login to my server and create a new workspace and give my workspace name and the URL and save it.
• Now I’m going to create store for which the shape file will be publish.
• We have to give a name for the data source, in my case since im using shapefile I will give shp and in the connection parameters go to the data directory and chose states shape file.
• Once everything is filled then save and it will pops up description of what you did and hit publish button.
• Now it will pops up a basic resources info, name a title to your layer and click on  compute the data as well as compute on native bound, it will get the file projection and hit save.
• Now go to preview the layer and find your layer through your tittle name and see using openlayers.



**Uploading the shapefile to my geoserver**
• Firstly, in order to style my shapefile, I need to create a new style by clicking the icon of style.
•  Name the data and choose the workspace and in the style content choose whatever the data is but in my case my data are polygon, so I’m going to choose polygon and hIt generate.
• Now it will generate a list of existing code where you can play with your data.
• Now, I Changed the title , the fill color, stoke color, stroke width and then I validate hit apply.
• After the above step, go the layer and find your layer and hit the publishing and in the WMS settings change the default to your saved styled. Finally hit save and apply and go the openlayers to see the magic that you have created.



**Labeling the name of my shapefile in the geoserver**
• I went to my style layer and find my layer and in the publishing, WMS setting there will find a box for the code.
• In order to display the data you want to display you have to see the type of data in my case I want to show the State Name of U.S.A.
• Now I wrote a code for displaying the label which is state name of USA  in the map.
• Codes:
• <TextSymbolizer>
•  <Label>
•<ogc:PropertyName>STATE_NAME</ogc:PropertyName>
•  </Label>
• </TextSymbolizer>




**To create a simple interactive map using Leaflet,  and implement hover effects on markers to display popups**.
• I Created a new HTML file named leaflet.html to contain the map.
• I Included the Leaflet library by adding the necessary <link> and <script> tags in the HTML file from leaflet website.
• And, then added a <div> element with id map to serve as the container for the map.
• Initialized a new Leaflet map object by calling L.map() and passing the id of the map container.
• Set the initial view coordinates and zoom level using setView() method.
• Added a base map layer using L.tileLayer() and specified the URL template for the OpenStreetMap tiles. (leaflet website)
• Created markers for two locations, Taj Mahal and Shah Jahan Garden, using L.marker() and specifying their coordinates.
• Bound popups to the markers using bindPopup() method and provided appropriate content for each popup.
• Added hover effects to the markers to display popups when the mouse enters the marker area and hide them when the mouse leaves.
• Used Leaflet's event handling mechanism with mouseover and mouseout events to achieve this functionality.
• Attached event listeners to each marker using on('mouseover') and on('mouseout') methods.
• Credit: leaflet website




**Publishing arcgis online hosted feature layer into leaflet**
• I Created a basic HTML5 document structure with <html>, <head>, and <body> tags.
• And, included necessary <meta> tags for character set and viewport settings.
• Added a <div> element with the ID ""map"" to serve as the container for the Leaflet map.
• I then linked Esri Leaflet JavaScript file (esri-leaflet.js) to enable integration with ArcGIS Online services.
• Then Initialized a Leaflet map instance (map) with a specific center coordinate [50.434, -104.625] and zoom level 5.
• Added an ArcGIS Online basemap layer using L.esri.basemapLayer('Topographic') and appended it to the map.
• I defined the URL of the ArcGIS Online hosted feature layer (featureLayerUrl) containing seismic data.
• Created a feature layer object (featureLayer) using L.esri.featureLayer() and specified the URL.
• Added the feature layer to the map using .addTo(map) method.
• Lot of things to learn left such as how to add existing legend in the leaflet map.
• How to add web map etc, due to time constraint im not able to execute it.



**Exploring Clustering method in arcgis online**
• I added the earthquake data from Esri living atlas
• Then I styled the symbology and went to aggregation option in arcgis online and choose clustering option.
• And, adjusted the clustering distance to determine the proximity threshold for points to be grouped together into clusters.
• Configured the appearance of clustered symbols.
• Finally, saved the changes made to the layer settings to apply clustering to the map permanently.




