TallyKhata made use of clustering for effective field visits throughout Bangladesh. For context, Bangladesh is divided into 4578 union parishads and merchants were distributed throught. The business questions were:
- How many field officers should be deployed?
- Which merchants would the filed force visit, for optimum coverage in lowest costs?

DBSCAN and k-Mean clustering were applied to address the problem, with DBSCAN proving to be a better fit for the purpose. hDBSCAN (DBSCAN with Haversine distance) was applied for the purpose, which took 2 parameters:
- Radius within which merchants should be searched: 2 * Radius of circular BD area per merchant
- Minimum no. of merchants to form a cluster: 3
