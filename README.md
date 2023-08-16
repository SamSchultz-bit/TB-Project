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

#### HIV
To explore the relationship between TB and HDI, I started by importing and creating data frames from the csv files. Then I dropped the unnecessary columns and renamed the remaining ones. 

My next step was to merge the two dataframes, find the upper and lower quartiles of the HDI index and seperate the countries into two dataframes. One each for the higher and lower quartiles.

To prepare the data I grouped all the countries in each dataframe by year, showing the mean value for each column. I also created calculated columns to get the Mortality Raates.

Finally, I created four plots showing the relationships between infection rates with and without HIV, Mortality Rates with and without HIV, and how cases and mortality compare in high and low HDI countries.

While people with HIV make up a small proportion of overall cases, if a person has both, they are much more likely to die.

Very much like Matt's previous findings, people in lesser developed countries are much worse off for both contracting and dying from TB. They are roughly 100 times more likely to do each. 

#### Drug Resistance



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
https://stackoverflow.com/questions/44413020/how-to-specify-legend-position-in-matplotlib-in-graph-coordinates > used to create multi-index line plots for drug resistance
