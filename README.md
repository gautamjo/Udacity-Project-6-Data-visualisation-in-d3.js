## Data Visualisation with D3: Total US Flights Cancellations 2008 ##

### Summary ###

There are three visualisations used in this project. All three of them display cancelled flights in the US in year 2008. I started the presentation with a line chart, following it up with an ordered bar chart and finally finishing with a grouped chart. Both the line chart and the bar chart show total annual cancellations broken down into months. The grouped bar chart shows the number of cancellations broken down into months and then further separated by days of week.

### Design ###

I used US flights data from 2008 downloaded from <a href="http://stat-computing.org/dataexpo/2009/the-data.html">this page</a> and is provided by <a href="https://www.transtats.bts.gov/OT_Delay/OT_DelayCause1.asp">RITA</a>. When I started working on the project I focused on designing only one chart which was a grouped chart showing number of cancellations separated by months and days of week. However, after the project was reviewed, I changed my approach and decide to introduce two more chart in order to show the trends more clearly. Below is the image of an initial sketch of the grouped chart I made using ggplot in R. 

![alt text](img/ggplot_grouped_chart.png)

For more information regarding this plot and data re-modelling process kindly click <a href="https://gautamjo.github.io/blogdown/2017/12/12/us-flight-cancellations-in-2008/">here</a>. 


My design choices were to keep the plot simple yet informative. I used minimal backgrounds, basic axes and solid colour schemes for the plots in order to keep the plots easy on the eyes yet look professional. In all the three plot my intentions have been to show the viewer flight cancellation trends on an annual basis. To explain this better, here are images of the three plots I have used in this project. 

#### Line Chart: ####

![alt text](img/line_chart.png)

#### Ordered Bar Chart: ####

![alt text](img/ordered_bar_char.png)

#### Grouped Chart: ####

![alt text](img/grouped_chart_month_dow_feb_mar.png)

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





      

