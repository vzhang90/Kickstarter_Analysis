# **An Analysis of Kickstarter Campaigns**

[Compressed_Kickstarter_Challenge](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Kickstarter_Challenge.zip)

## Overview of Project

Louise is an up-and-coming playwright, whose recent first-ever crowdfunding campaign for her play *Fever* came close to reaching the $10,000 initially estimated goal. Despite not achieving her fundraising goal in a short amount of time, she wants to know how different campaigns fared in relation to their launch dates and their funding goals. 

This project's main purpose is to analyze the data with Excel to organize, sort, and analyze crowdfunding data to determine whether there are specific factors that make a project's campaign successful.

## Analysis & Challenges
***Theater Outcomes vs Launch*** visualized in line chart from Pivot Table generated from *Sheet1* in the Excel data set [Kickstarter_Challenge](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Kickstarter_Challenge.xlsx):

![Theater_Outcomes_vs_Launch](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Theater_Outcomes_vs_Launch.png)

A pivot table was created in the worksheet titled *Theater Outcoes by Launch Date*
  -filters on "Parent Category" and "Years"
    -"Parent Category" is filtered on "theater"
    

***The Outcomes vs Goals*** line chart visualized the data of the outcomes based on pledge goals:
![Outcomes_vs_Goals](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Outcomes_vs_Goals.png)


Difficulties encountered with analyzing Louise's requested data may be challenging in the conversion of the Unix Timestampes in columns Deadline and Launched_at columns in Sheet1 to a readable format.

## Results

To help Louise better understand campaigns from start to finish, the visualized outcomes of all the crowdfunding plays in graphical representations are generated through a pivot table so that she can benefit from additional visualtion of the data so she can see the outcomes of all categories. From analyzing the Kickstarter data with Theater Outcomes based on Launch Date, the line chart shows an increase in successful number of U.S. Theater crowdfudning campaigns in the months May. However, May, June, July, August, and October all had roughly the same number of failed campaigns launched.

To closer look at how campaign length might be might be tied to its outcome.

From analyzing data on the Outcomes based on goals, it can be concluded there tends to be a negative correlation between percentage successful and percentage failed. As the goal amount increases, the overall percentage successful decreases while the overall percentage failed increases.

Throughout analyzing this Kickstarter_Analysis.xlsx, this data set can be challenging in its lack of further trend analysis. With the two month surge in Successful Theater Outcomes by Launch Date, it would be highly recommended to further analyze the correlation between Outcomes and Years with T-tests. Visually, it would be highly recommended to included a correlation co-efficient and trend line associated with each legend. 
