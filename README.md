# TaskForBeyondAnalysis
The program is writen in python with jupyter tool suite.

1. The program partitions the main file into many files sorted by date.
	Here we see anomalies - e.g. row number 782435 has dropoff date of 2003.
	Since the files are partitioned by date, it is easy to see these anomalies.

2. The data is read again, but only the rows with expected dates.
	In this case we started with 6405008 entries, now we have 6402165.
	All anomalous entries remain stored in the ./partitioned folder and can be used for closer inspection.

3. The re-read data (from dataFrame newdf) is uploaded to sql database.
	Implementation is reusable - if, let's say we want to add another dataframe of dates 2020-02, we can change the part_files to "./paritioned/*2020-02&/*".
	When loading to database, we use if_exists = 'apend', so new data can be added to existing database.

ER diagram:
![ERD photo](/ERD.PNG)
