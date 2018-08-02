# Data Science: Final Project Scoping

## Classifying Use Types for the City of Montgomery<img src="https://www.camelliabowl.com/wp-content/uploads/2016/07/City-of-Montgomery-300x235.png" alt="Smiley face" style="float:right">

**In an effort to reduce workload and minimize error for the City of Montgomery's Permit Department, the categorization of certain fields based on user input could be implemented using machine learning.**

### The Problem:
Currently, city personel manually enter data into a program to record building permits.  Multiple fields are populated by the user.  However, one of the fields is manually entered memo text that contains a broad description of the permit for which a contractor is applying.  Could automatically categorizing the "Use Type" and potentially other fields based on this text reduce staff workload and significantly improve accuracy?

### Solution:
There are various data science models which can classify certain fields much easier and with a higher degree of accuracy than humans.  The most likely path for success in this case is to use natural language processing to preprocesses the "Description" memo field and use Logistic Regression, Decision Trees, or another similar model to classify certain categorical fields.  In the end, the most accurate model will be implemented for production. 

### The Data:
[City of Montgomery Building Permits 2014 to Present](https://data.montgomeryal.gov/Permits/Building-Permit-2014-Present-Download-/qvzc-ejq2 "City of Montgomery Building Permits")

#### Key Data Columns for Automation
| Column | Type of Data | Examples |
| ------------- |:-------------:| :-------------:|
| description | text | 'REPLACE WINDOWS TO EXISTING SINGLE FAMILY DWELLING. BEDROOM WINDOWS PER CODES. TO MEET ALL APPLICABLE CODES.' |
| usetype | nominal | 'Residential', 'Commercial', 'Mixed Occupancy' |
| jobtype | nominal | 'New', 'Existing', 'Alteration' |
| licensefeetype | nominal | 'Building Fee', 'Lic Fee', 'Base Permit Fee'

#### Other Data Columns for Analysis
| Column | Type of Data | Examples | 
| ------------- |:-------------:| :-------------:|
| contractors_location | lat/long | {'type': 'Point', 'coordinates': [-86.187505, 32.312643]} |
| contractorsname | nominal | 'LOWDER NEW HOMES', 'CERT OF OCCUPANCY', 'WINDOWS USA' |
| estimatedcost | numeric | 0.0, 1000.0, 5000.0 |
| owners_location | nominal | {'type': 'Point', 'coordinates': [-86.187022, 32.312276]} |
| ownersname | nominal | 'LOWDER NEW HOMES', 'STONE MARTIN BUILDERS', 'D R HORTON' |
| parcelno | nominal | '10 04 18 1 001 001.000', '10 04 18 1 036 002.000', '09 05 21 2 000 001.006' |
| permitno | nominal | 'B171250', 'B180601', 'B180453' |
| permittypecode | nominal | 'B434', 'B437', 'B101' |
| permittypedescription | nominal | 'Additions, Residential', 'Addition, Commercial', 'New Single Family Residence' |
| physical_location | lat/long | {'type': 'Point', 'coordinates': [-86.302972, 32.377624]} |
| physical_location_address | nominal | '445 DEXTER AVE', '1470 TAYLOR RD', '36 DEXTER AVE' |
| physical_location_city | nominal | 'MONTGOMERY', 'HOPE HULL', 'PIKE ROAD' |
| physical_location_state | nominal | 'AL', 'GA' |
| physical_location_zip | numeric | 0, 36117, 36116 |
| subdiv | nominal | ' ', 'THE PLAZA AT CENTENIAL HILL 1B', 'RYAN RIDGE 8' |
| totalfee | numeric | 50.0, 0.0, 25.0 |
| zoning | nominal | 'PUD', 'B-2', 'B-3' |

### Business Benefits:
The automation of populating the Use Type code, and possibly others, would: 
1. Reduce/eliminate the time it takes a user to manually populate Use Type and other fields;
2. Ensure better record keeping by correctly classifying target fields;
3. Possibily lead to more accurate fees being charged for the given permit.

### Stakeholders:
City personnel along with city elected officials, particularly the mayor, should find this extremely appealing.  In addition, the successful implementation of this solution *could lead to additional contracts with the city as well as other government client opportunities*.
>"Technological advancement is also occurring as we construct an innovation district and move forward with attaining Smart City/Smart Base status. Unforeseen business and military opportunities will abound thanks to our embrace of technology." 
[2017 Year in Review: Montgomery Mayor Todd Strange](https://www.montgomeryadvertiser.com/story/opinion/columnists/2017/12/30/2017-year-review-montgomery-mayor-todd-strange/992698001/)
### Publication:

Because the data is "open", sharing this repository via github, posting links to social media, and tagging various elected officials could garner attention for the need for the city to invest in this and similar data science projects, which would lead to taxpayer and city budget savings.
