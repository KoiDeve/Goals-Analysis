# Goals-Analysis
 
This project was created in order to notice any patterns, trends, or other interesting factors that can explain my progress in achieving my current goals for the year. In this project, we will be exploring a data set that I have created for myself that records each goal and when I do it for the day, as well as my thoughts behind it. The original data set was taken from google sheets, and later converted into a Pandas dataframe in Jupyter notebook. A quick visualization can be seen here:

![alt text](https://github.com/KoiDeve/Goals-Analysis/blob/main/Screenshots/02_original_data_comparison.PNG?raw=true)

As can be seen in the visualization, we will be focusing on the gray data (not the purple), which lists all of my goals for this year. In addition, I have cleaned the data and converted all of the T/F data into ones and zeroes respectively. An example of the clean data can be seen below:

![alt text](https://github.com/KoiDeve/Goals-Analysis/blob/main/Screenshots/03_cleaned_data.PNG?raw=true)

Much better! This will allow greater ease in plotting and using this data. The following columns, or goals, are described below:

- DAY: The day that the goals were recorded
- WOUT: This goal is considered a '1', or 'complete' when I do a workout greater than 30 minutes for the day.
- INIT: This goal is considered a '1' when I am start/plan/research a new course of action.
- DUO1: This goal is considered a '1' when I do a 10-minute lesson to learn another language.
- DUO2: This goal is considered a '1' when I do another 10-minute lesson.
- DANCE: This goal is considered a '1' when I do a 15-minute dance session, or a 15-minute streth session.
- PORTF: This goal is considered a '1' when I work on a personal software project.
- JOURN: This goal is considered a '1' when I write in a journal about my day.
- BED: This goal is considered a '1' when I go to bed on time.

Now that we have a better understanding of the data, we can look at some visualizations that I have created to better describe the data. Let's look at the first chart:

![alt text](https://github.com/KoiDeve/Goals-Analysis/blob/main/Screenshots/04_da_cumulative.PNG?raw=true)

As we can see, this chart takes the total amount of times I did a task (or goal), and plot the total frequency of it throughout time. The data ranges from mid-april to the end of September, and that the ideal for each of these goals can be visualized along the line y = x.

An important thing I noticed when I first created this graph was that a lot of these goals weren't actually even started until the middle of May, so what I've decided to do was reduce the data set to the date range of 5/20/23 - 8/31/23. From here, I decided to create a correlation chart to see if there were any patterns with the goals that I have set for myself:

![alt text](https://github.com/KoiDeve/Goals-Analysis/blob/main/Screenshots/05_da_correlation.PNG?raw=true)

This chart is interesting, because it measures the correlation on a scale of -1.0 to 1.0 between each goal. The most notable piece of information here is that the journaling category "JOURN" is moderately correlated with most of the other goals that are in this data set. This can be interprited as either two things:

1. Every time I journal, the chances that I do other goals will go up
2. If I don't do the goals for the day, the chance I will journal goes down 

These two hypothesis are based upon the completion order of the tasks, which is dependant upon the time of the journal entry. I'll elaborate more later.

Another measurement that I wanted to take into account is the consistency of the goals that I am setting for myself. To calculate this, I decided to create a 5-day average of the amount of goals (tasks) completed. The visualization can be seen below:

![alt text](https://github.com/KoiDeve/Goals-Analysis/blob/main/Screenshots/06_da_average.PNG?raw=true)

This chart shows the average amount of tasks completed in the last 5 days. An example for context would be at 06/01/23 (the "June" label seen in the chart), on average from the last 5 days (so in this case, it would be the average of tasks completed for the day from May 28th to June 1st. The reason why I scaled it up to five days is due to the lack of consistency if it were to be seen from the daily perspective. One thing I noticed from this chart is that overall I have never had an instance where I completed on average 7 tasks a day for 5 days straight, meaning that there isn't a sufficient consistency towards me completing my goals. In order to take a better look, I decided to do the same analysis, but on the individual goals themselves. See below:

![alt text](https://github.com/KoiDeve/Goals-Analysis/blob/main/Screenshots/07_da_average_indiv.PNG?raw=true)

As we can see here we are able to see on an individual level of the frequency of completion for 5-day periods. Some things we can note while looking at this is that any instances of jagged behaviour can be seen as inconsistent completion, and any instance of slow transitions can indicate more consistent behaviour. For example, "DUO1" has mostly consistent behaviour with the exception of an instance right before August. "BED" has the same consistent behaviour, in the case that I am consistently not going to bed on time. The ones that strike me the most insteresting are the "READ" and "JOURNAL" ones, which seem to be inconsistent in several mannerisms.

Overall, this was a really interesting project. Based on the information here I determined that these would be the possible next steps for me to do personally:
- Prioritize journaling. For the next 4 months (September - December), I plan on achieving a consistent journaling frequency of 70% for each month. 
- Set a new goal to try to sleep on time for 5 days consecutively.
- Establish a general routine for one task (in this case, I plan on completing DUO1 at 9:00AM every day).

As for the next steps for this project, I have several ideas in mind for the future:
- Increase the data set to incorporate times of completion for each task.
- Feeding this data into Chat-GPT using an OpenAI API to get a better understanding of the data (I originally tried this, but got vague results since the model wasn't fine-tuned to my specific needs).

This is the end of the report for now. I'll create an update to this soon once I curate more data. Thank you for reading! 
