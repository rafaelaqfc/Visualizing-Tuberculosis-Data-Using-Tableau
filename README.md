# Final-Project-Tableau

## Project/Goals
Tuberculosis is not a disease of the past: about 
Tuberculosis (TB) is caused by a bacterium called Mycobacterium tuberculosis. The bacteria usually attack the lungs, but TB bacteria can attack any part of the body such as the kidney, spine, and brain. Not everyone infected with TB bacteria becomes sick. As a result, two TB-related conditions exist: latent TB infection (LTBI) and TB disease. If not treated properly, TB disease can be fatal (reference: https://www.cdc.gov/tb/topic/basics/default.htm).
In this project, you can find the analysis and visualizations experimented from a Tuberculosis dataset given by country. The dataset is a .csv file composed of one physical table called *TB_Burden_Country* and it has 47 fields or columns and 5120 rows in total.

## Process
The project process, in an overwall way, followed the steps below:
Step 1: Connecting the dataset about tuberculosis count by country with Tableau
Setp 2: Checking different data types and columns in the data set, such as:

- Ckecking the datatypes of each column and changing some of them ("Region" converted to the geographical role "Country/Region")
- Updating columns names (such as by removing the expression "estimated" of the labels to make them more readable as there was no colum with abolute measurements, but only with estimated ones approximate/estimates (float data type) and to not forget that I wrote this information as a note before displaying the analysis);
- Checking Null or NaN values (such as under the table "Mortality of TB cases who are HIV-positive, per 1000.000 population low bound" and "Mortality of TB cases who are HIV-positive, per 100 000 population, high bound" were full of rows with null values)
- Creating 2 relational hyerarchies in the table, such as between "Country/Terriotry", "Region", ISO-2"and ISO-3" which were under "Country/Territory or ISO Classification" and "Methods to Derive Estimates" which groupe the methods to derive incidence estimates, prevalence estimats, mortality estimates and TBHIV estimates.
- Understanding the difference between some classifications presented in the dataset, such as the meaning of "low-bound" x "high-bound" and "latent TB" and "TB disease": whereas a person can have tuberculosis and not show up symptoms and spread the disease what is called "latent TB",



ISO 2 and ISO 3 character given by country or territory (abreviation)
ISO-numerical given by country/territory code;
The estimated total number of a population given by year;
Prevalence of TB (All formas) per 100 000 population
Prevalence of TB (All formas) per 100 000 population, low bound
Prevalence of TB (All formas) per 100 000 population, high bound




Step 3: Build at least 5 different visualizations to learn more about the dataset. 
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



### (your step 2)

## Results
(Fill in which Option you chose, either 1 or 2. List the dataset you selected for the project if you selected Option 2. Also, discuss the visualizations you created, and why. For Option 2, also identify what your data question was, and how you went through the prompts.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
