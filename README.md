# mapzoomer
a number of houdini hdas that allow superzoom to specific coordinates of the map

* map generator:
  
  A simple asset that (ab)uses googlemaps to fetch multiple zoom levels of tiles to some specific location

  Multiple points can be selected by uv or by map coordinates to generate detailed texture for

  You can put in your own geometry to for a map

* map generator texture sampler:

  A vop node will output the map texture sample, should be used to build your proper earth/ground shader

* map generator camera curve

  A simple asset that helps you append a given curve to end up exactly at map's zoom location, and produces proper looking path animation to be used for camera


### Examples:

![imgur](https://i.imgur.com/KQXpRyZ.gif)

![imgur](https://i.imgur.com/XY21yUC.gif)

and a special version for 5p3tial children:

![imgur](https://i.imgur.com/r5OKBHq.gif)

## WARNING !
**OPEN HIP FILES IN MAUNAL MODE !!**

Creating high resolution maps will take potentially a LOT of time and can result in a ban of your IP at google maps for 24 hours... (auto proxies will probably help download maps though, but anyway)

* In examples the point zoom level is set to 20, that is super high, consider changing it to something like 8-9 as a start for tests. 

* Also keep in mind that the zoomsize is stated in **uv** units, so if you accidently set your zoomsize to something like default 0.01 with zoomlevel 20 - that will cause the generation of impossibly huge map texture (about 5000000x5000000 pixels), and will probably just fail due to lack of memory.


See example scene for example. But **BEWARE** for it will start downloading highres maps through proxies, that can take potentially up to 30 min

### TODO:
add less highres examples...
