## Planetary data downloads

### Mars

#### CTX

* 99M [ D21_035563_1987_XN_18N282W.IMG](http://pds-imaging.jpl.nasa.gov/data/mro/mars_reconnaissance_orbiter/ctx/mrox_2008/data/D21_035563_1987_XN_18N282W.IMG)
* 49M[F04_037396_1985_XN_18N282W.IMG](http://pds-imaging.jpl.nasa.gov/data/mro/mars_reconnaissance_orbiter/ctx/mrox_2213/data/F04_037396_1985_XN_18N282W.IMG)
* 79M[P19_008650_1987_XI_18N282W.IMG](http://pds-imaging.jpl.nasa.gov/data/mro/mars_reconnaissance_orbiter/ctx/mrox_0589/data/P19_008650_1987_XI_18N282W.IMG)

#### HRSC

* H0988_0000
  * [H0988_0000_BL4.IMG - blue](http://pds-geosciences.wustl.edu/mex/mex-m-hrsc-5-refdr-dtm-v1/mexhrs_2001/data/0988/h0988_0000_bl4.img)
  * [H0988_0000_BL4.IMG - green](http://pds-geosciences.wustl.edu/mex/mex-m-hrsc-5-refdr-dtm-v1/mexhrs_2001/data/0988/h0988_0000_gr4.img)
  * [H0988_0000_RE4.IMG - red](http://pds-geosciences.wustl.edu/mex/mex-m-hrsc-5-refdr-dtm-v1/mexhrs_2001/data/0988/h0988_0000_re4.img)
  * [H0988_0000_ND4.IMG - nadir  - panchromatic](http://pds-geosciences.wustl.edu/mex/mex-m-hrsc-5-refdr-dtm-v1/mexhrs_2001/data/0988/h0988_0000_nd4.img)
  * [H0988_0000_DA4.IMG - topography  - areoid](http://pds-geosciences.wustl.edu/mex/mex-m-hrsc-5-refdr-dtm-v1/mexhrs_2001/data/0988/h0988_0000_da4.img)

## Coordinate Reference System (CRS)

### Mars CRS

example:

```
Group = Mapping
    ProjectionName     = EQUIRECTANGULAR
    CenterLongitude    = 0.0
    CenterLatitude     = 0.0
    TargetName         = Mars
    EquatorialRadius   = 3396190.0 <meters>
    PolarRadius        = 3396190.0 <meters>
    LatitudeType       = Planetocentric
    LongitudeDirection = PositiveEast
    LongitudeDomain    = 180
  End_Group
```

### Moon CRS

example:

```
Group = Mapping
    ProjectionName     = Equirectangular
    CenterLongitude    = 0.0
    TargetName         = Moon
    EquatorialRadius   = 1737400.0 <meters>
    PolarRadius        = 1737400.0 <meters>
    LatitudeType       = Planetocentric
    LongitudeDirection = PositiveEast
    LongitudeDomain    = 180
    PixelResolution    = 1 <meters/pixel>
    CenterLatitude     = 0.0 <DEG>
End_Group
```

### Mercury CRS

example:

```
Group = Mapping
    ProjectionName     = EQUIRECTANGULAR
    CenterLongitude    = 0.0
    CenterLatitude     = 0.0
    TargetName         = Mercury
    EquatorialRadius   = 2440000.0 <meters>
    PolarRadius        = 2440000.0 <meters>
    LatitudeType       = Planetocentric
    LongitudeDirection = PositiveEast
    LongitudeDomain    = 180
End_Group
```

### Moon (LROC exemplary)

#### LROC NAC over Apollo 17 landing sites

```
http://pdsimage.wr.usgs.gov/Missions/Lunar_Reconnaissance_Orbiter/LROC/EDR/LROLRC_0001/DATA/COM/2009192/NAC/M101949648LE.IMG
http://pdsimage.wr.usgs.gov/Missions/Lunar_Reconnaissance_Orbiter/LROC/EDR/LROLRC_0001/DATA/COM/2009192/NAC/M101956806LE.IMG
http://pdsimage.wr.usgs.gov/Missions/Lunar_Reconnaissance_Orbiter/LROC/EDR/LROLRC_0003/DATA/MAP/2010141/NAC/M129086118LE.IMG
http://pdsimage.wr.usgs.gov/Missions/Lunar_Reconnaissance_Orbiter/LROC/EDR/LROLRC_0001/DATA/MAP/2009356/NAC/M116113215LE.IMG
```

data have been processed with isis3 to level2 (i.e. map-projected)


### Mercury

list of EDR:

#### MESSENGER MDIS-NAC CDRNAC - Narrow-angle Calibrated Data Record####

```
http://pdsimage.wr.usgs.gov/Missions/MESSENGER/MSGRMDS_1001/DATA/2008_014/EN0108828332M.IMG
http://pdsimage.wr.usgs.gov/Missions/MESSENGER/MSGRMDS_1001/DATA/2008_014/EN0108828384M.IMG
http://pdsimage.wr.usgs.gov/Missions/MESSENGER/MSGRMDS_1001/DATA/2008_014/EN0108828436M.IMG
http://pdsimage.wr.usgs.gov/Missions/MESSENGER/MSGRMDS_1001/DATA/2008_014/EN0108828488M.IMG
http://pdsimage.wr.usgs.gov/Missions/MESSENGER/MSGRMDS_1001/DATA/2008_014/EN0108829085M.IMG
http://pdsimage.wr.usgs.gov/Missions/MESSENGER/MSGRMDS_1001/DATA/2008_014/EN0108830179M.IMG
```
data have been processed with isis3 to level2 (i.e. map-projected)
