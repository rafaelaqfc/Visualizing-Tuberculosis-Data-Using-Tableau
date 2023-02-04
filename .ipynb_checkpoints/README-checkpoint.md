# Final-Project-Tableau

## Project/Goals
Tuberculosis is not a disease of the past: about 

## Process
### (your step 1)

The Tuberculosis dataset given by country is a .csv file composed of one physical table called "TB_Burden_Country" with 47 fields or columns and 5120 rows in total.

ISO 2 and ISO 3 character given by country or territory (abreviation)
ISO-numerical given by country/territory code;
The estimated total number of a population given by year;
Prevalence of TB (All formas) per 100 000 population
Prevalence of TB (All formas) per 100 000 population, low bound
Prevalence of TB (All formas) per 100 000 population, high bound

low-bound meaning
high-bound meaning


hiv in tb cases x non-hiv in tb cases: how does it affect it?

- Ckecking the datatypes of each column and changing some of them ("Region" converted to the geographical role "Country/Region")
- Updating columns names (such as by removing the expression "estimated" of the labels to make them more readable as there was no colum with abolute measurements, but only with estimated ones approximate/estimates (float data type) and to not forget that I wrote this information as a note before displaying the analysis);
- Checking Null or NaN values (such as under the table "Mortality of TB cases who are HIV-positive, per 1000.000 population low bound" and "Mortality of TB cases who are HIV-positive, per 100 000 population, high bound" were full of rows with null values)
- Creating 2 relational hyerarchies in the table, such as between "Country/Terriotry", "Region", ISO-2"and ISO-3" which were under "Country/Territory or ISO Classification" and "Methods to Derive Estimates" which groupe the methods to derive incidence estimates, prevalence estimats, mortality estimates and TBHIV estimates.
- Understanding the difference between some classifications presented in the dataset, such as of "low-bound" x "high-bound" and "latent TB" and "TB disease"

https://www.cdc.gov/tb/topic/basics/default.htm

a latent TB person doesn't show up symptoms and cannot spread the disease



Tuberculosis (TB) is caused by a bacterium called Mycobacterium tuberculosis. The bacteria usually attack the lungs, but TB bacteria can attack any part of the body such as the kidney, spine, and brain. Not everyone infected with TB bacteria becomes sick. As a result, two TB-related conditions exist: latent TB infection (LTBI) and TB disease. If not treated properly, TB disease can be fatal.




### (your step 2)

## Results
(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
