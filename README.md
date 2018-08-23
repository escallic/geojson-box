# geojson-box
Collect GeoJSON features that lie inside a boundary coordinate box

This Node command takes a file with a geographically dispersed feature collection as its input. Of those features, it filters out the ones contained by the square neighborhood near the coordinate specified. Large database files [like these ones from Microsoft](https://github.com/Microsoft/USBuildingFootprints) won't load in certain GIS applications like [iD](https://github.com/openstreetmap/iD), but they can be made smaller in size by omitting features from the invisible portion of its window.

Example:
$ `./geojson --latitude 34.43914 --longitude -119.90258 -p 0.01 -o out1.geojson -i California.geojson`

In OSM, the smaller buildings file can be uploaded and rendered as a GPS trace.
![Before](https://screenshotscdn.firefoxusercontent.com/images/eb47f10b-f1d2-42a4-a3e8-90678cffd55d.png)
![After](https://screenshotscdn.firefoxusercontent.com/images/42175e53-483e-4fb6-9d0e-1125066b12ee.png)
