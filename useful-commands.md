## useful commands

### visualise  map projection code (proj4)

one can use ```gdalsrsinfo```, e.g.

```
gdalsrsinfo mars.mola.cea.tif

PROJ.4 : +proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=3396190 +b=3396190 +units=m +no_defs

OGC WKT :
PROJCS["unnamed",
    GEOGCS["unnamed ellipse",
        DATUM["unknown",
            SPHEROID["unnamed",3396190,0]],
        PRIMEM["Greenwich",0],
        UNIT["degree",0.0174532925199433]],
    PROJECTION["Cylindrical_Equal_Area"],
    PARAMETER["standard_parallel_1",0],
    PARAMETER["central_meridian",0],
    PARAMETER["false_easting",0],
    PARAMETER["false_northing",0],
    UNIT["metre",1,
        AUTHORITY["EPSG","9001"]]]
```

Mars topography in Cylindrical_Equal_Area projection looks like:

<img src="images/mars-topo-cea.jpg">

### change projection

e.g. from a Cylindrical_Equal_Area to an Equirectangular (can you spot the difference?)

#### Mars case

```
gdalwarp -s_srs "+proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=3396190 +b=3396190 +units=m +no_defs" -t_srs "+proj=eqc +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=3396190 +b=3396190 +units=m +no_defs" mars.mola.cea.tif mars.mola.eqc.tif
```

Mars topography in Equirectangular projection looks like:

<img src="images/mars-topo-eqc.jpg">

#### Moon case

```
gdalwarp -s_srs "+proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=1737400 +b=1737400 +units=m +no_defs" -t_srs "+proj=eqc +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=1737400 +b=1737400 +units=m +no_defs" moon.lola.cea.tif moon.lola.eqc.tif
```

#### Mercury

```
gdalwarp -s_srs "+proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=2439700 +b=2439700 +units=m +no_defs" -t_srs "+proj=eqc +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=2439700 +b=2439700 +units=m +no_defs" mercury.mla.cea.tif mercury.mla.eqc.tif
```

#### Venus case

```
gdalwarp -s_srs "+proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=6051800 +b=6051800 +units=m +no_defs" -t_srs "+proj=eqc +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=6051800 +b=6051800 +units=m +no_defs" venus.magellan.filled.cea.tif venus.magellan.filled.eqc.tif
```

One can change the Mooon topography to something similar to what one would see from Earth

```
gdalwarp -s_srs "+proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=1737400 +b=1737400 +units=m +no_defs" -t_srs "+proj=ortho +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=1737400 +b=1737400 +units=m +no_defs" moon.lola.cea.tif moon.lola.ortho.tif
```

It is a bit easier using imagery rather than topography:


```
gdalwarp -s_srs "+proj=cea +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=1737400 +b=1737400 +units=m +no_defs" -t_srs "+proj=ortho +lon_0=0 +lat_ts=0 +x_0=0 +y_0=0 +a=1737400 +b=1737400 +units=m +no_defs" moon.image.eqc.cub moon.image.ortho.tif
```

i.e.

<img src="images/moon-topo-ortho.png">

or in color

<img src="images/moon-topo-ortho-color.png">

vs.

<img src="images/moon-image-ortho.png">


see e.g. wikipedia entry based on LRO data:

<img src="https://upload.wikimedia.org/wikipedia/commons/c/c9/Moon_nearside_LRO.jpg">

[wikipedia animation of near side of the Moon](https://en.wikipedia.org/wiki/Near_side_of_the_Moon#/media/File:Lunar_libration_with_phase_Oct_2007_450px.gif)

#### Hillshading

```
gdaldem hillshade moon.lola.cea.tif moon.lola.cea.shade.tif
```

produces from:

<img src="images/moon-topo-cea.png">

this:

<img src="images/moon-shade-cea.png">


### mosaic

assuming that all images have the same projection (CRS) and PixelResolution.

e..g done for those images:

* EN0108828332M.lev2.cub
* EN0108828384M.lev2.cub
* EN0108828436M.lev2.cub
* EN0108828488M.lev2.cub
* EN0108829085M.lev2.cub
* EN0108830179M.lev2.cub

<img src="images/mercury-images.png">

the command to mosaic them (provided that they  already have the same map projection, see [gdal_merge](https://www.gdal.org/gdal_merge.html))
```
gdal_merge.py -o mosaic-test-mercury.tif EN0108828332M.lev2.cub EN0108828384M.lev2.cub EN0108828436M.lev2.cub EN0108828488M.lev2.cub EN0108829085M.lev2.cub EN0108830179M.lev2.cub
```

<img src="images/mercury-mosaic.png">