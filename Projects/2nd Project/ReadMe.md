This is a project from Practicum Program

Its about researching on car sales ads and finding the best sources <br>
Its done in Jupyter<br>
Language: Python<br>
Source file: vehicles_us.csv



# Researching car sales ads

👉 View the `notebook` **[here](https://nbviewer.org/github/AviVolah/AviVolah/blob/Practicum/Projects/2nd%20Project/Project%202%20-%20Research%20on%20car%20sales%20ads.ipynb)** using **nbviewer**.


## Project description
### Objective
To study advertisements for vehicles data collected over the last few years at Crankshaft List and determine which factors influence the price of a vehicle.

### Description of data

`vehicles_us.csv`:  Data on vehicles ads
- **price**: the price of the vehicle
- **model_year**: the year the vehicle's model was manufactured
- **model**: the make and model of the vehicle
- **condition**: the condition of the vehicle (e.g. "new", "like new", "excellent", "fair", "salvage")
- **cylinders**: the number of cylinders in the vehicle's engine
- **fuel**: the type of fuel used by the vehicle (e.g. "gas", "diesel", "electric")
- **odometer**: the vehicle's mileage when the ad was published
- **transmission**: the type of transmission used by the vehicle (e.g. "automatic", "manual")
- **paint_color**: the color of the vehicle's exterior paint
- **is_4wd**: whether the vehicle has 4-wheel drive (Boolean type)
- **date_posted**: the date the ad was published
- **days_listed**: the number of days between the publication and removal of the ad


### Libraries to run the notebook locally
***Python version 3.8.8***
|Library| Version|
|---|---|
|Pandas | 1.3.5 |
|NumPy | 1.20.1 |
|Matplotlib | 3.5.2 |
|Seaborn | 0.11.2 |


## Project overview

### Prepare data
- The data had some issues, including missing values and errors, but no duplicates
- Organized the table by lower casing text columns and rounding numerical columns.
- Filled in missing values in the is_4wd column with 0 and in paint_color with "other" since I had no way of determining which color it was and it didn't really matter.
- Replaced the condition values with numbers and used a correlation table to fill in null values in other columns by grouping them based on odometer and price.
- Converted all floats to integers and dates to datetime.
- Checked for duplicates and abnormal values, such as very high prices compared to other vehicles of the same model and condition.
- Obtained a clean table with 51,525 rows and no NaNs or duplicates.
- Added Day of the week, month, and year the ad was placed, the vehicle's age (in years) when the ad was placed and the vehicle's average mileage per year

### Exploratory analysis
*Overall dataset exploration*
- Analyzed histograms of the tasked columns to identify outliers and their location.
- Filtered outliers beyond the extreme points of each column and created an outlier table as requested.
- Created new histograms for the same columns with the filtered data and compared them to the previous histograms to draw conclusions.
- Studied the "days listed" column and selected the two types with the most ads posted.
- Checked which of the tasked columns had the greatest impact on price, and found that vehicle age was the most significant factor.


### Conclusion

In conclusion, we have successfully analyzed the advertisements for vehicles data collected over the last few years at Crankshaft List, with the objective of determining which factors influence the price of a vehicle. We prepared the data by addressing missing values, organizing the table, and converting data types. We also performed exploratory data analysis, which included analyzing histograms, filtering outliers, and studying the "days listed" column. We found that vehicle age had the greatest impact on the price of a vehicle. Overall, our analysis has provided valuable insights into the factors that influence vehicle prices, which can be used to inform future pricing decisions.
