<p align="center">
<a href="https://github.com/PhinanceScientist"><img src = "https://i.ibb.co/NLfc0SV/Deveaner.png" width = 100> </a>
</p>
<h1 align=center><font size = 5>Merida Neighbourhoods Clustered by Economic Vulnerability due to the COVID-19 Outbreak</font></h1>
<br>

## Introduction
<br>
For this project I will be using some prepared data from a postal public web page due to the lack of postal and geodata from Mérida, Yucatán in México. The goal is to obtain some relevant information from the economic vulnerability of neighborhoods from Merida based on the information retrieved by the Foursquare API. k-means will be used to group the neighbourhoods and finally I will use the Folium library to visualize the results.
This approach is an attempt for visualizing the main neighborhoods inside Merida in order to cluster the most economic vulnerable places as the COVID-19 expands.

Please do notice that if you want to render this Jupyter notebook (show the folium maps) you can use this link https://nbviewer.jupyter.org/

## Data
<br>
The data needed for this project  can be found on this local postal services web page called <a href="https://www.heraldo.com.mx/"> Heraldo.com.mx </a> where we can find several postal codes from México. In this case we will be focused on <a href="https://www.heraldo.com.mx/yucatan/merida/merida/">Mérida's postal codes</a>.<br>
As for the CSV file used it is based on the first 100 postal codes from Mérida (ascending order starting from the downtown area as common knowledge) and then linked to its own Latitude and Longitude as a result of a Google Maps Search for each one.<br>
The Foursquare's API will be used to retrieve information of the venue on each neighborhood, type of each venue will be our goal to determine how crowded they are and therefore the whole vulnerability of the surrounding area.  

***
# Results and discussion<br>

### I decided to use the  first 100 postal codes from Merida for this excercise due to their exposure in Foursquare as the people found there are most likely to utilice this application for tips and reviews. A brief expected behaviour for each cluster is written next to it.  

### The clusters were defined by the most common type of venue: <br>
   <li> <b>Cluster 0, Sport oriented venues around:</b>   If the places remain closed for activities as expected, it should show moderate economic downturn and represent low risk of contagion.<br></li>
   <li> <b>Cluster 1, Venues for High Income costumers:</b> Common places known for nightlife, economic downturn and expected low risk of contagion as all this venues are closed. <br></li>
   <li> <b>Cluster 2, Restaurants, food venues mostly: </b> High economic downturn, probably most of the venues will received a hard hit on their operations and cashflow, expected shutdown of the smallest venues of this cluster. Low risk of contagion<br></li>
   <li> <b>Cluster 3, Big Box Stores:</b> Places still opened due to their food and basic needs distribution function. The risk of contagions its moderate as people gather for buying.<br></li>
   <li> <b>Cluster 4, Parks and recreational venues as movie theaters and shopping mall:</b> High economic downturn, low risk of contagion.<br></li>
   <li> <b>Cluster 5, Residential area, no parks around but a lot of Convenience Store:</b> Expected economic downturn and moderate contagion risk for the people gathering on the convenience stores. <br></li>
   <li> <b>Cluster 6, Restaurants close to parks or gyms:</b> High economic downturn, low risk of contagion as the gyms remain closed.<br></li>
   <li> <b>Cluster 7, Stables around, outside the city:</b> Expected economic downturn, low risk of contagion.<br></li>
   <li> <b>Cluster 8, Highly touristic places and gyms as the most common venue:</b> Very high economic downturn caused by lack of international tourism, food venues almost closed, moderate risk of contagion<br></li>
   <li> <b>Cluster 9, Outside the city with sports club as the most common venue:</b> Expected economic downturn, low risk of contagion.</br>

 
 # Conclussion<br>
 In conclusion, we can observe that, regardless of the cluster, the most often venue are the restaurants. We should look for special importance to this as this kind of venue shows that it receives the most economic damage during this pandemic.</br> In Mexico, 97% of food related venues are classified as micro or small companies within 10 or fewer employees (CANIRAC, 2014), this means that they are an economic sector highly affected by situations such as COVID-19's outbreak. </br> As society, we and government should take special care for this business sector in an attempt to stop the disappearance of jobs created by restaurant entrepreneurs.
 
 ## Bibliografy
https://molekule.science/places-to-avoid-flu-virus/ <br>
https://www.babymed.com/health-news/8-public-places-avoid-during-cold-and-flu-season <br>
https://www.nhs.uk/conditions/coronavirus-covid-19/ <br>
https://www.health.gov.au/news/health-alerts/novel-coronavirus-2019-ncov-health-alert/what-you-need-to-know-about-coronavirus-covid-19 <br>
https://www.who.int/emergencies/diseases/novel-coronavirus-2019/advice-for-public <br>
https://www.healthline.com/health-news/public-places-and-the-coronavirus-what-to-know#Coronavirus-can-spread-through-contact-with-contaminated-surfaces,-too <br>
https://www.cdc.gov/coronavirus/2019-ncov/prepare/transmission.html <br>
https://www.bbc.com/future/article/20200317-covid-19-how-long-does-the-coronavirus-last-on-surfaces <br>
https://canirac.org.mx/images//files/TODO%20SOBRE%20LA%20MESA%20ESTUDIOS%20DE%20LA%20INDUSTRIA.pdf
***
This notebook was <b>The final Capstone</b> from the week 5 of the Applied Data Science Capstone track from IBM Professional Certificate made by <a href='https://www.linkedin.com/in/novelo-luis/'> Luis Novelo </a>