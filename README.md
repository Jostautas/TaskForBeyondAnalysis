# TaskForBeyondAnalysis
The program is writen in python with jupyter tool suite.

1. The program partitions the main file into many files sorted by date.
	Here we see anomalies - e.g. row number 782435 has dropoff date of 2003.
	Since the files are partitioned by date, it is easy to see these anomalies.

2. The data is read again, but only the rows with expected dates.
	In this case we started with 6405008 entries, now we have 6402165.
	All anomalous entries remain stored in the ./partitioned folder and can be used for closer inspection.

