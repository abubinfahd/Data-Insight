
The North American Industry Classification System (NAICS) is an industry classification system developed by the statistical agencies of Canada, Mexico, and the United States. NAICS is designed to provide common definitions of the industrial structure of the three countries and a common statistical framework to facilitate the analysis of the three economies.

Time series analysis is a statistical technique that deals with time-series data, or trend analysis.  Time series data means that data is in a series of particular time periods or intervals.

The files from the data set are flat files, Excel (.xlsx), and CSV (.csv) files, we will merge and append data from several files to make a Data Output file. Our first task would be to carry out some data wrangling processes before we can make analysis, ask questions, and gain insights. 

Summary of the data set files we will be using:-
- 15 RTRA (Real-Time Remote Access) CSV files containing employment data by industry at different levels of aggregation, 2-digit NAICS, 3-digit NAICS, and 4-digit NAICS. We will search through rows with 2, or 3, or 4 digits NAICS and append employment data each month of each year from 1997 - 2018 
	Meaning of columns in the files:
		- SYEAR: Survey Year
		- SMTH: Survey Month
		- NAICS: Industry name and associated NAICS code in the bracket
		- _EMPLOYMENT_: Employment


- LMO Detailed Industries by NAICS: An excel file for mapping the RTRA data to the desired data row.
 Columns in the file:
		- Column 1 lists all 59 industries that are used frequently 
		- Column 2 list the industries NAICS definitions


As part of our data wrangling, we would create a dataset of monthly employment series from 1997 to 2018 for the industries.

One of the guiding principles for our data wrangling is to try to create each series from the highest possible level of aggregation in the raw data files, thus, if an LMO Detailed Industry is defined with a 2-digit NAICS only, we would not use a lower level of aggregation (i.e. 3-digit or 4-digit level NAICS files in the RTRA), similarly, if an LMO Detailed Industry is defined with a 3-digit NAICS only, we would not use the 4-digit NAICS files for that industry. 
