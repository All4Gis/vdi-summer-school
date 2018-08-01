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

LROC NAC over Apollo 17 landing sites

```
http://lroc.sese.asu.edu/data/LRO-L-LROC-3-CDR-V1.0/LROLRC_1011/DATA/SCI/2012147/NAC/M192703697RC.IMG
http://lroc.sese.asu.edu/data/LRO-L-LROC-3-CDR-V1.0/LROLRC_1007/DATA/SCI/2011158/NAC/M162107606LC.IMG
```

### Mercury

list of EDR

#### MESSENGER MDIS-NAC CDRNAC - Narrow-angle Calibrated Data Record####

```
http://pdsimage.wr.usgs.gov/data/mess-e_v_h-mdis-4-cdr-caldata-v1.0/MSGRMDS_2001/CDR/2008_280/CN0131773932M_IF_5.IMG
http://pdsimage.wr.usgs.gov/data/mess-e_v_h-mdis-4-cdr-caldata-v1.0/MSGRMDS_2001/CDR/2008_280/CN0131773984M_IF_5.IMG
http://pdsimage.wr.usgs.gov/data/mess-e_v_h-mdis-4-cdr-caldata-v1.0/MSGRMDS_2001/CDR/2008_280/CN0131774854M_IF_5.IMG
http://pdsimage.wr.usgs.gov/data/mess-e_v_h-mdis-4-cdr-caldata-v1.0/MSGRMDS_2001/CDR/2008_280/CN0131774859M_IF_5.IMG
http://pdsimage.wr.usgs.gov/data/mess-e_v_h-mdis-4-cdr-caldata-v1.0/MSGRMDS_2001/CDR/2008_280/CN0131774905M_IF_5.IMG
http://pdsimage.wr.usgs.gov/data/mess-e_v_h-mdis-4-cdr-caldata-v1.0/MSGRMDS_2001/CDR/2008_280/CN0131785976M_IF_5.IMG
```

---
---
---
---
