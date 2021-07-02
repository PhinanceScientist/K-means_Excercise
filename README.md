<p align="center">
<a href="https://github.com/PhinanceScientist"><img src = "https://i.ibb.co/NLfc0SV/Deveaner.png" width = 100> </a>
<h1 align="center"><font size = 5>Segmenting and Clustering Neighborhoods in Toronto</font></h1>
</p>

## Introduction

For this project I will be testing some web scraping methods (Beautiful Soup) with python in order to obtain data from a public web page. After cleaning and exploring the data, the goal is to obtain some relevant information from the neighbourhoods from Toronto, Canada based on the information retrieved by the Foursquare API. k-means will be used to group the neighbourhoods and finally I will use the Folium library to visualize the results.

Please do notice that if you want to render this Jupyter notebook (show the folium maps) you can use this link https://nbviewer.jupyter.org/

This project it is divided in Parts, each one with its own conclussion adn references for further analysis.

# <p style =" text-align: center">PART 1</p> 

### Scraping data from Wikipedia using BeautifulSoup

## Final Thoughts <br>

<li>Beautiful Soup is easy to use and understand, really well documented</li>
<li>There were not Borough names for the Not assigned Neighbourhoods, so, we skipped the instruction of using the same name as de Borough for the Neighbourhood with a value of "Not assigned" (March 2020).</li>
<li>The Original table from the wikipedia (March 2020) has fewer rows than the Example's image provide for the instructions. </li>
<li>The example's image showed a duplicate Neighbourhood value for the M5A Postal Code but It was not found in the Wikipedia Table (March 2020).</li>
### References <br>
Medium post: <br>
https://medium.com/analytics-vidhya/web-scraping-wiki-tables-using-beautifulsoup-and-python-6b9ea26d8722 (How BeautifulSoup Works)<br><br>

Coursera threads:<br>
https://www.coursera.org/learn/applied-data-science-capstone/discussions/all/threads/WwZwTZcmQJuGcE2XJuCb4g  (Scrap and turn to dataframe) <br><br>
https://www.coursera.org/learn/applied-data-science-capstone/discussions/all/threads/czrpnE_gEemX6BLS8CLb5g (Group by, merge Poste Code) <br><br>

thispointer.com:<br>
https://thispointer.com/python-pandas-how-to-drop-rows-in-dataframe-by-conditions-on-column-values/ (How to drop rows)
***


# <p style =" text-align: center">PART 2</p> 

## Final Thoughts <br>

<li>The data set provided by the instructions was used in order to simplify the excercise (March 2020).</li>

### References <br>
note.nkmk.me: <br>
https://note.nkmk.me/en/python-pandas-dataframe-rename/ (How to rename dataframe's columns )<br><br>

Stack overflow:<br>
https://stackoverflow.com/questions/43297589/merge-two-data-frames-based-on-common-column-values-in-pandas  (How to merge columns by value in pandas) <br><br>
https://stackoverflow.com/questions/32400867/pandas-read-csv-from-url (How to read CSV from URL) <br><br>

pandas.org:<br>
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html (How to read CSV with pandas)
***

# <p style =" text-align: center">PART 3</p> 

## Report <br>

### I decided to use the Downtown Toronto Borough for this excercise due to its great economic impact and because it has most of the well know neighbourhoods including some of the "Top Ten Best Toronto Neighbourhoods To Live In 2019" according to TorontoRentals.com.

### The clusters were defined by the most common venues: <br>
   <li> Cluster 0: A lot of coffe shops and restaurants<br></li>
   <li> Cluster 1: Public and recreational places like parks and playgrounds<br></li>
   <li> Cluster 2: Self service stores, Grocery Stores and Café<br></li>
    <li>Cluster 3: Airport services<br></li>
    <li>Cluster 4: A lot of coffe shop and recreational places like parks and aquariums, <b>excelent for touristic purposes!</b> <br></li>
***

This notebook was <b>Part 1, 2 and 3</b> of the Final assignment from the week 3 of the Applied Data Science Capstone from IBM Professional Certificate made by <a href='https://www.linkedin.com/in/novelo-luis/'> Luis Novelo </a>