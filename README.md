# Repository Data (RepoData) for United States Archives

## About

This repository contains the public-facing data for the RepoData project, an effort to gather a comprehensive data set of US archival repositories. The RepoData project team contacted over 150 archival organizations, and received more than 30,000 data points for archives and institutions with archival records across the United States.

## Contact Information

Ben Goldman, Penn State University, bmg17@psu.edu
Eira Tansey, University of Cincinnati, eira.tansey@uc.edu

## Credit/Citation

RepoData, 2017-2019, Ben Goldman, Eira Tansey, and Whitney Ray.

## Access/Use

This data is licensed under ODbL 1.0 license (Open Data Commons Open Database License: https://opendatacommons.org/licenses/odbl/summary/) We ask that any re-use of this data acknowledge both RepoData and the original source of individual data points.

All code (located in the `bin` directory) is released under an [MIT License](https://opensource.org/licenses/MIT).

## Date of collection

Data collected and processed between 2017-2019.

## Project Website

https://repositorydata.wordpress.com/

## Status

As of March 1, 2019, all 50 states are now available, as well as Washington DC.

## Funding Source

This project was supported by a Society of American Archivists Foundation grant awarded in 2017. Data processing was completed on March 1, 2019.

## Additional Acknowledgements

We are greatly indebted to Hillel Arnold and Ed Summers for their continued advisement on data maintenance and contributions to this repository.

We would also like to thank the following organizations that shared data with us:

* Archivists for Congregations of Women Religious
* National Association of Government Archivists and Records Administrators
* NARA
* Business Archives Section
* National Library of Medicine
* National Park Service
* John Slate and Dave Evans survey of Local Government Repositories
* UT iSchool
* ASHRAB
* Northwest Archivists, Inc., Directory
* Society of Alabama Archivists
* Alabama Department of Archives and History
* Arkansas State Archives
* Arizona Archivists Alliance (AZAA) (President)
* Society of Southwest Archivists
* Society of Rocky Mountain Archivists
* Online Archive of California
* LA As Subject
* County Recorders' Association of California
* California State Archives
* Los Angeles Archivists Collective
* Society of California Archivists
* CHRAB
* CT SHRAB
* New England Archivists
* New England Archivists of Religious Institutions
* District of Columbia Caucus of MARAC
* District of Columbia Office of Public Records
* SAA@CUA
* Archivists of Metro D.C.
* Historical Society of Washington, D.C.
* WorldBank Archives
* Delaware Public Archives
* Society of Florida Archivists
* University of Central Florida
* Florida HRAB
* Georgia Historical Records Advisory Council.
* Society of Georgia Archivists
* Association of Hawai'i Archivists
* HI SHRAB
* State Historical Society of Iowa
* Consortium of Iowa Archivists
* Idaho State Archives
* Chicago Area Religious Archives
* Illinois SHRAB
* Chicago Area Archivists
* Chicago Area Medical Archivists
* Midwest Archives Conference
* Indiana Historical Society
* Society of Indiana Archivists
* Indiana State Library
* Kansas Historical Society
* Kentucky Council on Archives
* Louisiana Archives and Manuscripts Association
* Greater New Orleans Archives Directory
* Lousiana HRAB
* Massachusetts Board of Library Commissioners
* Massachusetts SHRAB
* University of Massachusetts
* New England Association of City and Town Clerks
* Maryland State Archives
* Maine Archives and Museums
* Metro Detroit Archivists League
* MSHRAB
* Michigan Museums Association
* Historical Society of Michigan
* Michigan Archival Association
* Minnesota Digital Library
* Minnesota SHRAB (Minnesota Historical Society)
* Twin Cities Archives Round Table
* Association of St. Louis Area Archivists
* Kansas City Area Archivists
* MHRAB
* Saint Louis Area Religious Archivists
* State Historical Society of Missouri
* Society of Mississippi Archivists
* Mississippi HRAB
* Montana Memory Project
* Montana Library Association
* Montana SHRAB
* Museums Association of Montana
* Federation of North Carolina Historical Societies
* North Carolina Digital Heritage Center
* North Carolina SHRAB
* Society of North Carolina Archivists
* North Dakota SHRAB
* Nebraska State Historical Society (Listed as Nebraska SHRAB on CoSA)
* New Hampshire Historical Society
* New Hampshire Archives Group
* New Hampshire SHRAB
* New Jersey SHRAB
* New Mexico HRAB
* Nevada SHRAB
* Archivists Round Table of Metropolitan New York, Inc. (A.R.T.) (President)
* Capital Area Archivists of New York (CAA)
* New York Archives Conference
* Documentary Heritage and Preservation Services for New York
* ReCAP
* Mid-Atlantic Regional Archives Conference
* Cleveland Archival Roundtable
* Ohio Local History Alliance
* Cincinnati Area Archives Roundtable
* Society of Ohio Archivists
* Miami Valley Archivists Roundtable
* OHRAB
* Tri-State Catholic Archivists
* Oklahoma Historical Society
* Central Oklahoma Archivists League
* Oregon SHRAB
* Hidden Collections Initiative for Pennsylvania Small Archival Repositories (maintained by the Historical Society of Pennsylvania)
* Pennsylvania Historical and Museum Commission
* Pennsylvania Historical and Museum Commission
* Pennsylvania Historical and Museum Commission
* Heinz History Center
* Philadelphia Area Consortium of Special Collections Libraries (PACSCL)
* Three Rivers Archivists
* Delaware Valley Archivists Group
* RIHRAB
* South Carolina Department of Archives and History
* South Carolina Archival Association
* Charleston Archives, Libraries and Museum Council
* South Dakota SHRAB
* Tennessee State Library and Archives
* Society of Tennessee Archivists
* Texas HRAB
* San Antonio Regional Archivists
* Archivists of the Houston Area
* Archivists of Central Texas
* Utah SHRAB / Utah State Archives and Records Service
* Conference of Inter-Mountain Archivists
* Library of Virginia (Virginia SHRAB)
* Virginia Association of Museums
* Vermont SHRAB
* Washington SHRAB
* Seattle Area Archivists
* Southeastern Wisconsin Archives Group
* Wisconsin SHRAB
* West Virginia Archives and History
* Wyoming State Archives

## Utilities

This repository also contains Python 3 utility scripts:
* `convert.py`, which creates JSON and GeoJSON derivatives from the main CSV file.
* `check.py`, which makes sure all the column headers in the Excel files match (this is important because the column headers are used by the JSON serialization).
* `generate_ids`, which generates unique identifiers for all repositories in a source CSV file.
* `geocode.py`, which adds geocoding data exported from ArcGIS to the main CSV file.
* `trim_rows`, which ensures that all rows in the source CSV are the same length.

### Usage

To run any of these scripts, first navigate into the `bin` directory:

```
$ cd bin/
```

Then, install the required packages:

```
$ pip install -r requirements.txt
```

Finally, run the script:

```
$ python convert.py
```
or
```
$ python check.py
```

#### Optional arguments for convert.py

If you want to produce a single output format, you can pass `convert.py` an argument:

```
$ python convert.py -o format
```

where `format` is the output format. Choices are `csv` and `json`.
