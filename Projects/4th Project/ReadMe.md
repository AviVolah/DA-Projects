# Video gmes trends

👉 View the `notebook` **[here](https://nbviewer.org/github/shirarua/practicum-projects/blob/main/sales_funnel_AAB/sales_funnel_AAB_test.ipynb)** using **nbviewer**.


## Project description
### Objective
Identify patterns that determine whether a game succeeds or not.

### Description of data
`games.csv`: User and expert reviews, genres, platforms (e.g. Xbox or PlayStation), and historical data on game sales.
- **Name:** Name of the game
- **Platform:** The gaming console
- **Year_of_Release:** The release year
- **Genre:** Game genre
- **NA_sales:** North American sales in USD million
- **EU_sales:** Europe sales in USD million
- **JP_sales:** Japan sales in USD million
- **Other_sales:** Other countries's sales in USD million
- **Critic_Score:** The score a critic gave a game, maximum of 100
- **User_Score:** The avg score players gave a game, maximum of 10
- **Rating:** ESRB rating for a game


### Libraries to run the notebook locally
***Python version 3.8.8***
|Library| Version|
|---|---|
|Pandas | 1.3.5 |
|NumPy | 1.20.1 |
|SciPy | 1.6.2 |
|Sidetable | 0.9.0 |
|Matplotlib | 3.5.2 |
|Missingno | - |
|Termcolor | - |
|Seaborn | 0.11.2 |


## Project overview

### Prepare data
- Organized the table by making the column names lower case as well as all their contents
- Converted the columns to their proper data types
- Removed duplicates
- Dealt with missing values
- Adjusted the ESRB ratings to remove any old rating types

### Exploratory analysis
*Overall dataset exploration*
- Looked at how many games were released in different years, and if the data for every period were significant
- Looked at how sales varied from platform to platform
- Built a distribution based on data for each year for the platforms with the greatest total sales
- Determined a period to take data for
- Analyzed which platforms are leading in sales and which are growing or shrinking
- Built a box plot for the global sales of all games, broken down by platform
- Looked at how user and professional reviews affect sales for one popular platform
- Looked at the general distribution of games by genre


### Hypothesis testing
- Tested if the average user ratings of the Xbox One and PC platforms are the same.
- Tested if the average user ratings for the Action and Sports genres are different.

### Conclusion

Preprocessing - originally i got a data about game sales and their different platforms and genres. The data contained nulls that needed to be calculated to fill and had errors and little duplicates. first i organized the table by making the column names lower case as well as all object columns contents
then i converted the columns to their proper data types, fixed little errors and removed duplicates. then i filled several nulls in year_of_release, rating and critic_score, with values (or medians of them) from other rows of games with the same name available for other platforms and the year also by the numbers in the name itself, additional nulls in year_of_release and rating, with high sales i filled manually, and the little bit of the remaing year_of_release nulls i dropped. i left missing values in rating, user_score, and critic_score, because those columns are not needed for all parts of our analysis.
then i adjusted the ESRB ratings to remove any old rating types, and in the end i got a table of 16583 rows with no problematic nulls and no duplicates.

Analyzing the data - i checked how many games were released in different years to start seeing the relevant years for the analysis, then found the platforms with the greatest total sales and figured out the timeframe of relevance for platforms in general to know which years are relevant, and determined what period to take data for building a prognosis for 2017.

i took data from 2012 - 2016 of all platforms that were still active in 2016.
i found that the leading platforms were ps4, ps3 and x360
but the platforms that are growing in sales are ps4 and xone
the north american region has the largest influence on overall global sales.
there is no need to consider the user score, the critic score is a bit more important but still not critical for the sales
the european and north american regions are roughly the same but entirely different strategies have to be adopted for the japanese region.
for example home consoles perform better than their handheld counterparts across both regions but handheld platforms are very popular in japan.
another example is the ESRB rating - europe and north america follow the exact same pattern, the T rating has the least sales per unit/name (not game/title) and M has the most sales and japan un-surprisingly sells the E rating better than the rest ratings (since it includes the non-gore and RPG genres they love), followed by the T rating and the least profitable rating is for E10+
Testing the hypotheses - i couldnt reject the first H0, but did reject the second H0

so in both na and eu regions, i would suggest focusing advertising mainly on ps4, xone, ps3 and x360 platforms, action and shooter genres, of the T rating.
and for the jp region i would suggest focusing advertising mainly on a handheld platform, specifically 3ds and also on the last 2 playstation genarations, RPG and action genre-wise, of the E rating.
