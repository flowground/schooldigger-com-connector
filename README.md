# ![LOGO](logo.png) SchoolDigger API V1 **flow**ground Connector

## Description

A generated **flow**ground connector for the SchoolDigger API V1 API (version v1).

Generated from: https://api.apis.guru/v2/specs/schooldigger.com/v1/swagger.json<br/>
Generated at: 2019-05-07T17:43:57+03:00

## API Description

Get detailed data on over 120,000 schools and 18,500 districts in the U.S.

## Authorization

This API does not require authorization.

## Actions

### Returns a list of districts

> Search the SchoolDigger database for districts. You may use any combination of criteria as query parameters.

*Tags:* `Districts`

#### Input Parameters
* `st` - _required_ - Two character state (e.g. 'CA') - required
* `q` - _optional_ - Search term - note: will match district name or city (optional)
* `city` - _optional_ - Search for districts in this city (optional)
* `zip` - _optional_ - Search for districts in this 5-digit zip code (optional)
* `nearLatitude` - _optional_ - Search for districts within (distanceMiles) of (nearLatitude)/(nearLongitude) (e.g. 44.982560) (optional) (Pro, Enterprise API levels only. Enterprise API level will flag districts that include lat/long in its attendance boundary.)
* `nearLongitude` - _optional_ - Search for districts within (distanceMiles) of (nearLatitude)/(nearLongitude) (e.g. -124.289185) (optional) (Pro, Enterprise API levels only. Enterprise API level will flag districts that include lat/long in its attendance boundary.)
* `boundaryAddress` - _optional_ - Full U.S. address: flag returned districts that include this address in its attendance boundary. Example: '123 Main St. AnyTown CA 90001' (optional) (Enterprise API level only)
* `distanceMiles` - _optional_ - Search for districts within (distanceMiles) of (nearLatitude)/(nearLongitude) (Default 5 miles) (optional) (Pro, Enterprise API levels only)
* `isInBoundaryOnly` - _optional_ - Return only the districts that include given location (nearLatitdue/nearLongitude) or (nearAddress) in its attendance boundary (Enterprise API level only)
* `boxLatitudeNW` - _optional_ - Search for districts within a 'box' defined by (BoxLatitudeNW/BoxLongitudeNW) to (BoxLongitudeSE/BoxLatitudeSE) (optional)
* `boxLongitudeNW` - _optional_ - Search for districts within a 'box' defined by (BoxLatitudeNW/BoxLongitudeNW) to (BoxLongitudeSE/BoxLatitudeSE) (optional)
* `boxLatitudeSE` - _optional_ - Search for districts within a 'box' defined by (BoxLatitudeNW/BoxLongitudeNW) to (BoxLongitudeSE/BoxLatitudeSE) (optional)
* `boxLongitudeSE` - _optional_ - Search for districts within a 'box' defined by (BoxLatitudeNW/BoxLongitudeNW) to (BoxLongitudeSE/BoxLatitudeSE) (optional)
* `page` - _optional_ - Page number to retrieve (optional, default: 1)
* `perPage` - _optional_ - Number of districts to retrieve on a page (50 max) (optional, default: 10)
* `sortBy` - _optional_ - Sort list. Values are: districtname, distance, rank. For descending order, preceed with '-' i.e. -districtname (optional, default: districtname)
* `appID` - _required_ - Your API app id
* `appKey` - _required_ - Your API app key

### Returns a detailed record for one district

> Retrieve a single district record from the SchoolDigger database

*Tags:* `Districts`

#### Input Parameters
* `id` - _required_ - The 7 digit District ID (e.g. 0642150)
* `appID` - _required_ - Your API app id
* `appKey` - _required_ - Your API app key

### Returns a SchoolDigger district ranking list

*Tags:* `Rankings`

#### Input Parameters
* `st` - _required_ - Two character state (e.g. 'CA')
* `year` - _optional_ - The ranking year (leave blank for most recent year)
* `page` - _optional_ - Page number to retrieve (optional, default: 1)
* `perPage` - _optional_ - Number of districts to retrieve on a page (50 max) (optional, default: 10)
* `appID` - _required_ - Your API app id
* `appKey` - _required_ - Your API app key

### Returns a SchoolDigger school ranking list

*Tags:* `Rankings`

#### Input Parameters
* `st` - _required_ - Two character state (e.g. 'CA')
* `year` - _optional_ - The ranking year (leave blank for most recent year)
* `level` - _optional_ - Level of ranking: 'Elementary', 'Middle', or 'High'
* `page` - _optional_ - Page number to retrieve (optional, default: 1)
* `perPage` - _optional_ - Number of schools to retrieve on a page (50 max) (optional, default: 10)
* `appID` - _required_ - Your API app id
* `appKey` - _required_ - Your API app key

### Returns a list of schools

> Search the SchoolDigger database for schools. You may use any combination of criteria as query parameters.

*Tags:* `Schools`

#### Input Parameters
* `st` - _required_ - Two character state (e.g. 'CA') - required
* `q` - _optional_ - Search term - note: will match school name or city (optional)
* `districtID` - _optional_ - Search for schools within this district (7 digit district id) (optional)
* `level` - _optional_ - Search for schools at this level. Valid values: 'Elementary', 'Middle', 'High', 'Alt', 'Private' (optional)
* `city` - _optional_ - Search for schools in this city (optional)
* `zip` - _optional_ - Search for schools in this 5-digit zip code (optional)
* `isMagnet` - _optional_ - True = return only magnet schools, False = return only non-magnet schools (optional) (Pro, Enterprise API levels only)
* `isCharter` - _optional_ - True = return only charter schools, False = return only non-charter schools (optional) (Pro, Enterprise API levels only)
* `isVirtual` - _optional_ - True = return only virtual schools, False = return only non-virtual schools (optional) (Pro, Enterprise API levels only)
* `isTitleI` - _optional_ - True = return only Title I schools, False = return only non-Title I schools (optional) (Pro, Enterprise API levels only)
* `isTitleISchoolwide` - _optional_ - True = return only Title I schoolwide schools, False = return only non-Title I Schoolwide schools (optional) (Pro, Enterprise API levels only)
* `nearLatitude` - _optional_ - Search for schools within (distanceMiles) of (nearLatitude)/(nearLongitude) (e.g. 44.982560) (optional) (Pro, Enterprise API levels only. Enterprise API level will flag schools that include lat/long in its attendance boundary.)
* `nearLongitude` - _optional_ - Search for schools within (distanceMiles) of (nearLatitude)/(nearLongitude) (e.g. -124.289185) (optional) (Pro, Enterprise API levels only. Enterprise API level will flag schools that include lat/long in its attendance boundary.)
* `boundaryAddress` - _optional_ - Full U.S. address: flag returned schools that include this address in its attendance boundary. Example: '123 Main St. AnyTown CA 90001' (optional) (Enterprise API level only)
* `distanceMiles` - _optional_ - Search for schools within (distanceMiles) of (nearLatitude)/(nearLongitude) (Default 5 miles) (optional) (Pro, Enterprise API levels only)
* `isInBoundaryOnly` - _optional_ - Return only the schools that include given location (nearLatitdue/nearLongitude) or (nearAddress) in its attendance boundary (Enterprise API level only)
* `boxLatitudeNW` - _optional_ - Search for schools within a 'box' defined by (boxLatitudeNW/boxLongitudeNW) to (boxLongitudeSE/boxLatitudeSE) (optional)
* `boxLongitudeNW` - _optional_ - Search for schools within a 'box' defined by (boxLatitudeNW/boxLongitudeNW) to (boxLongitudeSE/boxLatitudeSE) (optional)
* `boxLatitudeSE` - _optional_ - Search for schools within a 'box' defined by (boxLatitudeNW/boxLongitudeNW) to (boxLongitudeSE/boxLatitudeSE) (optional)
* `boxLongitudeSE` - _optional_ - Search for schools within a 'box' defined by (boxLatitudeNW/boxLongitudeNW) to (boxLongitudeSE/boxLatitudeSE) (optional)
* `page` - _optional_ - Page number to retrieve (optional, default: 1)
* `perPage` - _optional_ - Number of schools to retrieve on a page (50 max) (optional, default: 10)
* `sortBy` - _optional_ - Sort list. Values are: schoolname, distance, rank. For descending order, preceed with '-' i.e. -schoolname (optional, default: schoolname)
* `appID` - _required_ - Your API app id
* `appKey` - _required_ - Your API app key

### Returns a detailed record for one school

> Retrieve a school record from the SchoolDigger database

*Tags:* `Schools`

#### Input Parameters
* `id` - _required_ - The 12 digit School ID (e.g. 064215006903)
* `appID` - _required_ - Your API app id
* `appKey` - _required_ - Your API app key

## License

**flow**ground :- Telekom iPaaS / schooldigger-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
