# Data-analysis-of-NZ-Crashes
Data analysis of NZ Crashes

## Purpose
Understand the relationship between fatalCount (the count of fatalities associated with a crash) and the rest of the variables in the Crash_Analysis_System_(CAS)_data data set.

## Overall Process
Whilst working on this project I handled data cleaning, data visualization and data analysis. I also used feature selection techniques, regression (Poisson and negative binomial), checked model assumptions and performed model evaluation.

## Result
The coefficients of the the regions Gisborne, Marlborough, Nelson, Southland and Tasman aren’t statistically significant which means that there is no statistically significant difference in the count of deaths for a car crash (fatalCount) between those regions and the reference level Auckland. However other regions have a statistically significant difference in the count of deaths for a car crash when compared to Auckland.

The variable flatHill is statistically insignificant however I will not be removing this variable from the data due to the fact that stepwise BIC keeps this variable in the model.

The variables are on extremely different scales, which could be affecting the specific values of regression coefficients, however this does not affect the statistical significance or interpretation of the coefficients.

Each observation in this data set could have a different number of people in the car at the time of the crash which will affect the total number of possible fatalities for that car crash, this is difficult to account for. Unfortunately since the total number of people in the car at the time of the crash for each observation is unreported and I cannot determine a way to derive this variable from the variables in the data set. If the number of people in the car for each observation had been recorded then I would have treated this variable as an exposure variable and I would have used this variable as an offset in my model.

I started this project with the intent of understanding the relationships between fatalCount (the count of fatalities associated with a crash) and the other variables in the data set. I have fit a model that provides information about the relationship each variable has with the response (whether it is negative or positive, and whether it is statistically significant). I also found that the data follows a negative binomial distribution.

## References and citations
Waka Kotahi NZ Transport Agency. (n.d.). CAS data field descriptions and data set. Retrieved May 19, 2025, from https://opendata-nzta.opendata.arcgis.com/pages/cas-data-field-descriptions

