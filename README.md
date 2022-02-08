<b>Operational procedures to produce the roads and structures index.</b>

<p>The OpenStreetMap (OSM) feature set, for a given area, can have a number of vertices greater than the Google Earth Engine (GEE) limit. In this case, it is necessary to simplify the lines of streets and roads and eliminate small polygons. In addition, very large areas would need to be subdivided to enable processing. In our study, the division by state was necessary due to the size of Brazil.

<p>The features of streets, avenues and roads were converted into a raster file using the ArcGIS 10.2 line-density tool. Quantum GIS has a similar tool, but the pixel values are much lower. In this case, it would be necessary to adjust the thresholds.

<p>Landscaped areas, including arboreal vegetation, may occur in the vectors of buildings area. In land-use vectors such as military areas, airports, and parks, vegetation and water surfaces can be aggregated.
  
<p>We imported those polygons into Google Earth Engine (GEE) and eliminated surfaces covered by water and vegetation. In these procedures, exportLandUseMask and exportBuildingMask scripts were used.
  
<p>We aggregated the remaining vectors from the polygons of buildings and land uses. To avoid high values for small buildings, we eliminated the features of small areas. Later, we converted all vectors to polylines. In ArcGIS, we applied the line-density function. At the end of process, the rasters and vectors of the remaining buildings and land uses were imported to GEE.
  
<p>The rsiSentinel script groups vectors and raster files to make up the roads and structures index. In addition, it maps urban surfaces not covered by water or vegetation, displays the confusion matrix and calculates the quantitative of areas per municipality in decameters.

<p><b>Data availability</b>
  <ul>
    <li><b>Brazilian municipalities</b>: https://www.ibge.gov.br/geociencias/downloads-geociencias.html</li>
    <li><b>OpenStreetMap</b>: https://download.geofabrik.de/south-america/brazil.html</li>
    <li><b>Scripts in the Google Earth Engine (GEE)</b>: https://code.earthengine.google.com/?accept_repo=users/ejustiniano/IRS</li>
  </ul>
