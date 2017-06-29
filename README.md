# geojson-web-viewer

This is a tiny web page template for displaying GeoJSON paths in a mobile browser.

### Why?

I use [geojson.io](http://geojson.io) to draw and update maps of hiking routes, places I've walked, and areas to explore. I often store them as [GitHub gists](https://gist.github.com), but it's hard to look at the maps when you're on the go. This mobile web viewer changes that!

### What does it do?

`index.html` loads a raw geojson file from the web and displays it on top of a [Mapbox base map](https://www.mapbox.com/mapbox-gl-js/api/). That's about it. You can pan, zoom, etc. 

https://smmaurer.github.io/geojson-web-viewer

For now it's hard-coded to a particular file of mine. Feel free to fork this repository and edit the code to host your own map. 

Coming soon:
- zoom to bounds of geojson file
- an indication of your current location
- dialog box to load an arbitrary geojson file