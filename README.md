# Mall_customer_segmentation
The main aim is to segregate the customers coming to the mall into clusters and target the clusters which are more likely to increase the business revenue

The first step is to import the relevant libraraies.

The next step is to load the dataset

The 3rs step is to analyse and explore the dataset.

Hence, as observed, the dataset conatins 5 columns. We could even go on to find the correlations between all the columns, we could even map the plot for the same. 

(We dropped the columnsID as it as not required for the analysis)

Hence, we plot a heatmap which can be plotted only by using seaborn.

This heatplot tells us the correlations between various columns graphically. Hence, as observed in the heatmap:
a) Higher the correlation, lighter the shade in the heatmap
b) Conclusions :
* ![image](https://user-images.githubusercontent.com/112570856/189483789-208e99fa-956b-41bc-8d01-ea7ba749094f.png)

a) Nil correlations between the spending scores and the age
b) High correlations between the spending scores and the gender 

Now, we try to visualize the various details in order to better understand our data

Now, we go column by column to understand the range of distribution of our data
i.e : Annual income:
a) we need to understand the range of the annual income in our dataset, ie to get an idea about:
*The smallest annual income, the largest and the average. This could help us to give recomm about a product.
*We use a distplot for the same as:
a) It gives an idea about the range in which the data in the column is distributed.
b) Hence, in our case : The annual income is within the range of : 15k$ to around 140k$
c)it is used for plotting the cont variables 

Similarily, we develop a plot to measure the age distribution.In this case it goes from:
18-70

Hence, the distplot helps us to get a clearer picture about the distribution of the attributes

Thus, we go on to do the same for the spending scores.

Now, we wish to know the gender distributions. Hence, 
* 'genders' is a variable which we create to store the gender data.
The gender data tells how many males and females we have in our dataset.
* Now, we just have to visualize this 'genders' data.

We do the same by plotting a barplot.
Thus, there are more females than males in our dataset.

After analysing the range of data in several columns, we need to visually represent the individual correlations between several columns, in order to get better insights about the data.

a) The first step is to plot the annual income vs age wrt gender.
INSIGHTS DRAWN:
A) Based on the heatmap and the scatterplot, we could conclude that the correlation between the age and the annual income is not high, they are correlated but to a lesser extent.
b) There exists, a wide distribution and not a single conclusion could be drawn.

ANALYSIS:
*For the age group of 18-20 : Males have a higher annual income than females.
*for the age group of 20 - approx 25/26 : The number of female customers are higher than males , however, the hishest annual income is that of a male- 79k$ approx.
*Thus, similarily these analysis could be drawn for diff age groups.

Hence, after drawing insights from this graph, we move on to plot another graph. 

*THE graph now plotted is between the annual income and the spending score with gender as a hue

*Analysis:
a) between the age of 18-20 : The females with lower annual income still have a higher spending score, ie:
half of the people with lower annual income have a lower spending score whereas the other half have a higher spending score even with a lower annual income.
b)The highest spending score is by a female with a lower annual income(arround 19k$)
c)the lowest spending score is by a male with an annual income of approx 80k$


Now, we Plot another graph which would give insights on:
*the distribution of the customers in the mall on the basis of their age groups.
*The code algorithm is as follows :
1-dividing the customers into diff age groups by making lists
2-plotting those values on x - axis
3- plotting the count on y axis, ie : there are 38 ppl whose age range is from 18 - 25
4 - plotting all of that in a barplot and then displaying it.

ANALYSIS:
*The maximum number of customers which the mall is getting is from the age range : 26-35
*The minimum number of customers which the mall is getting is from the age range : 55+
*Thus, our target hence should be ppl between 26-35.

WE hence make a similar plot for spending scores :
ANALYSIS:
*the highest customers from the mall are the ppl having a spending score between 26 - 50.
*the lowest customers having to appear in the mall are the ppl having a spending score between 76 - 100

Similarily, an another plot is drawn to get insights about the annual income:
*It is observed that the highest number of customers are from the ppl having an annual income of :$ 60,001 - 90,000
*Lowest  mall visitors are the customers whose income is : $ 120,001 - 150,000

NOW WE START PERFORMING K MEANS CLUSTERING:

