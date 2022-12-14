# **An Analysis of Kickstarter Campaigns**

[Compressed_Kickstarter_Challenge](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Kickstarter_Challenge.zip)

## Overview of Project

Louise is an up-and-coming playwright, whose recent first-ever crowdfunding campaign for her play *Fever* came close to reaching the $10,000 initially estimated goal. Despite not achieving her fundraising goal in a short amount of time, she wants to know how different campaigns fared in relation to their launch dates and their funding goals.  

This project's main purpose is to analyze the Kickstarter Campaign data in the attached excel file [Kickstarter_Challenge](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Kickstarter_Challenge.xlsx). The crowdfunding data will be further organized, sorted, and analyzed to determine whether there are specific factors that make a project's campaign successful.

## Analysis & Challenges
***Theater Outcomes vs Launch*** visualized in a marked line chart from a Pivot Table generated from "Sheet1" in [Kickstarter_Challenge](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Kickstarter_Challenge.xlsx):

![Theater_Outcomes_vs_Launch](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Theater_Outcomes_vs_Launch.png)

1. A pivot table created in the worksheet titled "Theater Outcomes by Launch Date" from "Sheet1"
    - filters on "Parent Category" and "Years"
      -  "Years" extracted from "Data Created Conversion" Column
    - "Parent Category" filtered on "theater" 
2. Campaign outcomes sorted descending order so "successful" is first
3. Line chart created showing number of successful, failed, or canceled projects by months

>*Difficulties encountered with analyzing Louise's requested data may be challenging in the conversion of the Unix timestampes in columns Deadline and Launched_at columns in Sheet1 to a readable format. The "Launch_At" and "Deadline" columns are represented in a Unix timestamp that much be converted into a readable format first before utilizing the `Years()` function.*

---
***The Outcomes vs Goals*** line chart showing the outcomes based on pledge goals:
![Outcomes_vs_Goals](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Outcomes_vs_Goals.png)

1. `COUNTIFS()` function populated the "Number Successful," "Number Failed," and "Number Canceled" columns by:
      - filtering on the [Kickstarter_Challenge](https://github.com/vzhang90/Kickstarter_Analysis/blob/main/Kickstarter_Challenge.xlsx) "outcome" column
      - "goal" amount column using ranges created from Column A
     - "subcategory" column using "plays" as criteria
2. `SUM()` function to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row
3. Percentage calculated of successful, failed and calceled projects for each row from "Total Projects," "Number Successful," "Number Failed," and "Number Canceled" columns
4. Line chart created visualizing the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis.

>*Difficulties encountered with analyzing Louise's requested data may be challenging in the `COUNTIFS()` function. Refer here for [help](https://support.microsoft.com/en-us/office/countifs-function-dda3dc6e-f74e-4aee-88bc-aa8c2a866842?ui=en-us&rs=en-us&ad=us)*

## Results

To help Louise better understand campaigns from start to finish, crowdfunding plays are created from a pivot table so that she can benefit from visualizing the outcomes of all categories. The graphical representation of the Pivot Table in "Theater Outcomes by Launch Date" worksheet give a closer look at how campaign length might be more specifically tied to its outcome. The line chart shows an increase in successful number of U.S. Theater crowdfunding campaigns in the months May. However, May, June, July, August, and October all had roughly the same number of failed campaigns launched.


Outcomes based on goals line chart shows an inverse relation between percentage successful and percentage failed. As the pledge goal amount becomes incrementally larger, the overall percentage successful decreases while the overall percentage failed increases.

Throughout analyzing this data set, it can be very limited in its lack of further trend analysis. With the two month surge in Successful Theater Outcomes by Launch Date, it would be highly recommended to further analyze the correlation between Outcomes and Years with T-tests. Visually, it would be highly recommended to included a correlation co-efficient and trend line associated with each legend. 
