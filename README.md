### Dataset of vegetation fire events (georeferenced polygons) in northwest Yunnan from 1987 to 2018 - NWY_Fire_LS v1 and v2

Links to datasets:  
- [`NWY_Fire_LS.zip`](NWY_Fire_LS.zip) (6,076 KB, OGC GeoPackage format: 44,896 KB)
- [`NWY_Fire_LS_v2.zip`](NWY_Fire_LS_v2.zip) (6,103 KB, OGC GeoPackage format: 43,340 KB)
 
#### Attribute table field description
The attribute table contains 4 fields:
- <ins>fid</ins>: an automatically created ID number
- <ins>area</ins>: the size of the burned polygon in square meters
- <ins>PathRow</ins>: WRS-2 Path and Row of the Landsat series from which the fire event (polygon) has been extracted
- <ins>Year</ins>: year of the burn. Note that the dates of the reference image pair from which the fire events have been detected may vary according to Path/Row and Year. For the exact dates of the Landsat images in the time-series, check this table: [`NWY_Fire_LS_timeseries_dates.csv`](NWY_Fire_LS_timeseries_dates.csv).  

#### General information
The first version of this dataset (v1) has been produced using a methodology specifically designed to overcome common issues encountered in remote sensing applications in complex landscapes. It is applied to burned area extraction. The difficulties tackeld are:
- Small fires
- Rugged terrain
- Frequent cloud coverage
- Patchy vegetation
- Fast post-fire reovery
- No training data

Burned areas have been detected for the period 1987-2018, using one Landsat scene per year, selected during the (almost) cloud-free winter season. Only images from Landsat TM and OLI sensor have been used. Consequently, there's a 2-year gap between 2010 and 2013. The fires of 2013 may include burns from 2011 and 2012. Only polygong bigger than 62,500 square meters are included.

NWY_Fire_LS accuracy in detecting fire events has been tested using a stratified random sampling scheme. Also, a burned area mapping accuracy has been performed. 
- **Fire events detection (polygon-matching)**: Omission error 20%, Commission error 22%
- **Burned area mapping (pixel-based)**: Omission error 27%, Commission error 13%

#### Identified limitations and caveats
- The accuracy assessment has been performed for the period 2001-2018, excluding 2011, 2012, and 2013. Previous years' accuracies were not assessed
- Because of the gap between 2010 and 2013, fires of the year 2013 may include burns from 2011 and 2012. 

#### Improvements of the second version (v2)
A quick manual (visual) check of the entire dataset, year-by-year in each WRS-2 tile, has been performed to correct obvious mistakes, in particular commission errors. Despite the automatic routine merging fragmented polygons belonging to the same fire event, further fragmentation was found and corrected with a manual merging operation. Morevover, we found that commission was mostly due to undetected cloud and cloud shadows, as well as snow. This wasn't the case in the overall dataset but ony in some regions and particular years. Whenever possible, omission errors where also corrected.   
> **_NOTE:_**  These corrections are not exhaustive and v2 still includes errors of omission and commission as well as mapping inaccuracies.
The number of fire events has been significantly reduced from 10,549 in v1 to 6,745 in v2, which represents a 30.06% of decrease. More specifically, 953 (9%) polygons were merged with other fire events, 	3,195 polygons representing commission errors were deleted (30.3%), and 344 polygons representing omission errors were added (3.3%). In terms of burned area, the reduction rate was 17.87% (3,156.25 km2 to 2,592.32 km2).  
Detail of fire counts differences between v1 and v2 can be found in this table: [`Difference_fire_counts_v1-v2.csv`](Difference_fire_counts_v1-v2.csv).

#### Publication
Detailed methodoly description and accuracy assessment can be found in the following publication:  
Fornacca D, Ren G, Xiao W (2020) Small fires, frequent clouds, rugged terrain and no training data: a methodology to reconstruct fire history in complex landscapes. _International Journal of Wildland Fire_ **30**(2): 125-138. https://doi.org/10.1071/WF20072
