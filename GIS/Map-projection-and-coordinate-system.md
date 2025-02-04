# Introduction
* GIS users work with map features on a two-dimensional or plane surface.
* Problem:
  * Location of map features: based on a plane coordinate system expressed in x- and y-coordinates.
  * Location of spatial features: based on the geographic coordinate system expressed in longitude and latitude values.  
  => **Projection** transforms the spherical surface of the Earth to a map projection.
* Basic principle: map layers to be used together must have the same coordinate system.
* Projection and Reprojection:
  * *Projection*: converts digital maps from longitude and latitude values to plane coordinates.
  * *Reprojection*: converts from one plane coordinate system to another.  
  => Projection and reprojection is the initial task in a GIS project.

# Geographic Coordinate System:
* **Geographic Coordinate System** is the location reference system for spatial features on Earth's surface, consisting of meridians and parallels.
* **Meridians**:
  * Lines of longitude.
  * Running north and south.
  * Used for measuring location in the E-W direction.
* **Parallels**:
  * Lines of latitude.
  * Running east and west.
  * Used for measuring location in the N-S direction.
* Geographic coordinate system is similar to the plane coordinate system.
* Longitude ≈ *x*
* Latitude ≈ *y*
* Latitude > 0 => north of the equator.
* Latitude < 0 => south of the equator.
* Longitude > 0 => eastern hemisphere.
* Longitude < 0 => western hemisphere.
* Longitude and latitude values may be measured in the degrees-minutes-seconds (DMS) or decimal degree (DD).
# Map Projection:
* **Map projection**: a systematic construction of lines on a plane surface representing the geographic coordinate system.
* Transformation from the Earth's surface to a flat surface always involves distortion and no map projection is perfect.
* Every map projection preserves certain spatial properties while sacrificing other properties.
* 4 class of map projections:
  * Conformal projection: preserves local angles and shapes.
  * Equivalent projection: represents areas in correct relative size.
  * Equidistant projection: maintains consistency of scale along certain lines.
  * Azimuthal projection: retains certain accurate direction.
* Conformal projection and equivalent projection are mutually exclusive, applying to the entire map projection (global properties).
* Equidistant and Azimuthal: local properties and may be true only from or to the center of the map projection.
