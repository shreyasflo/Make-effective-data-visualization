# P6:Make Effective Data Visualization
Shreyas Ramnath
26thFeb 2018

## Summary
In this project, I focus on visualization by using d3.js and dimple.js.
Data I used in this project is about the baseball players' performance which includes 1157 players.
Data is available [Dataset](https://docs.google.com/document/d/1w7KhqotVi5eoKE3I_AZHbsxdr-NmcWsLTIiZrpxWx4w/pub?embedded=true)


I chose dimple bubble chart due to following reasons.
A bubble chart displays a set of numeric values as circles. It is especially useful for data sets with dozens to hundreds of values, or with values that
differ by several orders of magnitude.
The circles in a bubble chart represent different data values, with the area of a circle corresponding to the value. 
The positions of the bubbles don't mean anything, but are designed to pack the circles together with relatively little wasted space.
Because a bubble chart uses area to represent numbers, it is best for positive values.

I chose three colors yellow,pink and blue to represent handedness as Both, Left and Right respectively.
First I plotted the graphs of average runs vs BMI, to see the number of overweight and normal weight players. The graph depicted that there much more number
of overweight players than normal weight players in the dataset. 

My assumption :
High BMI players tend to have better batting performance.

## Design
Out of the 1157 players I selected the top 60 players in the first graph due to the huge number of data points.
In the subsequent graphs, I performed the classification of the batters in terms of BMI(more than 24 or not) and Handedness.

## Deployment
1. Download the nodejs framework from https://nodejs.org/en/.
2. To install the http-server type npm install http-server on the command line
3. Deploy the http-server by typing http-server & (to run in background)
4. Open the browser and type localhost:8080 to see the graph

Feedback 1: Your visualization is great, however, the message ("High BMI players tend to have better batting performance.".) is not fully addressed.
As you mention in your design section: "Out of the 1157 players I selected the top 60 players in the first graph due to the huge number of data points." 
having so many points is really a problem and would make the visualization impossible to understand. To avoid this problem, you selected 60 players out of 1157... 
note you loss ~94% of your dataset!
Having so many points shouldn't be a problem if there is a clear trend

So, I took the original data set with the 1157 data points instead of the subset of the top 60 players and plotted them in the first graph and I adjusted the scales 
accordingly.

Feedback 2: Well done on addressing the main issue with your visualization.It is great you found a specific finding to focus: "High BMI players tend to have better
batting performance.", however, as I will explain in the following section, the current visualization fails to capture this message and this is why this section 
is marked off.As a suggestion, you also can consider a different chart type, for example, since the message your visualization pretends to convey is: "High BMI
players tend to have better batting performance." why don't you try to represent the mean batting average performance for Low BMI players versus High BMI players?.
This would be a simple visualization that fully addresses the message. Your visualization doesn't need to be complex, but explanatory. That is, the audience should
be able to grasp the main message at first glance in a clear and effective manner.

To end, HR and Handedness are also represented in the visualization, but the main message is not related to them, so you could consider removing them since this 
is not important information in order to help the audience grasp the main message.

So, I plotted the bar charts average vs BMI and HR(home runs) vs BMI and this time considered all the 1157 players. I was able to see the trend that even though
the overweight players have better home runs that normal weight players they suffers in the average runs comparison. So my assumption that higher BMI players 
have a better performance was not supported by the graphs and hence is wrong.

Feedback 3:There are a few changes that you need to make to fulfill the project requirements. Have a look at the comments for details on this.
This was a good first submission. With little more efforts, you will be able to fulfill all the project requirements. Some changes in indentation in the code was 
recommended. I was also ask to change the axis name and units to be more meaningful.
