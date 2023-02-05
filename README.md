# Final Project with Tableau


## Project/Goals
Tuberculosis is not a disease of the past: although it was discovered in 1988, the whole world did not reach the milestone of 0% tuberculosis patients. Fortunately, it can be cured and prevented. According with the *World Health Organization*, a total of 1.6 million people died from tuberculosis in 2021. Ranked as the 13th leading cause of worldwide death and as the 2nd leading killer infectious after COVID-19 (above HIV/AIDS), tuberculosis (TB) is present in all countries and age groups. One of the *United Nations Sustainable Development Goals (SDGs)* is to put an end in the TB epidemic by the year of 2030. 
Tuberculosis (TB) is caused by a bacterium called *Mycobacterium tuberculosis*. This bacteria attacks mostly the lungs, but it can also attack other parts or organs of the body such as the kidney, spine, uterus, and brain. It is important to note that not everyone infected with the TB bacteria becomes sick. As a result, there are two TB-related conditions: (1) latent TB infection (LTBI) and (2) TB disease. If not treated properly, TB disease can be fatal.
In this project, you will find the analysis and visualizations experimented from a Tuberculosis dataset given by country. The dataset is a .csv file composed of one physical table called *TB_Burden_Country* and it has 47 fields or columns and 5120 rows in total. Also, this dataset shows information per country collected from 1990 until 2014. Although it doesn't go further than that, this dataset represents possibilities of predictions of the variable TB count per year, type and country which can be considered as part of health measurements of prevention and control in the years that follow. In addition to that, all those measurements were estimates or approximate numbers as this is part of a geographical dataset, therefore it is important to keep in mind that the numbers analyzed represent approximate values of TB incidence, TB cases and mortality rate by year and country.


## Process
The project process, in an overwall way, followed the steps below:


### Step 1: Connecting the dataset about tuberculosis count by country with Tableau
At this step, the dataset, which is a .csv file composed of one physical table called *TB_Burden_Country*, was downloaded and connected as the data source in Tableau Public. This step was followed by EDA which is described in the next step.


### Setp 2: Checking different data types, columns and rows in the data set
At this step, it was done an initial EDA of the dataset by: 
- Ckecking the datatypes of each column and changing some of them (e.g. "Region" was converted to the geographical role "Country/Region");
- Updating columns names by removing some expressions on their titles as those expressions were making them very lenght and less readable (e.g. the expression "estimated" was removed as there was no colum with absolute measurements due to the geographic role of the data that we were working with, but only with estimated ones approximate/estimates numbers (decimals or floats data type);
- Understanding the meaning of Null or NaN values under some columns and rows in the dataset (columns such as "Mortality of TB cases who are HIV-positive, per 1000.000 population low bound" and "Mortality of TB cases who are HIV-positive, per 100 000 population, high bound" were full of rows with null values but this is expected to be found in a dataset composed mostly with numbers with a geographical role);
- Grouping the data dimensions into 2 relational hierarchies: (1) "Country/Territory or ISO Classification" grouped the information from country/territory, region, ISO-2 and ISO-3 (both represent classifications of country abreviations) and (2) "Methods to Derive Estimates" which grouped the methods to derive incidence estimates, prevalence estimates, mortality estimates and TBHIV (Tuberculosis with HIV incidence) estimates;
- Understanding the difference between some classifications presented in the dataset, such as the meaning of "latent TB" x "TB (active) disease", "low-bound" x "high-bound" and "ISO-2 country classification" x "ISO-3 country classification":
  a) latent-TB is given to a person that has tuberculosis, but doesn't show up symptoms or spread the disease,
  b) TB disease is given to a person that has the disease, can manifest its symptoms and can spread the disease,
  c) low-bound and high-bound
  c) ISO-2 and ISO-3 are numerical international codes used to designate every country/territory like an acronomy by using a 2 letter (ISO-2) or 3 letters combination (ISO-3) that designates as especific region or country.

- Updated some geographical regions/countries wich weren't accepted by Tableau as those existed during the flow of the history but were changed afterwards:
a) for "Serbia & Montenegro", it was added the latitude of 44.8166634 and longitude of 20.4666648,
Footnote: Serbia and Montenegro was a country in Southeast Europe, created from the two remaining republics of Yugoslavia after its breakup in 1991. The republics of Serbia and Montenegro together established a federation in 1992 as the Federal Republic of Yugoslavia.
b) for "Netherlands Antilles", it was added the latitude 12.226079 of longitude of -69.060087, 
Footnote: The Netherlands Antilles was a constituent country of the Kingdom of the Netherlands. The country consisted of several island territories located in the Caribbean Sea. The islands were also informally known as the Dutch Antilles. The country came into being in 1954 as the autonomous successor of the Dutch colony of Curaçao and Dependencies.
c) for "West Bank and Gaza Strip", it was left like this as those were palestinian territories that I couldn't find the accurate latitude and longitude to update them.


### Step 3: Build at least 5 different visualizations to learn more about the dataset. 
3.1 The first graph used to explore this dataset is titled "TB Detection Rate by Year". Similarly, this graph is divided into 3 big rows: the first shows the detection rate percent in a whole, the second, the detection rate low bound, and the thirs the detection rate high bound. By analyzing those lines, you can notice that the TB case detections in all forms (LTBI and TB disease) has a constant rate by year: the graph line is mostly high and stable and points out only small variations. Also, the 3 lines, which start in 1990 and finish in 2014, has their first small peak in 2003 and, after, in 2011. Those peaks were not showing significative changes in the percent of number cases of TB tough.

3.2 The second 


The first visualization was a graph about the tuberculosis data evolution by year in the world. Right after that, you can encounter another evolution table, but in this one the tuberculosis is visualized by country and year togeter.

From those visualizations, some questions poped up, such as:
3.1 HIV in tb cases x non-hiv in tb cases: how does it affect it?
3.2 Is there a correlation between TB count and HIV?
3.3 Is there a correlation between TB mortality and other diseases?





4. This table has 47 different features. Can you detect the most important features ? Why do you think these are important? Can you define a question for yourself? Try to learn more about these categories and find appropriate numerical features to study different trends in them. 
  - For example , the following features could be important for your analysis:
    - Country or territory name
    - Year
    - Estimated total population number
    - Estimated prevalence of TB (all forms) per 100 000 population
    - Estimated prevalence of TB (all forms)
    - Method to derive prevalence estimates
    - Estimated number of deaths from TB (all forms, excluding HIV)
    - Method to derive mortality estimates
    - Case detection rate (all forms), percent



### Step 2:








## Results
(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)

## Challenges 
Some of the challenges are descibed below:
- The dataset doesn't describe the information of TB count by age or different groups (e.g., male, female and children). As it only references the count by country and year with some columns bringing out the information by HIV/AIDS relationship, I found that the lacking of people segmentation impacted the analysis as it could give us a better picture of the tuberculosis incidence and mortality rate;
- 


## Future Goals
(what would you do if you had more time?)


## References
CDC. https://www.cdc.gov/tb/topic/basics/default.htm
https://www.nationsonline.org/oneworld/map/google_map_palestine.htm
WHO. https://www.who.int/news-room/fact-sheets/detail/tuberculosis
Nations online. https://www.nationsonline.org/oneworld/country_code_list.htm
