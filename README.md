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

- Analyzing the meaning of Null or NaN values in certain columns and rows in the dataset. For example, some columns such as *Mortality of TB cases who are HIV-positive, per 1000.000 population low bound* and *Mortality of TB cases who are HIV-positive, per 100 000 population, high bound* had many rows with null values, which is expected in a dataset composed mostly of numbers with a spatial distribution;

- Grouping the data dimensions into two relational hierarchies: (1) *Country/Territory or ISO Classification* which groups information from country/territory, region, ISO-2, and ISO-3 (abbreviations for classifying countries), and (2) *Methods to Derive Estimates* which groups the methods used to derive estimates of incidence, prevalence, mortality, and TBHIV (Tuberculosis with HIV incidence);

- Understanding the differences between various classifications presented in the dataset. For example, the difference between *latent TB* and *TB (active) disease*, *low-bound* and *high-bound*, and *ISO-2 country classification* and *ISO-3 country classification* which are described below:

  a) *latent-TB* is given to a person that has tuberculosis, but doesn't show up symptoms or spread the disease,
  
  b) *TB (active) disease* is given to a person that has the disease, can manifest its symptoms and can spread the disease,
  
  c) *TB (all forms)* include both *latent-TB* and *TB (active) disease*,
  
  d) *low-bound* and *high-bound*: these are mathematical values that are used to do estimations of numbers; so whereas a low-bound feature brings out the smallest value that would be rounded up to the estimated value, a high-bound would round up the smallest value that would be rounded up to the next estimated value. This means that the detection rate, for example, should stay between those 2 in order to be accurate and objective. As in the dataset we have the number of cases per 100,000 people and its stay between the low-bound and hig-bound, we will stick with the rate detection estimation numbers,
  
  e) *ISO-2* and *ISO-3* are numerical international codes used to designate every country/territory like an acronomy by using a 2 letter (ISO-2) or 3 letters combination (ISO-3) that designates a especific region or country.

- Updating some geographical regions/countries which were not accepted by Tableau:

  a) For Serbia & Montenegro, the latitude 44.8166634 and longitude 20.4666648 were added. It's worth noting saying that Serbia & Montenegro was a country in Southeast Europe formed from the two remaining republics of Yugoslavia after its breakup in 1991. 

  b) For Netherlands Antilles, the latitude 12.226079 and longitude -69.060087 were added. The Netherlands Antilles was a constituent country of the Kingdom of the Netherlands consisting of several island territories located in the Caribbean Sea. Informally known as the Dutch Antilles, the country emerged in 1954 as the autonomous successor of the Dutch colony of Curaçao and Dependencies.
  
  c) For West Bank and Gaza Strip, the location was left unchanged as it is a Palestinian territory and accurate latitude and longitude could not be found to update. it.

These actions helped me to gain a deeper understanding of the data, its structure, and the information it contains, which was crucial for conducting meaningful analysis and drawing accurate conclusions.


### Step 3: Exploring the dataset with different visualizations
This step involved exploring the dataset with different visualizations. Twelve visualizations are described in this step:

3.1 A map called "Tuberculosis around the Globe" show the mortality rate of TB (with and without considering HIV), the detection rate of TB, and the total population of each country.

3.2 A line graph called "TB Detection Average Rate per Year" displays the average rate of TB detection per year and region/country based on high-bound, low-bound, and general estimates.

3.3 A line graph called "TB Count per Region and Year" depicts the count of TB cases over time, with one line for each region.

3.4 A horizontal bar chart called "TB Detection Rate x TB Mortality Rate per Region and Country" compares the TB detection rate (including and excluding HIV cases) and TB mortality per country.

3.5 Two line graphs, "TB Detection Rate per Year, Region and Country" and "TB Prevalence Rate per Year, Region and Country", show the evolution of TB detection rate and TB prevalence rate in different regions and countries, and can be viewed individually in the dashboard.

3.6 A two-part area graph called "Number of Deaths of TB per Year, Region and Country" compares the number of TB deaths including and excluding HIV cases per region and country over the years.

3.7 A line graph named "Incidence of TB Cases Including HIV" shows the incidence rate of TB with consideration of the HIV group as an important variable.

3.8 A split line graph called "Forecast of Incidence of TB Cases until 2015" compares the incidence rate of TB between two groups, one including and one excluding HIV, since 1990 and forecasted until 2025. The forecast was based on the region and its population estimate, considering a 95% confidence interval and adding 12 years to the last year of the dataset.

3.9 A treemap graph called "TB Mortality Rate, +HIV and Methods to Detect the Mortality Rate" displays the 3 methods used to detect TB mortality, with Indirect being the most commonly used method.

3.10 Another treemap graph named "Methods to Derive Prevalence of TB x TB Prevalence Rate" shows the 5 methods used to detect the prevalence of TB and the TB prevalence rate, with survey imputed being one of the most used methods across countries.

3.11 Additionally, there are two regression model graphs: a linear regression model named "TB Regression Model (Number of Deaths, + HIV x TB Detection Rate" and another one named "TB Linear Regression Model (Number of Deaths, -HIV x TB Detection Rate)". The first model includes the group with HIV and the second excludes it from the model.


### Step 4: Analyzing the features of the dataset to consider the ones with more statistical significance
In the analysis of the dataset, certain features were found to be more significant for the prediction model than others. These include the country or territory name for understanding the distribution of data and potential patterns between countries, the year to show the evolution of TB detection and mortality over time, and the region to see the count of TB cases per region and year. The region feature was particularly relevant when combined with the year feature. The analysis showed that Europe had the highest count, Africa and America had a similar count that intertwined with each other, and Southeast Asia had the lowest count over the years.

While the dataset has been exploring, some of the 47 different features showed to be more significative than others to our prediction model, such as:
   
  
   
   - Year: this feature is important as it can point out the evolution of the TB detection and TB mortality per year despicting a trajectory of the disease;
   
   - Region: this feature is also relevant especially if combined with the *year* feature. For example, it is relevant to see the TB count per region and year together. From one of our line graphs, it was possible to analyze the count of TB cases per region in descending order:
    
    1 EUR (Europe), 
    2 AFR (Africa), 
    3 AMR (America),
    4 WPR (Western Pacific Region), 
    5 EMR (Eastern Mediterranean Region),
    6 SEA (Southeast Asia)

*Where Europe has the highest count, Africa and America regions have a similar count as their lines intertwin each other and Southeast Asia has the lowest count throught the years*.
    
    
    - Estimated total population number
    - Estimated prevalence of TB (all forms) per 100 000 population
    - Estimated prevalence of TB (all forms)
    - Method to derive prevalence estimates
    - Estimated number of deaths from TB (all forms, excluding HIV)
    - Method to derive mortality estimates
    - Case detection rate (all forms), percent


### Step 5: Retaking the most significative visualizations done in step 3 to analyze some patterns, trends and keypoints of the dataset to create the dashboard
From those visualizations, some questions popped up, such as:
  - *Is there a correlation between TB detection rate and TB number of deaths? In other words, are the countries with a higher TB detection rate the ones with less number of deaths of TB? And are the countries with lower TB detection rate the ones with a higher number of TB deaths?*
  - *Is there a correlation between TB mortality rate and HIV?* 
  - *Is there a correlation between TB mortality and other diseases?*

With those questions in mind, this is the moment that the dashboard was created. 




## Results
One of the *United Nations Sustainable Development Goals (SDGs)* is to put an end in the TB epidemic by the year of 2030. 


By examining the correlation between the rate of TB detection and the decline in the number of deaths, the project aims to shed light on whether the methods used to estimate mortality in countries are contributing to the global decline of the disease. This objective is relevant and meaningful as it can provide important insights into the effectiveness of TB control and prevention efforts.

These visualizations aim to explore different aspects of the tuberculosis data and present them in a clear and concise way. The maps, line graphs, horizontal bar chart and area graphs provide a comprehensive understanding of the rate of detection, mortality, prevalence, and number of deaths due to TB over time, across regions and countries. The use of different visualization types (map, line graphs, bar chart and area graph) helps to highlight specific trends and patterns, making it easier to understand and analyze the data.


Aggregation of results

A treemap graph called "TB Mortality Rate, +HIV and Methods to Detect the Mortality Rate" shows case the 3 methods used to detect the mortality of TB, such as: Indirect, VR and VR Imputed as the first one being most used.

s titled "TB Detection Rate by Year". The first visualization was a graph about the tuberculosis data evolution by year in the world. Similarly, this graph is divided into 3 big rows: the first shows the detection rate percent in a whole, the second, the detection rate low bound, and the third, the detection rate high bound. By analyzing those lines, you can notice that the TB case detections in all forms (LTBI and TB disease) has a constant rate by year: the graph line is mostly high and stable (constant), and points out only small variations. Also, the 3 lines, which start in 1990 and finish in 2012, show their first small peak in 2003 and, after, in 2011. 



3.10 Another treemap named "Methods to Derive Prevalence of TB x TB Prevalence Rate" shows 5 methods used to detect the prevalence of TB x the TB prevalence rate, such as: NTP, pooled surveys, predicted, survey and survey imputed, whereas the survey imputed appears as one of the most used considering the whole countries. 

3.6 More two graphs called "Methods to Derive Mortality of TB x Mortality Rate of TB" and "Methods to Derive Prevalence of TB x Prevalence Rate of TB". In the first, we can see that the "indirect" method is the most used but still the least effective as it doesn't impact in the decline of the mortality rate of TB. In the second, the method most used to detect the prevalence of TB is survey which can correlate positively with the detection of the prevalence rate of TB.

Important to nothe that both models have a high R-square value , so the model explains a lot about the number of deaths from the disease. However, a note about it is important to be mentioned: as this model describes a constant line between the detection rate of TB and number of deaths of TB, this means that althought there is a better rate of detecting the disease nowadays, tuberculosis is still a disease that has been killing lots of people. 



## Challenges 
The following challenges were encountered during the analysis:

- The lack of information on tuberculosis count by age, gender, and children in the dataset limited the analysis of tuberculosis incidence and mortality rate. The only available information was the count by country and year, and the impact of HIV/AIDS on tuberculosis;

- When trying to match significant map graphs, the legend and filter mismatch caused the need to explore each graph on separate sheets everytime the dashboard was updated;

- The geographical data had missing places which caused the dashboard map, a crucial tool for visualizing the dataset's distribution and spread, to malfunction at times. A temporary solution was to add a fixed map under the dynamic map to prevent blank spaces. A permanent solution will be found in the future;

- The dataset did not have any information on the correlation between TB mortality rates and immuno-deficient groups of people, making it impossible to answer one of the questions that came up during the exploratory data analysis (EDA) (*Is there a correlation between TB mortality rate with diseases that cause immuno-deficiency?*).


## Future Goals
(what would you do if you had more time?)


## References
ALL ACRONYMS. https://www.allacronyms.com/

CDC. https://www.cdc.gov/tb/topic/basics/default.htm

Nations online. https://www.nationsonline.org/oneworld/country_code_list.htm

WHO. https://www.who.int/news-room/fact-sheets/detail/tuberculosis
