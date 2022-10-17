# Kickstarting with Excel

## Overview of Project
Louise wanted to know how different campaigns fared in relation to their launch dates and their funding goals. My task was to use the KickStart Data Tables to visualize campaign outcomes based on their launch dates and their funding goals, and summarize results in a written report. 

Specifically, for this exercise there were two tables created. One to see the count of each outcome in the 'theater parent' category by month, the other to see the percentage of outcomes in the 'plays' subcategory.

### Purpose

## Analysis and Challenges


### Analysis of Outcomes Based on Launch Date

![Outcomes VS Launch](https://github.com/ahualoh/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

This was a pivot table and line chart created so that we can observe the outcomes of a campaign category over time, in partiular, this screenshot is displaying the 'theater' parent category (from all years).

Using the "pivot table" tool in excel, the table was created with the "parent cateogry" and "year" as filters, with the "date launched" as the rows, and outcomes as both the columns and values. The values are the count of each outcome. 

(The "Year" field was newly added to the original Kickstarter Data Table as a new column using the "YEAR" forumula)

### Analysis of Outcomes Based on Goals

![Outcomes VS Goals](https://github.com/ahualoh/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

This was table manually created so that we can observe the percentages of campaign outcomes compared by their goals. 

The data was generated using the COUNTIFS formula to produce respecitve outcome for each goal tier; those counts were summed, and then used to calculate their percentages of total campaign counts. 

This data table results in a line graph show the trends of failed and successful campaigns - how they performed compared to their goal tier. 

I added in cell A15 and A16 as well, a dynamic field that can be used to find the outcome of any other subcategory. 

### Challenges and Difficulties Encountered

#### Theater Outcomes Based on Launch
I did not encounter any challenges with this project. One only needed to be diligent about the field details - particularly the "Date Launched" field, since it gets broken up into three sub-fields. Which had the potential to be mixed up with the extracted "Year" field that was added to the data table. 

#### Outcomes vs Goals
This was a relatively straight-fowarded project as well, except that because there was so much manual data entry, it was easy to mistype. I made several typose that made producing the chart challenging (because the resulting data was incorrect)

- 1 My =COUNTIFS in B2 and B13 had the wrong number when defining those respecitive tiers (Less than 1000 was written as `=COUNTIFS(KickStarter!$D:$D,<100)`, and >5000 was written as `=COUNTIFS(KickStarter!$D:$D,>=500)`)
- 2 I referenced the wrong column in the original data table in my first COUNTIF condition... the "goals" column that I was supposed to reference was column D... but in my COUNTIF I originally referenced column E, which was "pledged" column
- 3 Not a mistake, I think... but just a note. I'm not certain if I could have done the "goal range" conditions a little differently, it just seemed redundant. 

## Results/Conclusions

- Two conclusions from "Theater Outcomes by Launch Date"
    - 1: May - July is the period when most successful campaigns were compelted.
    - 2: The trend patterns of successful and failed campaigns though, are similar. With the greatest difference in October.

- Conclusion from "Outcomes based on Goals"
    - The first and second tiers (<1000, and 1000-4999) have the most popular goal tier for successful plays.  

    After which, there is gradual drop-off of successful "Play" campaigns after the sixth tier (20000-24000). Past that tier, there are greater percetage of successful campaigns, but there are in general less campaigns at those higher tiers, so a greater change to swing fro one outcome to another. 


- Limitations of this dataset?
    - "Theater Outcomes by Launch Date"
    Sheer count of data doesn't necessarily give us information on the rates of sucess. Time of year is not a reliable factor when considering the outcomes of campaigns. Based on the trend lines, I was curious about what the percentages of each outcome was because each outcome seemed proportional for the most part. 

    - "Outcomes based on Goals"
    For Plays specifically, this data seems to have outliers when looking at the total number of projects for each tier. So the patterns of success/failure may not be reliable after a certain goal tier. 
    
- Other possible tables and/or graphs that we could create?
With such a large dataset, there seem to be endless tables and charts that could be created.... 
I might be curious to see a chart the data table with the Parent categories in the Y-axis and the count/percentage of each outcome in the X-axis. With the same axies, we may want to compare the averages goals/pledges of each category/subcategory of campaigns. We might also want to explore the duration of each campaign and see if we can find correclations to the campaigns' outcomes. 