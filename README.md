# Sample-oriented-task-driven-visualizations-
## Overview:
This project is to find out which x-axis values are most likely to be representative. 

## Context:

This project is based on   Ferreira, N., Fisher, D., & Konig, A. C. (2014, April). Sample-oriented task-driven visualizations: allowing users to make better, more confident decisions.       In Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (pp. 571-580). ACM

In this paper the author describes the challenges users face when trying to make judgement about probabilistic data generated through samples.  As an example, they look at a bar chart of four years of data (replicated below in Figure 1). Each year has a y-axis value, which is derived from a sample of a larger dataset. For instance, the first value might be the number votes in a given district or riding for 1992, with the average being around 33,000. On top of this is plotted the 95% confidence interval for the mean

<img width="389" alt="Assignment3Fig1" src="https://user-images.githubusercontent.com/32876600/87943670-5c2db700-ca6c-11ea-835b-361f3ff53d06.png">

Figure 1 From (Ferreira et al, 2014)

A challenge that users face is that, for a given y-axis value (eg.42,000), it is difficult to know which x-axis values are most likely to be representative, because the confidence levels overlap and their distributions are different ( the lengths of the confidence interval bar unequal). One of the solutions the author proposes for this problem (Figure 2c) is to allow users to indicate the y-axis value of interest (eg,42,000) and then draw a horizontal line and color bars based on this value. So, bars might be colored red if they are definitely above this value (given the confidence interval), blue if they are definitely below this value, or white if they contain this value.

<img width="441" alt="Assignment3Fig2c" src="https://user-images.githubusercontent.com/32876600/87944641-a8c5c200-ca6d-11ea-9e2e-5b180ffdcfd0.png">

Figure 2c from(Ferreira at el.2014).

## What I have achieved so far are:

•	 Implement the bar coloring as described above - a color scale with three color (blue, white, red)

•	Implement the bar coloring as described in the paper, where the color of the bar is actually based on the amount of data covered (eg. A gradient ranging from dark blue for the distribution being certainly below this y-axis, to white if the value is certainly contained, to dark red if the value is certainly not contained as the distribution is above the axis) 

## Future work (on going):

•	Add interactivity to the above, which allow the user to click on the y axis toe se the value of interest. The bar color should change with respect to what value the user has selected. 

•	Allow users to interactively a range of y value they are interested in, and recolor based on this ( e.g a y-axis band)

## Data: 

The data we test here is through Numpy.radom.normal(mean, std, size = 3650)

## The toolkits:

Matplotlib, Matplotlib. Color, Matplotlib.cm(this is a mixin class to support scalar data to RGBA mapping), NumPy

## The Statistics behind:

Decide what Confidence Interval we want: 95% or 99% are common choices. Then find the "Z" value for that Confidence Interval here:

![95% CON](https://user-images.githubusercontent.com/32876600/87951437-92703400-ca76-11ea-93ed-9fca9f87406f.JPG)

Use that Z value in this formula for the Confidence Interval
 
 Where:
 
•	X is the mean
•	Z is the chosen Z-value from the table above
•	s is the standard deviation
•	n is the number of observations

## Result:
![Capture](https://user-images.githubusercontent.com/32876600/87950640-92bbff80-ca75-11ea-8618-9d1e5d56dd92.JPG)

Note: Max value : mean value



