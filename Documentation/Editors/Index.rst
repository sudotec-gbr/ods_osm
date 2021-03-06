Users manual
============

Frontend Plugin
---------------
Insert the Openstreetmap as frontend plugin and define at least one marker to show.
The map will center to the average coordinates of the markers.

.. image:: ../Images/FrontendPlugin.png

+----------------------------+------------------------------------------------+
| Plugin option (TS option)  |                  Description                   |
+============================+================================================+
| Marker to show (marker)    | Show these records on the map.                 |
+----------------------------+------------------------------------------------+
| Cluster markers (cluster)  | Group nearby markers.                          |
+----------------------------+------------------------------------------------+
| Width (width)              | Width of the map in pixels.                    |
+----------------------------+------------------------------------------------+
| Height (height)            | Height of the map in pixels.                   |
+----------------------------+------------------------------------------------+
| Longitude (lon)            | Default longitude.                             |
+----------------------------+------------------------------------------------+
| Latitude (lat)             | Default latitude.                              |
+----------------------------+------------------------------------------------+
| Use this coordinates only  | If unset, the map is always centered at the    |
| if no marker exists        | given coordinates. If set, the map is only     |
| (use_coords_only_nomarker) | centered there if no marker exists.            |
+----------------------------+------------------------------------------------+
| Zoom (zoom)                | Zoom level.                                    |
+----------------------------+------------------------------------------------+
| Library (library)          | Choose between openlayers, leaflet or static.  |
+----------------------------+------------------------------------------------+
| Base layer (layer)         | Show this map. The user can switch between     |
|                            | these base layers if the layerswitcher is      |
|                            | is enabled.                                    |
+----------------------------+------------------------------------------------+
| Show popups (show_popups)  | Show a popup window with record information if |
|                            | the user hover or click a marker.              |
+----------------------------+------------------------------------------------+
| Show this marker's popup   | Open this marker's popup if the user visit the |
| initially                  | map.                                           |
| (marker_popup_initial)     |                                                |
+----------------------------+------------------------------------------------+
| Mouse navigation           | Allow navigation with the mouse.               |
| (mouse_navigation)         |                                                |
+----------------------------+------------------------------------------------+
| Show pan/zoom              | Show pan/zoom element.                         |
| (show_pan_zoom)            |                                                |
+----------------------------+------------------------------------------------+
| Show layerswitcher         | Show layerswitcher which allows the user to    |
| (show_layerswitcher)       | hide markers from the same group.              |
+----------------------------+------------------------------------------------+
| Show scalebar              | Show pan/zoom element.                         |
| (show_scalebar)            |                                                |
+----------------------------+------------------------------------------------+
| Show current position      | Center the map on the current position of the  |
| (position)                 | user (if available)                            |
+----------------------------+------------------------------------------------+

New elements
------------

Layer
.....

You can define your own layers on root level.

.. image:: ../Images/Layer.png

+----------------------------+------------------------------------------------+
|       Element option       |                  Description                   |
+----------------------------+------------------------------------------------+
| Title                      | Title of this layer. Shown in layerswitcher.   |
+----------------------------+------------------------------------------------+
| Is overlay                 | Base layer or overlay layer?                   |
+----------------------------+------------------------------------------------+
| JavaScript                 || JavaScript part to create this layer.         |
|                            || ###TITLE###: Title of layer.                  |
|                            || ###VISIBLE###: Contains “'visible':true” if   |
|                            | is overlay and no layerswitcher activated.     |
+----------------------------+------------------------------------------------+
| Include static JavaScript  || Optionally include this javascript file.      |
|                            || ###STATIC_SCRIPT###: Value set by TS          |
+----------------------------+------------------------------------------------+
| Static map URL             || Download static map from this URL.            |
|                            || ###lat###: Latitude of map center.            |
|                            || ###lon###: Longitude of map center.           |
|                            || ###zoom###: Zoom level.                       |
|                            || ###width###: Image width.                     |
|                            || ###height###: Image height.                   |
+----------------------------+------------------------------------------------+
| Tile URL                   | URL to fetch tiles.                            |
|                            | Used by OpenLayers if no JavaScript defined.   |
|                            | Used by leaflet.                               |
+----------------------------+------------------------------------------------+
| Maximum zoom               | Maximum zoom level of this layer.              |
+----------------------------+------------------------------------------------+
| Subdomains                 | Tile URL subdomains (Variable {s})             |
+----------------------------+------------------------------------------------+
| Attribution                | Attribution text of this layer.                |
+----------------------------+------------------------------------------------+
| Homepage                   | Homepage URL of this layer.                    |
+----------------------------+------------------------------------------------+

Marker
......

.. image:: ../Images/Marker.png

+----------------------------+------------------------------------------------+
|       Element option       |                  Description                   |
+----------------------------+------------------------------------------------+
| Title                      | Title for this track. Only shown in backend.   |
+----------------------------+------------------------------------------------+
| Icon                       | Icon file.                                     |
+----------------------------+------------------------------------------------+
| Size                       | The size of the icon. Would determined         |
|                            | automatically on save.                         |
+----------------------------+------------------------------------------------+
| Offset                     | The offset of the icon. It describes the       |
|                            | arrowhead. Would automatically choose the      |
|                            | middle bottom of the image.                    |
+----------------------------+------------------------------------------------+

Track
.....

.. image:: ../Images/Track.png

+----------------------------+------------------------------------------------+
|       Element option       |                  Description                   |
+----------------------------+------------------------------------------------+
| Title                      | Title for this track. Shown in layerswitcher.  |
+----------------------------+------------------------------------------------+
| Color                      | Color of the track line in the map.            |
+----------------------------+------------------------------------------------+
| Width                      | Width of the track line.                       |
+----------------------------+------------------------------------------------+
| File                       | Select only one gpx file here.                 |
+----------------------------+------------------------------------------------+

Extended elements
-----------------

Website user
............

.. image:: ../Images/Coordinates.png

+----------------------------+------------------------------------------------+
|       Element option       |                  Description                   |
+----------------------------+------------------------------------------------+
| Longitude and Latitude     | Enter the coordinates of an address here. It   |
|                            | would determined automatically if zip or city  |
|                            | is set and autocompletion is enabled in the    |
|                            | extension manager.                             |
|                            | Use the OpenStreetMap icon to search the       |
|                            | coordinates on the map.                        |
+----------------------------+------------------------------------------------+

Website usergroup
.................

.. image:: ../Images/Icon.png

+----------------------------+------------------------------------------------+
|       Element option       |                   Description                  |
+----------------------------+------------------------------------------------+
| Marker                     | Optionally specify a marker here.              |
+----------------------------+------------------------------------------------+
