---
title: "Datasets used"
questions:
- "What datasets will be used?"
- "Where do these datesets come from?"
- "What modified versions are available from this site" 
objectives:
- "Understand the bckground and format of the datasets to be used"
- "Understand their origin"
- "Undersstand which variations have been prepared for each lesson"
keypoints:
- "Identify the files and their locations"
---

## Audit of Political Engagement 11, 2013 (UKDS: SN7577)

### Where to find it:
The dataset is an open dataset available for download from the UK Data Service. [link to SN7577](https://discover.ukdataservice.ac.uk/?q=sn7577) It can be found by searching using the keyword SN7577.
### Variations available
The dataset being used is the 2013 edition. Several other years are available, although the columns may change. There is also a combined dataset for the years 2003-2012 under SN 7404.
### Format and details:
Downloadable formats are: SPSS, Stata and tab delimited.
There are 1286 records of 203 columns. The tab data is almost entirely numeric (integers) factors.
The SPSS file can be used to substitute the factor values for the relevant text. A constructed mix of the two variations is likely to be used.
There are many examples of missing data in the dataset.
One section on Newspapers read and Web use is ideal for demonstrating long to wide conversions (and vice cersa)
There are no examples of dates. The only real continuous variable is a weight, which is likely to be of limited use

The formats in which we will use it
(The full filenames as downloaded, audit_of_political_engagement_11, have been changed to SN7577 for brevity)

| *Name & Format* | *How we got it* | *Where we will use it* |
|-----------------|:----------------|:-----------------------|
| SN7577_spss.sav | Direct download from UK Data Service	| In the R module to demonstrate loading SPSS files into R. It has also been used to generate (using R code) the two files; SN7577_1.csv and SN7577_2.csv. (described later)|
| SN7577.tab |Direct download from UK Data Service |	Spreadsheet modules, Open Refine module, SQL module, Python module |
| SN7577_1.csv | Derived from SN7577_spss.sav | This is the .csv equivalent of SN7577.tab. However the missing values have been replaced with NA (as part of the processing in R) |
| SN7577_2.csv | Derived from SN7577_spss.sav |	This is another.csv file of the SN7577 data. However in this case the numerical factor values have been replaced by the equivalent text (as given by the data dictionary) Again, this was generated automatically from the SPSS version of the data when it was read into R |
| SN7577.sqlite | Loaded as an SQLite table | SQL module |

## SAFI (working title - I don't actually know what the project is called

### What it is:
This is survey data relating to households and agriculture in Tanzania and Mozambique. 
The survey has been created using the ODK (Open Data Kit) software via an Excel spreadsheet. 
This is used to create a form which can be downloaded and displayed (and completed) on an Android smartphone. 
The results are then sent back to a central server. 
The server can be used to produce the collected data in both JSON and XLSX formats. 
### Where to find it
This data has been made available by the SAFI project
### Variations and formats
This is original data from a currently running project, it is possible that the volume of data may increase before the end of the year. 
The dataset has been chosen because it is natively available in JSON and the variety of data types available within it. 
The .xlsx and .csv versions help illustrate the shortcomings of using structured data formats when presenting semi-structured data.
### Format and details:
The data is available in both JSON and .xlsx formats. 
There are separate files for each country. 
CSV files can be created from the .xlsx files and/or processing the JSON files. 
Because of the weird headings used in the .xlsx files we have chosen to create our own from the original JSON files.
The JSON documents demonstrate a complexity which makes it cumbersome at best to represent as structured data.
There is missing data in different forms and formats. 
There are text and numeric fields. 
There are typos. 
There are both date and Timestamp fields.

The formats in which we will use it

| *Name & Format*	       | *How we got it*	| *Where we will use it* |
|------------------------|:-----------------|:-----------------------|
| SAFI_Mozambique (JSON) |	SAFI project    |	Python module          |
| SAFI_Mozambique (CSV) (selected tables) |	Derived from SAFI project |	OpenRefine module, R module |
| SAFI_Mozambique (XLSX) | SAFI project |	Spreadsheets module |
| SAFI_Mozambique (SQLite) | Derived from SAFI project | SQL module |
	 	


