# protopro2
this portofolio pro 2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Map</title>
    <style>
        #map {
            height: 400px;
            width: 100%;
        }
    </style>
</head>
<body>

<div id="map"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>
    // Initialize the map
    var mymap = L.map('map').setView([51.505, -0.09], 13);

    // Add a tile layer to the map (using OpenStreetMap)
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; OpenStreetMap contributors'
    }).addTo(mymap);

    // Add a marker to the map
    var marker = L.marker([51.5, -0.09]).addTo(mymap);

    // Add a popup to the marker
    marker.bindPopup("<b>Hello world!</b><br>This is an interactive map.").openPopup();
</script>

</body>
</html>
