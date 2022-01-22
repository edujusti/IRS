<b>Operational procedures for the production of the roads and structures index.</b>

<p>The OpenStreetMap (OSM) feature set, for a given area, can have a number of vertices greater than the Google Earth Engine (GEE) limit. In this case, simplify lines of streets and roads and eliminate small polygons. In addition, very large areas would need to be subdivided to enable processing.
<p>The features of streets, avenues and roads were converted into a raster file, using line density tool of the ArcGis 10.2. Quantum QGis has a similar tool, but the pixel values are much lower. In this case it would be necessary to adjust thresholds.
<p>Due to the extension of the Brazilian territory, the division by state was necessary.
<p>Landscaped areas, including arboreal vegetation, may occur in the construction vectors area. In land use vectors such as military areas, airports and parks, among others, vegetation and water surfaces can be aggregated.
<p>We import these polygons into Google Earth Engine (GEE) and eliminate surfaces covered by water and vegetation. We use the <i>exportMask</i> and <i>exportBuildingMask</i> scripts.
We group the remaining vectors from the polygons of buildins and land use. To avoid high values in small buildings, we eliminate the features of small area. Later, we convert all vectors to polylines. In ArcGis, we apply the line density function. At end proccess, the rasters and vectors of the remaining buildings and land use were imported to GEE.
