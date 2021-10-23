### Analyzing Kickstarter campaigns with Excel
Analysis of Kickstarter campaign data to determine the optimal funding strategy for a theater & musical project in the U.S. and UK

## Overview of Project
Project analysis was based on a Kickstarter dataset of more than 4,000 funding campaigns, with the goal of determining the impact of launch time and funding goal on the campaigns' success. 

## Purpose
Help the client determine the optimal funding amount and timeline to successfully launch a new theater project

## **Findings**

* The Kickstarter data set illustrated the competitive nature of funding for arts and cultural project: across the U.S., out of a total of more than 3,000 campaigns, only a little over half were successfully funded, while around 45% of campaigns were either canceled or failed
* Results across all campaign categories in the UK showed a more favorable funding landscape, with 60% of all campaigns were successfully financed
* Across both counties, theater campaigns were shown to be the most popular funding category, vastly outstripping other categories

*U.S. Category Outcomes*

<img src="https://user-images.githubusercontent.com/90064437/138205061-79d352ec-21de-458a-8cd7-36673b0bfcf4.png" width="500" height="">


*UK Category Outcomes*

<img src="https://user-images.githubusercontent.com/90064437/138203543-b94497ca-b2c8-433f-b246-028cde6a4dea.png" width="500" height="">

# **Analysis and Challenges**

The client wanted to explore the correlation between funding launch dates and the outcome for theater campaigns across the entire dataset of more than 1,360 theater campaigns. Illustration of the outcomes was done via pivot table, allowing the client to filter by campaign launch year. To do so, we first had to separate the year from the full launch date using Excel's `YEAR()` function.

The second analysis the client wanted us to perform was the campaign outcome for plays based on total funding goals to determine whether the amount of targeted funding impacted the campaign's outcome. To allow Excel to count individual outcomes we used the program's `COUNTIFS()` function. This allows us to determine specific parameters according to which Excel filters the data to count.

### Analysis of Outcomes based on Launch Date

<img src="https://user-images.githubusercontent.com/90064437/138573095-ecb85645-86eb-42fb-ac6e-83ae0e0ca837.png" width="500" height="">
     
### Analysis of Outcomes Based on Goals

<img src="https://user-images.githubusercontent.com/90064437/138573323-794b5b94-d7dc-41d8-860b-55ca4f628cc6.png" width="500" height="">

    
### Challenges and Difficulties Encountered

The challenge in completing the pivot table consisted of sorting the outcome data into both the 'Columns' and 'Values' area. Challenges also could have arisen in sorting the pivot table for the 'Date Created Conversion' in 'Rows'. Because the client was most interested in the impact of a particular month on the campaign's outcome, we had to drop Excel's selection of 'Year' and 'Quarter' from the 'Row' area of the pivot table.

The challenge in analyzing outcomes based on goals was in using the `COUNTIFS()` function in Excel. I did not immediately understand how the function works and intially employed filters on my main Kickstarter data. But I quickly realized that the `COUNTIFS()` function disregards manual filters and instead looks at all the data in the dataset as if filters were not set. Once I understood that `COUNTIFS()` is smarter than I originally gave it credit for, I could simply tell it to look up the desired values on its own, and could simply copy and paste the command across all rows, each time simply modifying one of the parameters without having to retype the entire function.

# **Results**

*What are two conclusions you can draw about the Outcomes based on Launch Date?*

Filtering for theater campaigns, the analysis clearly showed the highest level of success during the late spring and summer. Success levels dropped off steeply beginning in October, reaching their lowest level in December. But campaign launches overall decreased during the winter months. Overall, the greatest amount of campaigns were launched in May - the month that also marked the highest level of successful campaigns. Based on the data analyzed, we would recommend launching a theater Kickstarter campaign in May.

*What can you conclude about the Outcomes based on Goals?*

Looking at how campaign outcomes for theater plays correlate with their funding goal we found that cheaper campaigns with funding targets of below $1,000 showed the highest level of success. More than three quarters of those low-cost campaigns were completed successfully. Campaigns targeting a funding range of between $45,000 and $49,999, as well as between $25,000 and $29,999 showed the lowest likelihood of success, with none or only 20% of those campaigns, respectively, concluding successfully. Interestingly enough, the dataset showed that campaigns targeting funding of between $35,000 and $44,999 showed a sudden uptick in success rates at 67%. More qualitative analysis is needed to understand that unexpected success rate.

Based on our analysis, we would recommend a target funding range of below $5,000, or between $35,000 and $44,999 for the highest likelihood of success.

*What are some limitations of this dataset?*

The data is fairly old, with 2017 being the last year for which we have data available. The data is also unequally distributed across the years. While there is hardly any data from 2009 through 2014 and for 2017, the bulk of the data is made up from years 2014, 2015 and 2016. Without a qualitative analysis we do not know whether those years were off-years for Kickstarter funding. 

Moreoever, we have little qualitative data to exclude other causes for the successful outcome of a play. Rather than simply the months or amount of funding, other parameters (such as the topic of the play; the director; the actors, etc) could influence donors' willingness to fund a campaign.

*What are some other possible tables and/or graphs that we could create?*

We could sort our Outcomes based on Launch Date pivot table by country to determine which country is the most generous in donating to theater Kickstarter campiagns. We could also look at Outcomes based on Goals across a variety of categories other than plays to determine whether particular categories are more or less popular and show fewer failed campaigns regardless of funding target.




