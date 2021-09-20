# Kickstarting with Excel

## Overview of Project
This analysis is of select Kickstarter campaigns started from May 2009 through March 2017 and includes:

* Theater outcomes based on the launch date
* Play outcomes based on goals

### Purpose
This analysis is to help Loise with her current project campaign by examining the timing and funding of similar projects on Kickstarter.

## Analysis and Challenges
The sub-sections below outline how this analysis was performed, challenges encountered, results, the limitations of those results, and options for future analysis. 

### Analysis of Outcomes Based on Launch Date
Analysis of theater outcomes based on the launch date was performed by: 
1. Adding the Year column and populating it by extracting the year from the Date Created Conversion column for each Kickstarter project
2. Creating a pivot table that displays the outcomes by month and can be filtered by Parent Category and Year
3. Removing Live projects
4. Filtering to show only Theater campigns
5. Ordered Outcomes so successful was first
6. Created a line chart visualization of the results
![Kickstarter theater project outcomes comparted to their launch date](https://myoctocat.com/assets/images/base-octocat.svg)

### Analysis of Outcomes Based on Goals
Analysis of play outcomes based on goals was performed by:
1. Sorting the Kickstarter projects by the amount of the goal and thier outcome
2. Verifying that the total projects matched the amount in the data set
3. Caluculating the percentage of each goal range that was successful, failed, or was canceled
4. Creating a line chart visualiztion of hte results
![Kickstarter play project outcomes based on goals](https://myoctocat.com/assets/images/base-octocat.svg)

### Challenges and Difficulties Encountered
The initial formuals I used to pull the counts of plays in each goal range did not count everything in the data set. Once the formulas were adjusted to include >= for the lowest number in the group and > the number starting the next group then all of the projects in the data set were counted. For example "=COUNTIFS(Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays", Kickstarter!$D:$D, ">=1000", Kickstarter!$D:$D, "<5000")"

## Results

Theater Kickstarters are launched throughout the year. May is when the highest number of projects launched and has a slightly higher percentage of successful projects. December is the least popular month to launch a theater project. 

The majority of plays have a goal of less than $5000, 720 plays were under $5000 while 327 had a goal of $5000 or higher. Plays with a goal of $5000 or higher had a lower success rate than plays with a goal of less than $5000. For plays under $5000, the success rate was 76% and 73%. For plays with a goal higher than $5000, the success rate ranged from 0% to 67%.  

This data set only includes projects that raised money through Kickstarter. Further analysis could combine information from other crowd funding platforms like indigogo or seedinvest. 

Additional analysis could include comparing the length of the campaign to the outcomes to see if there is a relationship between the success or failure and how many months the campaign is active. We could also analyze the outcomes by country to help determine where future projects have a better channce to succeed. Another option would be to further refine the analysis of outcomes based on launch date to only include results for the sub category plays. 