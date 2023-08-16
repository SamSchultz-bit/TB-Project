# Group_Project_1
Repo for Group Project 1, Team 3

### Title: 
TB: The Curable Disease Still Killing Millions

### Team: 
Colin Vehmeier (cvehmei3r), Laura Bishop (TLCLauraB), Matthew Bond (Matthewbond12), Sam Schultz (SamSchultz-bit), Sha'miah Lindsey (ShamiahL)

### Description: 
Examine the data collected by the World Health Organization's Global Tuberculosis Report and search for trends. We will be using the collective data of 2021. What can a local community do to address this global concern?

### Research Questions:
    1) Is there a link between HDI and infection and mortality?
    2) What role does HIV infection play in TB infection and mortality?
    3) What role does multidrug-resistant TB play in infection?

### Data Sets: 
	* Tuberculosis Data Documentation: https://www.who.int/teams/global-tuberculosis-programme/data
	* Data Dictionary: https://extranet.who.int/tme/generateCSV.asp?ds=dictionary
 	* Infection/Mortality Rates(HIV): https://extranet.who.int/tme/generateCSV.asp?ds=estimates  
	* MDR: https://extranet.who.int/tme/generateCSV.asp?ds=outcomes
	* UN HDI: https://hdr.undp.org/data-center/documentation-and-downloads

## Our Project:

We chose to explore the data from the World Health Organization for their Tuberculosis Report in conjuntion with the United Nations' Human Development Index. We wanted to look at how infection and mortality rates are affected by development, HIV infection, and drug resistance. 

#### HDI SECTION
Steps to Generate Output:

In determining the relationship between HDI and TB Incidence and Mortality Rates, I began by using an inner join to merge two previously imported CSV files (one having HDI values by country and the other Incidence and Mortality Rates by country). I also had to rename the "country" series name to perform the join.

After performing the join and merging the datasets, I dropped unnecessary columns and renamed them to display only "Country", "HDI Value", "Incidence Rate per 100k", and "Mortality Rate per 100k".)

To better get a sense of how HDI score impacts Incidence and Mortality, I researched HDI and gleaned that there are different classifications via which countries are sorted. I then "binned" the HDI values using widely established HDI classifications: Very High, High, Medium and Low. I then added those data points as another series in my DataFrame.

Next, I determined that a boxplot displayed by HDI classification would be a great way to visualize the impact HDI has on TB/Mortality rates. I also plotted a scatterplot removing HDI classifcation and just using HDI values as the independent variable.

Finally, I generated code displaying both the correlation coefficient and r-squared to understand both the strength of the relationship between the two variables and understand how well HDI explains the variation in Incidence/Mortality Rates by country.

Summary Analysis:

Generating the box plots allows us to see that countries with very high HDI scores have very low mortality rates. All high and very high HDI countries have mortality rates below the median outcomes of both low and medium countries. We can also see that the spread of outcomes in both high and very high HDI countries are quite small with few countries varying much from their respective medians. We also note that, interestingly, countries with medium HDI scores have a VERY wide spread in terms of mortality rate outcomes, much moreso than even low HDI countries. 

Possible reasons for this could include: a greater international and NGO focus on low HDI countries vs. HDI countries. Another possible reason is national median age. Age, while not part of this analysis, is strongly correlated with TB incidence and mortality rate, and medium HDI countries could have higher spreads of median age, which could affect mortality outcomes. Medium HDI countries are also more geographically diverse than the other three groupings perhaps indicating genetic factors and/or cultural factors impacting incidence and mortality. 

The correlation coefficient for these two variables is -0.49 indicating a weak to relatively moderate relationship between the two variables. The r-squared was determined to be 0.24 indicating HDI, by itself, explains relatively little of the variation in TB mortality outcomes. The relationship between the two variables is relatively strong as you move through the development curve, but seems to hit a "speed bump" in medium HDI countries that when evaluating HDI alone cannot explain.


#### HIV
To explore the relationship between TB and HDI, I started by importing and creating data frames from the csv files. Then I dropped the unnecessary columns and renamed the remaining ones. 

My next step was to merge the two dataframes, find the upper and lower quartiles of the HDI index and seperate the countries into two dataframes. One each for the higher and lower quartiles.

To prepare the data I grouped all the countries in each dataframe by year, showing the mean value for each column. I also created calculated columns to get the Mortality Rates.

Finally, I created four plots showing the relationships between infection rates with and without HIV, Mortality Rates with and without HIV, and how cases and mortality compare in high and low HDI countries.

While people with HIV make up a small proportion of overall cases, if a person has both, they are much more likely to die.

Very much like Matt's previous findings, people in lesser developed countries are much worse off for both contracting and dying from TB. They are roughly 100 times more likely to do each. 

#### Drug Resistance
To explore the effect of MDR TB on infection and to draw conclusions surrounding the data, we imported a Rifampicin-resistance .csv file from WHO. Unnecessary colums were dropped and colums were renamed to clean the dataframe. 

Since percentages and totals for new cases were given but only percentages for reinfection cases, as well as no data for non-MDR cases, I used some algebra to generate columns in the dataframe pertaining to the number of reinfection cases as well as the total amount of TB cases.

I felt the best way to see the global impact of MDR TB was to separate by region given the limits of the dataset. This would show if certain  regions are more susceptible to MDR TB or if the effect is indescriminate of region. To do this, I used the .groupby() function to group by region and year and took the average of the reinfection rates and the new case rates for every year from 2015-2021 of every country. I used a 'for' loop I found on stackoverflow to produce two line charts that showed the new case rates and reinfection rates per region over time.  I also created a line plot that did not take region into consideration to show the relationship between new cases and reinfection cases.

My findings were that new rifampicin resistant cases were usually not determined by the region, with Europe being an outlier. According to the ECDC, Europe has failed to meet their Rifampicin Resistant TB treatment success goal for the years 2015-2020, and the age structure of Europe aligns with the most affected groups. The data also suggests that treatment is what is affected by resistant TB as opposed to spread. The recurrence rate globally sits around 17% while the new case rate is around 4%.

Sources for extra information:
https://www.ecdc.europa.eu/en/publications-data/tuberculosis-surveillance-and-monitoring-europe-2021-2019-data
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9998482/#:~:text=The%20incidence%20trends%20of%20MDR-TB%20in%20most%20regions,of%20MDR-TB%20%28p%20%3C%200.001%2C%20%CF%81%20%3D%20%E2%88%920.43%29.
https://www.visualcapitalist.com/mapped-the-median-age-of-every-continent/
https://www.nature.com/articles/ja2014107


### Task Leads:
	* Data Cleaning: Sam & Laura
	* Manage GitHub: Laura
	* Q1: Matt
	* Q2: Sam 
	* Q3: Colin	
	* Analysis: Sha'miah & Laura
	* Slides: Sha'miah & Laura

### Proposal:
https://docs.google.com/document/d/1rxHTi2pmAGjePYVj5ul5AofuYjhgOCADi2n8ihrXRwE/edit?usp=sharing

### Presentation Slides:
https://docs.google.com/presentation/d/1gw5XUOpP7Q4jWMe-F52-K1BJLG8zBt4tJTS5yVlEl9A/edit?usp=sharing
### Resource:
* Used to create multi-index line plots for drug resistance: https://stackoverflow.com/questions/44413020/how-to-specify-legend-position-in-matplotlib-in-graph-coordinates

* Henry, John Green: https://youtu.be/JhVJMO0wgTE 
