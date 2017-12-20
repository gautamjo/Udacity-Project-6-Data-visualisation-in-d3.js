## Data Visualisation with D3: Total US Flights Cancellations 2008 ##

### Summary ###

There are three visualisations used in this project. All three of them display cancelled flights in the US in year 2008. I started the presentation with a line chart, following it up with an ordered bar chart and finally finishing with a grouped chart. Both the line chart and the bar chart show total annual cancellations broken down into months. The grouped bar chart shows the number of cancellations broken down into months and then further separated by days of week.

### Design ###

I used US flights data from 2008 downloaded from <a href="http://stat-computing.org/dataexpo/2009/the-data.html">this page</a> and is provided by <a href="https://www.transtats.bts.gov/OT_Delay/OT_DelayCause1.asp">RITA</a>. When I started working on the project I focused on designing only one chart which was a grouped chart showing number of cancellations separated by months and days of week. However, after the project was reviewed, I changed my approach and decide to introduce two more chart in order to show the trends more clearly. Below is the image of an initial sketch of the grouped chart I made using ggplot in R: 

#### Initial Sketch in ggplot: ####
![alt text](img/ggplot_grouped_chart.png)

For more information regarding this plot and data re-modelling process kindly click <a href="https://gautamjo.github.io/blogdown/2017/12/12/us-flight-cancellations-in-2008/">here</a>. 

The plot made in ggplot was then replicated in d3. Here is the image of the same:

#### Initial Sketch in d3: ####

![alt text](img/initial_sketch_in_d3.png)

If you wish to view the actual plot clicking [THIS](https://bl.ocks.org/gautamjo/raw/42f15332a5402ade4b314504edd31fb5/3efae9c49f774f414a5ecee4b211514e20dd9025/) link will take you there.


My design choices were to keep the plot simple yet informative. I used minimal backgrounds, basic axes and solid colour schemes for the plots in order to keep the plots easy on the eyes yet look professional. In all the three plot my intentions were to show the viewer flight cancellation trends either on an annual basis or between a particular period of time. To explain this better, here are images of the three plots I have used in this project. 

#### Line Chart: Showing total number cancellations by months ####

![alt text](img/line_chart.png)

Through this line chart we can observe rising and falling trends of cancellations throughout the year from January to December. We can see higher cancellations during the months of Jan, Feb, Mar and Dec. In the month of Februray we can observe highest number of cancellations with the total running above 20000 mark.

#### Ordered Bar Chart: Showing total number cancellation in descending order ####

![alt text](img/ordered_bar_char.png)

The bar chart represents total number of cancelled flights in the US in 2008. It is separated by months and is designed to show the count of cancelled flights in descending order. We can observe highest number of cancellations for the month of February with more than 20000 cancellations. Months of December, January and March are next in line with cancellation reaching above 16000 in each of these months.

#### Grouped Chart: Showing total number of cancellations from Dec-Mar separated by day of week ####

![alt text](img/grouped_chart_month_dow_feb_mar.png)

In this plot the four months (from Feb - Mar as they appear in the ordered chart)  with high cancellations is further separated by days of week. This is to show the viewer number of cancellations according to day of week.

### Feedback ###

I took two feedbacks from 2 different people here are there responses:

#### Interviewer #1 ####
>Your plot is animated but it does not have interactivity. Consider adding a tooltip to display day and count of cancellations so that it bring more clarity for the viewer.

#### Interviewer #2 ####
>Your plot is looking fine but if you add an animated title it might look better as a composition where all elements of the plot, be it shapes or text, are animated.

#### Interviewer #3 ####
> Currently, the visualisation is more exploratory than explanatory. Examples could include trends or periodicity by month or day of the week. This may be helped by a design change such as line charts or small multiples. The bar chart could still work though. Also consider a more divergent colour scheme (it's hard to see colours by day of the week) and using a narrative paragraph to help the reader focus on the main finding(s).

### Post Feedback ###

The changes I made to the chart post feedback are as follows:

* I added a tooltip displaying the name of day and total Number of cancelled flights on that day. I further added highlighting on the bars upon mouseover. 

* I added and styled an animated title in CSS which fades in and settles on top of the plot.  

Final rendition of the visualisation looks this:
<a href="https://bl.ocks.org/gautamjo/raw/42f15332a5402ade4b314504edd31fb5/3efae9c49f774f414a5ecee4b211514e20dd9025"> Final Plot</a>

### Resources ###

* https://d3js.org/

* <a href="https://bl.ocks.org/mbostock">Mike Bostock's Block - bl.ocks.org</a>

* Interactive Data Visualisation in D3 for the web by Scott Muray

* D3.js in action by Elijah Meeks

* Javascript Novice to Ninja by Darren Jones

### Data ###

* <code>total_cancellations_2008.csv</code> Remodelled data used for D3 visualisation.





      

