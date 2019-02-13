README
===========================
a brief introdution for how I solved the task one and task two in the assessment in Puget Financial Techinical Assessment.

****
	
|Author|Kiko|
|---|---
|E-mail|hw2671@columbia.edu

****
## catalog
* [import_package](#import_package)
* [structure_of_data](#structure_of_data)
* [challenges](#challenges)
* [overcome](#overcome)


### import_package
-----------
* `requests`
* `scrapy`
* `lxml`
* `json`
* `BeautifulSoup`
* `sys`
* `xlrd`


### structure_of_data
-----------
1. Data is in json format

2. The data in json has key in:

    'District', 'Formatted API', 'Operator Name', 'Operator Code', 'Field Name', 'Field Code', 'API', 'Lease Name', 'Well', 'Well Status', 'Pool WellTypes', 'Section', 'Township', 'Range', 'Base Meridian', 'Area Code', 'Area Name', 'Latitude', 'Longitude', 'GISSourceCode', 'DatumCode', 'BLMWell', 'DryHole', 'Directional', 'Hydraulically Fractured', 'SPUD Date', 'Completion Date', 'Abandoned Date'

3. The value of data is the responding value in the website. If there is no data in that key, the responding value in json data is empty string

4. The number of data equals to the up-to-data searching result in the well website, which is decided by the exact time and date




### challenges
-----------
1. When I clicked search in the well website, the URL didn't change, which was different from the traditional way of scrambling.

2. When I tried to scrambling URLS for dynamic data, I looked at the network in inspect of the website, the Request URL couldn't open.

3. When I downloaded the production data for all wells, I had to do it seperately and thus I had nearly 200k files. 
It was hard to do the following analysis in this amount of files.

### overcome
-----------
1. For challenge 1, I used the method of srambling website for dynamic data. (although it failed)

2. For challenge 2, I found there was a link for download excel containing all the data.
I used Request to download it and converted the excel into JSON format data.

3. I used `pandas` and organized these files in `Dataframe`. `Dataframe` is efficient when dealing with data and it looks well-organized in format.

