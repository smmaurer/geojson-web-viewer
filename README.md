# geojson-web-viewer

This is a tiny web page template for displaying web-hosted GeoJSON files in a mobile browser.

### Why?

I use [geojson.io](http://geojson.io) to draw and update maps of hiking routes, places I've walked, and areas to explore. I often store them as [GitHub gists](https://gist.github.com), but it's hard to look at the maps when you're on the go. This mobile web viewer is an attempt to sovle that.

### What does it do?

`index.html` loads a raw geojson file from the web and displays it on top of a [Mapbox base map](https://www.mapbox.com/mapbox-gl-js/api/). That's about it. You can pan, zoom, etc. 

For now, you have to pass an encoded URL and initial bounding box as query parameters. I'm working on inferring the bounding box, and some other features; check out the "Issues" tab to join the conversation.

URL format: `https://smmaurer.github.io/geojson-web-viewer/?url=<GEOJSON-URL>&bbox=<BOUNDS>`, where `<GEOJSON-URL>` is a [URL-encoded](https://www.urlencoder.org) path to the GeoJSON file and `<BOUNDS>` is a pair of coordinates formatted as `sw-lon,sw-lat,ne-lon,ne-lat`.

Example: https://smmaurer.github.io/geojson-web-viewer/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fgist%2Fsmmaurer%2Feddb484bc73eaed8a8c498589e0627bf%2Fraw%2F72caf5c7c733f21c19ae6f6bd40dd77ab19ca1a4%2Fmap.geojson&bbox=-122.52,37.72,-122.36,37.82

With default Cross-Origin Resource Sharing ([CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS)) access controls in place, the viewer and GeoJSON file must be hosted on related domains. (Github.io and a Github Gist work well.)

(It turns out there's already similar functionality to this built into [geojson.io](http://geojson.io). Click on "Share" to generate a desktop- and mobile-accessible viewing link.)
