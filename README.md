# DASQR
This is an open access data for the original article "Scalable and Data-Aware SQL Query Recommendations".

In folder "InputLogs" there are two files, "fullLog.txt" and "sampledLog.txt", which stand for full and sampled logs consequently.

Each row (except for the first) of teh files has three values: "seq", "us" and "class". 

1. "seq" is the seq of query in SkyServer query log: http://skyserver.sdss.org/log/en/traffic/sql.asp
To get an actual query by seq one should submit a query like this:
"SELECT *
FROM SqlLog
WHERE seq = 2118885444",
where 2118885444 is seq from either "fullLog.txt" or "sampledLog.txt".

2. "us" stands for user session id.

3. "class" shows to which pool a query (a user session) belong. 
It is used for 10-fold cross-validation in the original experiments of the article "Scalable and Data-Aware SQL Query Recommendations".
