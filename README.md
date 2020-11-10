## Dataset of vegetation fire events (polygons) in northwest Yunnan from 1987 to 2018 - NWY_Fire_LS

Link to dataset: `NWY_Fire_LS.zip` [[file]](NWY_Fire_LS.zip)
The dataset is in OGC GeoPackage format (.gpkg) and the size is 44,896 KB. You will find it here in zipped format (6,076 KB).

#### Attribute table field description
The attribute table contains 4 fields:
- <ins>fid</ins>: an automatically created ID number
- <ins>area</ins>: the size of the burned polygon in square meters
- <ins>PathRow</ins>: WRS-2 Path and Row of the Landsat series from which the fire event (polygon) has been extracted
- <ins>Year</ins>: year of the burn. Note that the dates of the reference image pair from which the fire events have been detected may vary according to Path/Row and Year. For the exact dates of the Landsat images in the time-series, check this table: `NWY_Fire_LS_timeseries_dates.csv` [[file]](NWY_Fire_LS_timeseries_dates.csv)

This dataset has been produced using a methodology specifically designed to overcome common issues encountered in remote sensing applications in complex landscapes. It is applied burned are extraction. The difficulties tackeld are:

- Small fires
- Rugged terrain
- Frequent cloud coverage
- Patchy vegetation
- Fast post-fire reovery
- No training data


#### Publication
Details on the methodoly in the following publication:
Fornacca D, Ren G, Xiao W (2020) Small fires, frequent clouds, rugged terrain and no training data: a methodology to reconstruct fire history in complex landscapes. _International Journal of Wildland Fire_. https://doi.org/10.1071/WF20072
