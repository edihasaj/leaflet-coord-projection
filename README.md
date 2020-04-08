# Leaflet Coordinates Projection

Show coordinates on mousemove in Leaflet map. Ability to change from different projections (But this requires a proj4leaflet object of projection).


# Demo
<a href="http://edihasaj.github.io/leaflet-coord-projection/">Demo Here</a>


# How to use ?
```
let coordP = L.control.coordProjection({
    crs: kosovarefCrs,
}).addTo(map);

// change projection with:
coordP.changeCrs(crs); // crs is string only if it's leaflet's official projections, otherwise it should be a proj4jsleaflet object.
```

# Options


Options available:

    position: Defaults to 'bottomleft'

    separator: Separate lon\lat values. Defaults to ' | '

    emptystring: Initial text to display. Defaults to ' '

    lngFirst: Longitude first or not. Defaults to false

    numDigits: Number of digits. Defaults to 3

    lngFormatter: Custom function to format the longitude value. Defaults to undefined

    latFormatter: Custom function to format the latitude value. Defaults to undefined

    prefix: Prepended a string to the coordinates. Defaults to the empty string ''

    crs: Projection to see the coordinates, it can be a string for 'EPSG4326, EPSG3857, EPSG3395' or a CRS complex object of proj4leaflet

    projection. Defaults to 'EPSG4326'.
