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

Note: To assist in reading the visualizations, the following are the legends for the regions:

- EUR (Europe)
- AFR (Africa)
- AMR (America) 
- WPR (Western Pacific Region)
- EMR (Eastern Mediterranean Region)
- SEA (Southeast Asia)
    

### Step 4: Analyzing the features of the dataset to consider the ones with more statistical significance
In the analysis of the dataset, certain features were found to be more significant for the prediction model than others. These include the country or territory name for understanding the distribution of data and potential patterns between countries, the year to show the evolution of TB detection and mortality over time, and the region to see the count of TB cases per region and year. Similarly, the region feature was particularly relevant when combined with the year feature as it could give us a general idea from different places and times. The initial analysis showed that Europe had the highest count, Africa and America had a similar count that intertwined with each other, and Southeast Asia had the lowest count over the years.

Likewise, to fully understand the relationship between TB detection rate and the decline of TB deaths, other relevant features were considered, such as the prevalence of TB in all forms (latent and active), detection rate estimates, number of deaths and mortality rate per 100,000 population, and the methods used to derive the prevalence and mortality of TB. By analyzing these features, it was possible to understand the relationship between some of them and determine the most important ones to help answer our major question of whether there is a correlation between the rate of TB detection and the decline of TB deaths, as the number of deaths are still high in some countries.


### Step 5: Retaking the most significative visualizations done in step 3 to analyze some patterns, trends and keypoints of the dataset to create the dashboard
The visualizations created in step 3 were organized and consolidated into a dashboard, which was then used to tell a story with the data. The visualizations were arranged in a specific order to follow the analytical trajectory and answer the main question: "Is there a correlation between the detection rate and number of deaths?" This approach was chosen as the project's goal was not solely to describe African countries - even though it is noted that some of them have higher rates of TB prevalence and mortality rate -, as some projects do, which in my opinion, contributes to further stigmatizing the region instead of providing an analytical view to reduce the TB prevalence and mortality rates there.

At first, we gained an overall understanding of TB around the world through the map, and then delved deeper to examine the average TB detection rate over the years and across countries (grouped together). So it was observed that the average detection rate has been relatively stable, reaching a peak in 2003 and then gradually improving over time. For that, the average detection rate was analyzed in comparison with its feature of low-bound and high-bound in order to see if it was accurate to work with the general number estimate.

Next, we analyzed the "TB count per year and region" graph to compare the trends among regions. This graph provided a visual representation of the TB count rate for each region over time. The analysis revealed that Europe has the highest count of TB, followed by Africa, America, Western Pacific Asia, Eastern Mediterranean Region and Southeast Asia.

Then, the next graph analyzed the relationship between the TB detection rate and mortality rate (including and excluding HIV). The graph revealed that the presence of HIV significantly increases the death toll of TB. Also, some countries in Africa have a higher count of TB due to the relationship with the HIV gvariable (as this disease lower the immune-system, the person is more susceptible to get sick). Similarly, the graph showed that countries with lower detection rates tend to have higher numbers of deaths, such as: Central African Republic, Mozambique, Lesotho and Botswana (in Africa); Cambodia and Lao's People Democratic (in Western Pacific Region), Myanmar, Democratic People's Republic of Korea and Bhutan (in Southeast Asia), Somalia, Pakhistan and Afeghanistan (in Eastern Mediterranean Region), and Haiti (in America). On the other hand, Europe has a high detection rate and low number of deaths, confirming the correlation between the two variables.

Following that, the other graphs helped us analyze the prevalence of TB cases, number of TB deaths in all forms, incidence of TB cases including and excluding the effect of HIV, and how the prevalence of TB has evolved over time. When visualized together, these graphs aided us in creating regression models to analyze the correlation between the detection rate and number of deaths. Model 1 included the effect of HIV, while Model 2 excluded it. Both models showed a significant p-value (very low) and a low r-squared, indicating a negative correlation between the detection rate and number of deaths (as the detection rate increases, the number of deaths decreases).

The inclusion of the two treemap graphs in the analysis provided additional insight into the detection and estimation of TB mortality and prevalence rates. The use of different methods, such as Indirect and VR Imputed for mortality detection and survey imputed for prevalence estimation, highlights the importance of considering the method used when interpreting the results. Although the relationship between these methods and the detection rate wasn't analyzed due to time constraints, they are important factors to consider in future studies.

The final graph on the forecast, with a 95% confidence level, indicated that the number of deaths is expected to decrease, with a more significant decline in regions such as Africa, Western Pacific Region, and Southeast Region (including HIV).


## Results
Tuberculosis (TB) remains a widespread issue, with several well-known contributing factors, such as a lack of access to adequate healthcare and treatment in low-income countries and regions, weak immune systems due to comorbidities, lifestyle factors, and age groups. While we were not able to investigate these factors in detail at this project (they weren't part of our dataset so I am retaking them from different studies done in the field), our study emphasized the importance of detecting and preventing TB. Our regression model showed a negative correlation between the increase in detection rate and decrease in the number of TB deaths, with countries in Europe serving as a prime example.

At this project, the visualizations and the dashboard were useful as they gave us a general overview of the data and, therefore, helped us to spot trends and patterns. These visualizations supported us in exploring different aspects of the tuberculosis data by presenting the information with our question in mind. The maps, line graphs, horizontal bar chart and area graphs gave us a comprehensive understanding of the rate of detection, mortality, prevalence, and number of deaths due to TB over time, across regions and different countries. Also, they helped us to highlight specific trends and patterns, making it easier to understand and analyze the data.

The key points were highlighted through this process above (steps 4 and 5) and were used to create a story that could help in the decision-making process of the health system network (hospitals, clinics etc.) with the public agenda. So if federal and private institutions increase their policies and measures of prevention TB, this will probably promote the decline in the number of deaths of TB as the most relevant features were taken into account to make this conclusion. 

This project's aim was to examine the correlation between the rate of TB detection and the decline in the number of deaths and it achieved that aim by analyzing several graphs and visualizations. The results showed a negative correlation between the increase in the rate of detection and the decrease in the number of deaths, exemplifying the importance of detecting and preventing measures.

However, the methods used to estimate mortality and prevalence in different countries and their impact on the findings could not be addressed at this moment due to time constraints. Further analysis of the type, frequency, and accuracy of these methods will be crucial to understand the correlation between the quality of the treatment and efforts in reducing the global incidence of TB.

Overall, it is possible to say that this project provides intresting insights into the effectiveness of TB control and prevention efforts as it highlights the importance of continuing to invest in detection as soon as possible to combat TB around the world.


## Challenges 
The following challenges were encountered during the analysis:

- The lack of information on tuberculosis count by age, gender, and children in the dataset limited the analysis of tuberculosis incidence and mortality rate. The only available information was the count by country and year, and the impact of HIV/AIDS on tuberculosis;

- When trying to match significant map graphs, the legend and filter mismatch caused the need to explore each graph on separate sheets everytime the dashboard was updated;

- The geographical data had missing places which caused the dashboard map, a crucial tool for visualizing the dataset's distribution and spread, to malfunction at times. A temporary solution was to add a fixed map under the dynamic map to prevent blank spaces. A permanent solution will be found in the future;

- The dataset did not have any information on the correlation between TB mortality rates and immuno-deficient groups of people, making it impossible to answer one of the questions that came up during the exploratory data analysis (EDA) (*Is there a correlation between TB mortality rate with diseases that cause immuno-deficiency?*).


## Future Goals
In the future, I plan to revisit the regression models from this project and complete the analysis by incorporating different (independent) variables. I also aim to use this dataset in conjunction with others, such as the ones more updated from the *World Health Organization*, to analyze the segmentation of tuberculosis by various factors and features such as age group, gender, comorbidities, and lifestyle, as this dataset couldn't go further than considering the HIV group. Likewise, I am curious about the impact of TB detection methods and prevalence on mortality rates and the way different healthcare systems approach TB patients.

By adding demographic, lifestyle, and healthcare system factors to the TB analysis, we can gain a deeper understanding of why TB remains widespread and how detection methods impact rates. Further examination of variables in regression models could provide valuable insights into the impact of different factors on TB detection and mortality rates. This information can be used to inform public policies and strategies aimed at reducing TB prevalence and mortality.


## Files Description
Please find attached the following files for this project:

a) A PDF file of the dashboard "The Impact of Tuberculosis in the Globe (1990-2025)";

b) PowerPoint (.pptx) and PDF files of the story "The Impact of Tuberculosis in the Globe (1990-2025)";

c) A Tableau workbook (.twbx) and PowerPoint (.pptx) files named "The Impact of Tuberculosis in the Globe (1990-2025)" which include all visualizations, worksheets, dashboard, and story in one place.


## References
ALL Acronyms. https://www.allacronyms.com/

CDC. https://www.cdc.gov/tb/topic/basics/default.htm

Nations online. https://www.nationsonline.org/oneworld/country_code_list.htm

WHO. https://www.who.int/news-room/fact-sheets/detail/tuberculosis
