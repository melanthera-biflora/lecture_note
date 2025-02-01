# GIS:
* **Geographic information system (GIS)**: a computer system for capturing, storing, querying, analyzing, and displaying geographically referenced data.
* **Geographically referenced data**: data describes both the location and characteristics of spatial features.
### GIS Application:
* Natural resources management including land-use planning, natural hazard accessment, wildlife habitat analysis, v.v..
* Crime analysis
* Emergency planning
* Land records management
* Market analysis
* Transportation application.
### Components of GIS:
GIS requires 4 components:
* **Computer System**: includes computer and operating system.
* **GIS Software**: program and user interface. Ex: menus, graphical icons, and command lines.
* **Brainware**: refers to purpose and objectives, and provide the reason and justification for using GIS.
* **Infrastructure**: necessary physical, orgranizational, administrative, and cultural environments that support GIS operations.
### GIS Brief History:
* Since 1960s computer have been used to store and process geographically referenced data.
* Problem with GIS in early age: difficult, expensive, and proprietary.

**Notes**: Some GIS software producers and their products:
| Producers | Products |
| -------- | ------- |
| ESRI Inc | ArcGIS, ArcView, ArcEditor, ArcInfo |
| Intergraph Corp. | GeoMedia, MGE |
| U.S Army Construction Engineering Research Laboratory | GRASS |
| Microsoft | Microsoft MapPoint |
| Oracle | Oracle Spatial |
| IBM | Spatial DataBlade |

# Geographically Referenced Data:
Including two components: **spatial data** and **attribute data**.
### Spatial Data:
* Describes the locations of spatial features, which may be discrete or continuous.
* **Discrete features**: individually distinguisable features. Ex: points, lines, areas, v.v..
* **Continuous features**: features exist spatially between observations. Ex: elevation, precipitation, v.v..
* **Topology**, as used in GIS, expresses explicitly the spatial relationships between features.
* ESRI uses coverage for topological data and shapefile for nontopological data.
* **Higher-level data**:
        * Triangulated irregular network (TIN): approximates the terrain wwith a set of non-overlapping trianges, is mae of points and edges (lines).
        * Regions data model, which allows regions to overlap and to have spatially disjoint components, is built on lines and polygons.
        * Dynamic segmentation, which combines plane coordinates with linear measures, is built on top of a network.
=> Higher-level data are useful in GIS because they can handle more complex spatial relationships.
* **Object-oriented data model** uses objects to organize spatial data.
### Attribute data:
* Describes the characteristics of spatial features.
* Raster data: each cell has a value that corresponds to the attribute of the spatial feature at that location.
* Vector data: the amount of attribute data to be associated with a spatial feature can vary significantly.
### Join Spatial and Attribute Data:
* **Georelational data model**: GIS packages store attribute data separately from spatial data in a split data system.
        * Spatial data: stored in graphic files
        * Attribute data: stored in tables.
=> Both data are linked through the featured ID.
* Object-oriented  data model stores spatial data as an attribute along with other attribute data in a single table.
* **Relational database**: a collection of tables (relations), with connection made through a key - a common field whose values can uniquely identify a record in a table.
# GIS Operation:
### Spatial data input:
* 2 options for data acquisition: (1) using existing data and (2) create new data.
* New digital spatial data can be created from satellite images, GPS data, field surveys, street addresses, text file with x-, y- coordinates.
* Paper map remain the dominant data sources.
### Attribute data management:
* We must enter, verify, and manage attribute data to complete a GIS database.
* Attribute data entry and verification also involves digitizing and editing.
### Data Display:
* Mapmaking is a routine GIS operation for data visualization, query, analysis and presentation.
* Elements in maps: title, subtitle, body, legend, north arrow, scale, acknowledgment, neatline, and border.
### Data exploration:
* is data-centered query and analysis, allowing user to explore the general trends in the data, to take a close look at data subsets, and to focus on possible relationship between dataset.
### Data analysis:
* Vector:
                            * Map overlay: combines spatial data and attribute data from different maps to create the output.
                            * Map manipulation: perform dissolving, clipping, merging, splitting, erasing, and other task.
                            * Buffering: measures straight-line distances from map features an creates buffer zones.
                            * Distance measurement: measures distances between map features.
* Raster:
                            * Local: involves individual cells.
                            * Neighborhood operation: a specified neighborhood.
                            * Zonal operation: A group of connected cell.
                            * Global operation: an entire grid.
=> Raster operation is computationally more efficient than the vector operation.
* Spatial interpolation: refers to the process of using points with known values to construct a statistical surface => converting point ata into raster data.
### GIS Modeling:
* GIS modeling refers to the use of a GIS and its functionalities in building a moel with geographically referenced ata.

