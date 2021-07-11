### Table of Contents
1. Installation
2. Project Motivation
3. File Descriptions
4. Results
5. Author and Acknowledgements


### Installation

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3.*.

### Project Motivation

I analysed Airbnb listings data obtained from the Inside Airbnb site to understand:


### File Descriptions
The Jupyter notebook contains the codes used for this exploratory analysis. 
The "data" folder contains the files downloaded from the Inside Airbnb site. 
The "assets" folder contains the charts from the Jupyter Notebook. 

### CRISP-DM Process
1. Business Understanding
London is one of the biggest markets in Europe for Airbnb. A typical holidaymaker that wants to book a stay in London might have the following questions in mind:
a) How does London listings compare with other European cities?
b) How does London listing prices change from now till end of year?
c) What is the distribution of listings in London?
d) Which borough has the best reviews?
e) How much can you expect to save by living in Outer London vs Inner London?

2. Data Understanding
We can use data from Inside Airbnb [website](http://insideairbnb.com/get-the-data.html) to answer these questions. They are stored in the "data" folder of this repository. Data that we use is as followings:
a) Listings data from European capital cities - this provides information on location, price, number of reviews, review score, etc.
b) Calendar data - this provides information on how each individual listing in London is priced over the next year. 
c) Reviews data - this provides all review comments that a listing has ever received.

3. Prepare Data
a) For the listings data of the different cities, we format the price field by converting it from string to integer so we can use price in our computations. For London listings, we merge it with [data](https://data.london.gov.uk/dataset/london-borough-profiles) from London Data Store (by the Great London Authority), so that we can identify which boroughs belong to inner and outer London. 
b) For the calendar data, we drop rows with missing price as it is only 0.01% of the dataset. 

4. Data Modeling
No modeling is required here. We are using descriptive statistics and data visualisation to answer the business questions in point 1. 

5. Results
Results can be summarised as follows:
a) London has the most listings compared to Paris, Amsterdam, Berlin and Madrid. In fact, it has more than Amsterdam, Berlin and Madrid combined, although London prices are in middle of the range. 
b) London prices for hotel rooms fluctuate between weekends and weekdays, with a 11% premium charged on weekdays. 
c) In London, top 10 boroughs with the most listings are from Inner London, and this constitutes over two thirds of total listings. 
d) Out of the top 10 boroughs with the best reviews, 8 are from Outer London. Westminster and Kensington & Chelsea, which charge the top 2 highest prices per night and are top 4 in most listings, are in the top 4 lowest scores.
e) You can expect to pay a 33% premium for an entire flat/home in Inner London compared to Outer London.

More details on the findings can be found at the post available [here](https://medium.com/@bryanchen21/londons-airbnb-market-explained-visually-2b9bb4d746aa).


### Author and Acknowledgements
- **Bryan Chen** - bryanchen21@gmail.com
- Credits to Inside Airbnb for the data. 
