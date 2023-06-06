# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
(fill in your description and goals here)


The objective of this project is to build up our skills in API requesting, retreiving the data, parsing json file to a dataframe, joining data from diffrent dataframes,EDA, build a model and analyze the results.

## Process
citybikes API: According the API documentation, explore the structure of data, chose city Hamilton and defined city and station function to retreive the information, 
               parse the JSON object into a Panda data frame and save the JSON file for future use.
Foursquare and Yelp API: sent request to all the bike stations in Hamilton, and get the POI, 
                parsing json file to a dataframe, and chose the top 10 restaurants.
                add the column ave_rating, num_restaurant and merge yelp_df with citybike dataframe.
Performmed EDA: drop columns and NaN value, and used group by command to filter data. for example, Filter rows where 'empty_slots' is greater than 10; Calculate the ratio of 'free_bikes' to 'empty_slots' 
               add it as a new column 'bike_ratio'. Group the DataFrame by 'station_name' and calculate the sum of 'total_review_count'
               use Seaborn’s Pairplot to check if there is linearity between the numerical variables. 


Model building: drop station_name column and retained only the numeric column.
                import statsmodel library,
                assign “free_bikes” from data frame to y as the target variable.Assign the column “ave_rating”and ‘num_restaurant’ from dataframe to X
                add a constant
                use ‘sm.OLS( )’ to create an ordinary Least Squares regression model, takes y, X
                Use the ‘.fit’ method to estimate the coefficients of the model that best fit the data
                Analyze the output, R-squared == 0,014, 3 p-value and associated p-value are greater than 0,05, F-statistic (0.6080) 
                get the couclusion: All the outputs show that the predictors are not effectively explaining the variability in 'free_bikes’.







## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)

I can't not get the rating from foursqure data, so I just used the Yelp API data.


The results of the model: Comparing the R-squraed  and3 p-values and associated p-value, all the outputs show that the predictors are not effectively explaining the variability in 'free_bikes’.

    (R-squared: 0.014: greater than 0 though, but is really small, indicating that the model explains only a small proportion of the variance in the target variable 'free_bikes’. 
    the p-value: all 3 p-values and associated p-value are greater than 0,05, suggesting that it is not statistically significant at a typical significance level (e.g., 0.05). 
    The F-statistic (0.6080) and its associated p-value (0.547) test the overall significance of the regression model. 

)


## Challenges 
(discuss challenges you faced in the project)

The challenges I faced in the project:
    1. parsing the nested json file into dataframe.
    2. building regression model, I went throught the lectures and assignments and figured it out.

## Future Goals
(what would you do if you had more time?)
If I have more time, I will do more about EDA and practise to use 2 for loops to send a request and parse it to a dataframe. 