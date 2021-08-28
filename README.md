# Module-1-Challenge
# Kickstarting with Excel
## Written Analysis

## Overview of Project
We will visualize campaign outcomes based on their launch dates and their funding goals.

### Purpose
The purpose of this analysis was to visualize how different campaigns fared in relation to their launch dates and their funding goals and understand the trends behind the data.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
I first wanted to create a new column "Years" in order to only extract the year from when these campaigns were created.
I did this by using function YEAR() and inputting S2 (the date created conversion) inside the function in order to retrieve the year of the first row. Then, I double clicked the bottom corner of the cell in order to apply the function to the entire column in accordance with each row.

Then, we created a pivot table using the parent category and years as the filters and filtered the parent category as "theatre", and at first I had to play with the pivot table in order to get the months but finally I used the "Date Created" conversion column to put inside rows. After, outcomes were used in columns as well as values in order to see which succeeded, failed, and canceled, as well as to see the counts of those outcomes for each month.

One challenge I saw myself and can see other people have is struggling to understand ways of retrieving the months of the data rather than the years or the quarters, but I think it just takes practice and plugging in and out in order to find that data.

![Theatre_Outcomes_vs_Launch](https://user-images.githubusercontent.com/57331058/131198675-88a3a204-2c8c-4b49-8b93-6985c18240ba.PNG)

Finally, we're able to create a line graph from this data and can clearly see that the majority of theatre events/campaigns were successful every month, then some failed, and very few of those were canceled. What we can also see from taking a look at this line graph is theatre events/campaigns were most successful in May and becomes least successful in the winter time. From this data, we can interpret that theatre campaigns may have a better chance at being successful when started in Spring/Early Summer which is useful information for people who would be interested in creating a theatre campaign. 
There could be a number of reasons as to why the numbers of success is high in the summer such as kids not having school and families wanting to go outside of the house more, depending on the state or country there could be an increase in the number of tourists around that time, meanwhile in the winter time less people are fond of going out and travelling in colder weather and there's less theatre campaigns starting around winter time anyway.

### Analysis of Outcomes Based on Goals
In this analysis, the purpose was to view the percentage of successful, failed, and canceled plays based on the funding goal amount and see if there was a correlation between the goal amount and the outcome.
We first created columns: goal, number successful, number failed, number canceled, total projects, percentage successful, percentage failed, and percentage canceled.

In the goal column, each row had a range in order to group these campaigns based on their goal range.

![image](https://user-images.githubusercontent.com/57331058/131199868-e54c8689-f9ce-43db-bdac-1570bd478197.png)

(This photo was taken from GWU Module only to help reader see the ranges that were used in each row.)

For the first three columns after Goal, the function COUNTIFS() was used in order to only count the data where the goal was in the range of that specific row, had the subcategory of "plays", and had the correct outcome for each column.

For example, if we wanted the count of the number successful in plays between the goal range of $25000 to $29999, the function would look like this:
![Functions COUNTIFS example](https://user-images.githubusercontent.com/57331058/131200269-59859526-6f55-4ef9-94d2-6822ad2b860f.PNG)

Where the D column would be the goal number we are grouping by ranges, F would be the outcome we are trying to find whether it's successful, failed, or canceled, and the R column would be the subcategory in which we are only looking for plays.

After finishing those numbers, we will use the SUM() function in the Total Projects column and add those three columns. We can do that quick by using =SUM(B2:D2), and then double clicking on the bottom left corner of the cell in order to apply it to the entire column accordingly.

In the last three columns, we will be using the IFERROR() and ROUND() function in order to get the percentage of the each outcome. We do so by dividing each outcome column by the total projects column, multiplying by 100, allowing 2 decimals, and if this function stumbles upon dividing by 0 then the error default result will be 0. 

Below is the function of percentage successful in the range of 5000 to 9999.

![Percentage Successful Example](https://user-images.githubusercontent.com/57331058/131200566-c18fc4bc-cbdf-489c-8de8-74a38c48917a.PNG)

Now, I have sufficient information in order to create a line chart where the x-axis will have the goal ranges, and the y-axis has the percentage of each outcome.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/57331058/131200642-e2d8d810-31ae-40ab-837c-a990f89111d0.PNG)

In this line graph, it's interesting to see because it looks like the percentage successful tends to be approximately 100 when the goal is either on the low extremity or the high extremety. We also see that in the middle there is still an intermediate to high successful percentage when the goal is between 25000 to 34000. The reason for these results could be that lower goals are easier to achieve, and higher goals could possibly do a lot more campaigning for their event.

One challenge I came across was trying to get the graph looking like the example we were shown, but it wasn't working because I accidentally graphed and used the pledged column at first rather than using the goal column. After doing that, the graph looked a LOT better. Other small mistakes I had to catch myself in were just making sure that the functions in these calculations were correct because I even caught myself missing a comma which easily made my argument pointless.

## Results
One conclusion we can draw from the Theater Outcomes by Launch Date is that people tend to do more and be out of the house a lot more when the weather is warm, allowing such campaigns that start during warm weather to have a higher chance of success. Another conclusion is that there are also more travelers during warm weather and most schools tend to have vacations right around early summer time.


A conclusion we can draw from the Outcomes based on Goals data and graph is that lower goals are easier to achieve and that can increase the chance of success, and higher goals on the extreme side may have a lot to correlate with how much they campaign for such a great amount of money.


Some limitations of this dataset could be the categories of these plays, the season of each country when the campaign started, and maybe even how they raised money for each campaign because there can be an influence on different kinds of ways people promote their events. Having all that information can aid in the confirmation of as to why certain events are more successful than others. Another limitation could be that we don't have the reason for why certain events were canceled and it would be interesting to view reasons why events tend to cancel.


There is so many tables and graphs we could create from this. We can easily find ways to analyze when categories or subcategories are the most popular during the year, whether shorter campaigns or longer campaigns have a higher success rate by calculating how long each campaign was in a new column and the outcome.
