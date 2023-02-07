# Final Project with Tableau


## Introduction and Goals
Tuberculosis (TB) is not a disease from the past: although it was discovered in 1988, the whole world did not reach the milestone of 0% tuberculosis patients or 0% in the death toll. Fortunately, this context can be changed as tuberculosis can be cured and prevented. According with the *World Health Organization*, a total of 1.6 million people died from tuberculosis in 2021. It is the 13th leading cause of death worldwide, and the 2nd leading killer infectious disease after COVID-19, affecting people of all ages and countries.

TB is indeed a global health issue and it is caused by the bacterium *Mycobacterium tuberculosis* and primarily affects the lungs, but can also impact other parts of the body such as the kidney, spine, uterus, and brain. Not everyone infected with the TB bacteria becomes sick, leading to two conditions: latent TB infection and TB disease. If left untreated, TB disease can be fatal.

In this project, you will read the analyses and visualizations experimented from the tuberculosis dataset, which provides information on TB incidence, cases, and mortality rates by country and year from 1990 to 2013. The dataset is a .csv file containing 47 fields and 5120 rows, and while the information is based on estimates, it provides valuable insights into the future possibilities of TB burden and control efforts. 

Also, this project has the purpose to dive deeper in the (alternative) hypothesis that there is a correlation between the rate of detection of TB with the decline of the number of deaths as this correlation could  shed more light if the methods to derive mortality estimates in the countries are being used to promote the decline of the disease in the world.


## Process
The project process, in an overwall way, followed the steps below:

### Step 1: Connecting the dataset about tuberculosis count by country with Tableau
At this step, the dataset, which is a .csv file composed of only one physical table called *TB_Burden_Country*, was downloaded and connected as the data source in *Tableau Public*. This step was followed by EDA which is described in the next step.


### Setp 2: Checking different data types, columns and rows in the data set
This step of the project describes the initial exploratory data analysis (EDA) of the tuberculosis dataset. It outlines some specific actions taken during this EDA, such as:

- Checking and updating the data types of each column in the dataset. For example, the data type of the "Region" column was updated to "Country/Region" to reflect its geographical role;

- Updating the names of columns to make them more concise and readable. This involved removing expressions from the column titles, such as the word "estimated." This change was made because all the columns in the dataset contain only estimated numbers due to the geographical nature of the data, and there are no absolute measurements.

These actions helped me to prepare the data for further analysis and ensure that it is organized and easily understood.

After that initial EDA, other steps were done to further explore the data in the tuberculosis dataset to gain a better understanding of its contents. The actions taken include:

- Understanding the meaning of Null or NaN values in certain columns and rows in the dataset. For example, some columns such as *Mortality of TB cases who are HIV-positive, per 1000.000 population low bound* and *Mortality of TB cases who are HIV-positive, per 100 000 population, high bound* had many rows with null values, which is expected in a dataset composed mostly of numbers with a spatial distribution;

- Grouping the data dimensions into two relational hierarchies: (1) *Country/Territory or ISO Classification* which groups information from country/territory, region, ISO-2, and ISO-3 (abbreviations for classifying countries), and (2) *Methods to Derive Estimates* which groups the methods used to derive estimates of incidence, prevalence, mortality, and TBHIV (Tuberculosis with HIV incidence);

- Understanding the differences between various classifications presented in the dataset. For example, the difference between *latent TB* and *TB (active) disease*, *low-bound* and *high-bound*, and *ISO-2 country classification* and *ISO-3 country classification* which are described below:

  a) *latent-TB* is given to a person that has tuberculosis, but doesn't show up symptoms or spread the disease,
  
  b) *TB (active) disease* is given to a person that has the disease, can manifest its symptoms and can spread the disease,
  
  c) *TB (all forms)* include both *latent-TB* and *TB (active) disease*,
  
  c) *low-bound* and *high-bound*: these are mathematical values that are used to do estimations of numbers; so whereas a low-bound feature brings out the smallest value that would be rounded up to the estimated value, a high-bound would round up the smallest value that would be rounded up to the next estimated value. This means that the detection rate, for example, should stay between those 2 in order to be accurate and objective. As in the dataset we have the number of cases per 100,000 people and its stay between the low-bound and hig-bound, we will stick with the rate detection estimation numbers,
  
  c) *ISO-2* and *ISO-3* are numerical international codes used to designate every country/territory like an acronomy by using a 2 letter (ISO-2) or 3 letters combination (ISO-3) that designates a especific region or country.

- Updating some geographical regions/countries which were not accepted by Tableau:

  a) For Serbia & Montenegro, the latitude 44.8166634 and longitude 20.4666648 were added. It's worth noting saying that Serbia & Montenegro was a country in Southeast Europe formed from the two remaining republics of Yugoslavia after its breakup in 1991. 

  b) For Netherlands Antilles, the latitude 12.226079 and longitude -69.060087 were added. The Netherlands Antilles was a constituent country of the Kingdom of the Netherlands consisting of several island territories located in the Caribbean Sea. Informally known as the Dutch Antilles, the country emerged in 1954 as the autonomous successor of the Dutch colony of Curaçao and Dependencies.
  
  c) For West Bank and Gaza Strip, the location was left unchanged as it is a Palestinian territory and accurate latitude and longitude could not be found to update. it.

These actions helped me to gain a deeper understanding of the data, its structure, and the information it contains, which was crucial for conducting meaningful analysis and drawing accurate conclusions.


### Step 3: Exploring the dataset with different visualizations 
During this step, the following visualizations were done:

- 3.1 The first graph used to explore this dataset is titled "TB Detection Rate by Year". The first visualization was a graph about the tuberculosis data evolution by year in the world. Similarly, this graph is divided into 3 big rows: the first shows the detection rate percent in a whole, the second, the detection rate low bound, and the third, the detection rate high bound. By analyzing those lines, you can notice that the TB case detections in all forms (LTBI and TB disease) has a constant rate by year: the graph line is mostly high and stable (constant), and points out only small variations. Also, the 3 lines, which start in 1990 and finish in 2012, show their first small peak in 2003 and, after, in 2011. 

- 3.2 The second line graph called "TB Count per Region and Year"

- 3.3 The third and fourth graphs, titled "TB Detection Rate By Country", "TB Mortality Rate by Country" and "TB Number of Deaths per 1000,000 population" were plotted as maps. 

- 3.4 There were two line graphs called "TB Number of Deaths Excluding HIV (Forecast 1)" and "TB Number of Deaths Including HIV (Forecast 2)" were done to perform some forecast of the number of TB deaths by including and excluding HIV. They were both created with a filter by region and its population estimative, considering a 95% of confidence interval and with the addition of 10 years from the last year of the dataset (the forecast was done from 2012 until 2022).

- 3.5 A vertical table called "Prevalence of TB" 

- 3.6 More two graphs called "Methods to Derive Mortality of TB x Mortality Rate of TB" and "Methods to Derive Prevalence of TB x Prevalence Rate of TB". In the first, we can see that the "indirect" method is the most used but still the least effective as it doesn't impact in the decline of the mortality rate of TB. In the second, the method most used to detect the prevalence of TB is survey which can correlate positively with the detection of the prevalence rate of TB.

- 3.6 Another graph called "TB Regression Model (Number of Deaths from TB x TB Detection Rate)" is done to visualize if there is a relationship between the detection rate of tuberculosis with the number of deaths. This model has a high R-square value  euals to 1, so the model explains a lot about the number of deaths from the disease. However, a note about it is important to be mentioned: as this model describes a constant line between the detection rate of TB and number of deaths of TB, this means that althought there is a better rate of detecting the disease nowadays, tuberculosis is still a disease that has been killing lots of people. 



### Step 4: Analyzing the features of the dataset to consider the ones with more statistical significance
While the dataset has been exploring, some of the 47 different features showed to be more significative than others to our prediction model, such as:
   
   - Country or territory name: spatial data can help us to understand how our data has been distributed and, therefore, what are some patters between them,
   - Year: this feature is important as it can point out the evolution of the TB detection and TB mortality by year;
   - Region: this feature is also relevant especially if combined with the "year" feature: in other words, it is interesting to see the TB count per region and year together. From our line graph, we could see that this is the descending order of TB count per region:
    
    - EUR (Europe), 
    - AFR (Africa), 
    - AMR (America),
    - WPR (Western Pacific Region), 
    - EMR (Eastern Mediterranean Region),
    - SEA (Southeast Asia)
*Where Europe has the highest count, Africa and America regions have a similar count as their lines intertwin each other and Southeast Asia has the lowest count throught the years*.
    
    
    - Estimated total population number
    - Estimated prevalence of TB (all forms) per 100 000 population
    - Estimated prevalence of TB (all forms)
    - Method to derive prevalence estimates
    - Estimated number of deaths from TB (all forms, excluding HIV)
    - Method to derive mortality estimates
    - Case detection rate (all forms), percent


### Step 5: Retaking the most significative visualizations done in step 3 to analyze some patterns, trends and keypoints of the dataset
From those visualizations, some questions popped up, such as:
  - *Is there a correlation between TB detection rate and TB number of deaths? In other words, are the countries with a higher TB detection rate the ones with less number of deaths of TB? And are the countries with lower TB detection rate the ones with a higher number of TB deaths?*
  - *Is there a correlation between TB mortality rate and HIV?* 
  - *Is there a correlation between TB mortality and other diseases?*



### Step 6: Creating the dashboard
With those questions in mind, this is the moment that the dashboard was created. 




## Results
One of the *United Nations Sustainable Development Goals (SDGs)* is to put an end in the TB epidemic by the year of 2030. 

By examining the correlation between the rate of TB detection and the decline in the number of deaths, the project aims to shed light on whether the methods used to estimate mortality in countries are contributing to the global decline of the disease. This objective is relevant and meaningful as it can provide important insights into the effectiveness of TB control and prevention efforts.

(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)

Aggregation of results



## Challenges 
Some of the challenges are descibed below:
- The dataset doesn't describe the information of TB count by age or different groups (e.g., male, female and children). As it only references the count by country and year with some columns bringing out the information by HIV/AIDS relationship, I found that the lacking of people segmentation impacted the analysis as it couldn't give us a better picture of the tuberculosis incidence and mortality rate;
- To match map graphs that were significative together, but as the legend wouldn't match both of them, I had to explory each one in different sheets;
- As I am working with geographical data, some places are not represented in the map, therefore the map of the dashboard which is one of the most important pieces of information fo visualiza the distribution and spread of the dataset, can stop working sometimes. So as a temporary solution, I added a fixed map under the dynamic map so there will not display a blanck space. In the future, I will find a solution for that. 
- One of the questions popped up during the EDA was not possible to be addressed as there was no feature in the dataset about if there is a correlation between the TB mortality rates with immuno-defficiency groups of people.


## Future Goals
(what would you do if you had more time?)


## References
ALL ACRONYMS. https://www.allacronyms.com/

CDC. https://www.cdc.gov/tb/topic/basics/default.htm

Nations online. https://www.nationsonline.org/oneworld/country_code_list.htm

WHO. https://www.who.int/news-room/fact-sheets/detail/tuberculosis
