<b>Operational procedures for the production of the roads and structures index.</b>

<p>The OpenStreetMap (OSM) feature set, for a given area, can have a number of vertices greater than the Google Earth Engine (GEE) limit. In this case, it is necessary simplify lines of streets and roads and eliminate small polygons. In addition, very large areas would need to be subdivided to enable processing.

<p>The features of streets, avenues and roads were converted into a raster file, using line density tool of the ArcGis 10.2. Quantum Gis has a similar tool, but the pixel values are much lower. In this case it would be necessary to adjust thresholds.

<p>Landscaped areas, including arboreal vegetation, may occur in the construction vectors area. In land use vectors such as military areas, airports and parks, among others, vegetation and water surfaces can be aggregated.

<p>We have imported those polygons into Google Earth Engine (GEE) and have eliminated surfaces covered by water and vegetation. In this procedures, <i>exportMask</i> and <i>exportBuildingMask</i> scripts were used.

<p>We have grouped the remaining vectors from the polygons of buildings and land use. To avoid high values in small buildings, we eliminated the features of small areas. Later, we converted all vectors to polylines. In ArcGis, we applied the line density function. At the end of process, the rasters and vectors of the remaining buildings and land use were imported to GEE.

<p>The <i>rsiSentinel<i> script groups vectors and raster files and makes up the roads and structures index. In addition, it performs a mapping of urban surfaces not covered by water and vegetation, displays the confusion matrix and calculates the quantitative of areas per municipality in dekameters.

<p>Due to the extension of Brazilian territory, the division by state was necessary.
