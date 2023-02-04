# Final Project with Tableau

## Project/Goals
   Tuberculosis is not a disease of the past: although it was discovered in 1988, the whole world did not reach the milestone of 0% tuberculosis patients. Fortunately, it can be cured and prevented. According with the *World Health Organization*, a total of 1.6 million people died from tuberculosis in 2021. Ranked as the 13th leading cause of worldwide death and as the 2nd leading killer infectious after COVID-19 (above HIV/AIDS), tuberculosis (TB) is present in all countries and age groups. One of the *United Nations Sustainable Development Goals (SDGs)* is to put an end in the TB epidemic by the year of 2030. 
   Tuberculosis (TB) is caused by a bacterium called *Mycobacterium tuberculosis*. This bacteria attacks mostly the lungs, but it can also attack other parts or organs of the body such as the kidney, spine, and brain. It is important to note that not everyone infected with the TB bacteria becomes sick. Due to that, there are two TB-related conditions: (1) latent TB infection (LTBI) and (2) TB disease. If not treated properly, TB disease can be fatal.
   In this project, you will find the analysis and visualizations experimented from a Tuberculosis dataset given by country. The dataset is a .csv file composed of one physical table called *TB_Burden_Country* and it has 47 fields or columns and 5120 rows in total. Also, this dataset shows information per country collected from 1990 until 2014. Although it doens't go more over than that, this dataset represents possibilities of predicition of the variable TB count which can be considered to the next years. In addition to that, all those measures were estimates or approximate numbers as this is part of a geographical dataset, therefore the numbers analyzed represent approximate values of TB incidence or mortality rate by year and country.

## Process
The project process, in an overwall way, followed the steps below:

### Step 1: Connecting the dataset about tuberculosis count by country with Tableau
At this step, the dataset, which is a .csv file composed of one physical table called *TB_Burden_Country*, was uploaded from the website. In total, the dataset has 47 fields or columns and 5120 rows in total.

### Setp 2: Checking different data types and columns in the data set, such as:
- Ckecking the datatypes of each column and changing some of them ("Region" converted to the geographical role "Country/Region")
- Updating columns names (such as by removing the expression "estimated" of the labels to make them more readable as there was no colum with abolute measurements, but only with estimated ones approximate/estimates (float data type) and to not forget that I wrote this information as a note before displaying the analysis);
- Checking Null or NaN values (such as under the table "Mortality of TB cases who are HIV-positive, per 1000.000 population low bound" and "Mortality of TB cases who are HIV-positive, per 100 000 population, high bound" were full of rows with null values)
- Creating 2 relational hyerarchies in the table, such as between "Country/Terriotry", "Region", ISO-2"and ISO-3" which were under "Country/Territory or ISO Classification" and "Methods to Derive Estimates" which groupe the methods to derive incidence estimates, prevalence estimats, mortality estimates and TBHIV estimates.
- Understanding the difference between some classifications presented in the dataset, such as the meaning of "low-bound" x "high-bound" and "latent TB" and "TB disease": whereas a person can have tuberculosis and not show up symptoms and spread the disease what is called "latent TB",
- ISO 2 and ISO 3 character given by country or territory (abreviation)
- ISO-numerical given by country/territory code;
- The estimated total number of a population given by year;
- Prevalence of TB (All formas) per 100 000 population x Prevalence of TB (All formas) per 100 000 population, low bound
- Prevalence of TB (All formas) per 100 000 population, high bound

### Step 3: Build at least 5 different visualizations to learn more about the dataset. 
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
The first graph used to explore this dataset is titled "TB Detection Rate by Year". On it, you can notice that the TB case detections in all forms (LTBI and TB disease) has a constant rate by year: the graph line is mostly constant and poins out only small variations. The line starts in 1990 and has its first peak in 2003 and, after, in 2011. This graph is divided into 3 parts as it shows the detection rate percent in a whole, the detection rate low bound, the detection rate high bound.
The second 








## Results
(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)

## References
CDC. https://www.cdc.gov/tb/topic/basics/default.htm