### Unsupervised Learning in BI

TallyKhata made use of clustering for effective field visits throughout Bangladesh. For context, Bangladesh is divided into 4578 union parishads and merchants are distributed throught. The business questions were:
- How many field officers (FOs) should be deployed for comprehensive coverage?
- Which merchants should the filed-force visit, for optimum coverage in lowest costs?

<p align="center"><img width="600" alt="c4" src="https://github.com/shithi30/Clusters_for_Field_Visit/assets/43873081/4d9cc36d-eaf3-4d7e-a67d-96f96413363d"></p>

DBSCAN and k-Means clustering were applied to address the problems, with DBSCAN proving to be a better fit for the purpose. hDBSCAN (DBSCAN with Haversine/geo distance) was applied for the purpose, which took 2 parameters:
- Radius within which merchants should be searched: 2 * Radius of circular BD area per merchant
- Minimum no. of merchants to form a cluster: 3

<p align="center"><img width="600" alt="c4" src="https://github.com/shithi30/Clusters_for_Field_Visit/assets/43873081/3d6f1093-bb9f-4f0f-8899-a594d8f6f672"></p>

The solution iterated over unions and output no. of FOs (clusters) per union and also their respective shops for visit. A parallel k-Means solution took a predefined 'k' from sillouhette scores, leaving many shops deserted. 

<p align="center"><img width="600" alt="c4" src="https://github.com/shithi30/Clusters_for_Field_Visit/assets/43873081/877cb376-f9af-4578-ab17-9711565734ee"></p>

Hence hDBSCAN was adopted as a more natural solution to the business problem. Also, for experimentation purposes, the algorithm clustered users into 7 clusters based on their usage patterns on the app. 
