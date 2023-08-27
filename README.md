# Boston-Crime-Analysis

## Technical Skills: Python, Pandas, Seaborn, Scipy, Numpy, Matplotlib, and Plotly

1. **Data Preparation**:
   - `boston_row` dataframe is loaded with the Boston crime data.
   - The `OCCURRED_ON_DATE` column is converted to a DateTime format.
   - Data for only half of the months of April 2015 and June 2020 is filtered out.
   - Temperature data from two files `Temp_1_Boston.csv` and `Temp_2_Boston.csv` spanning from 2015 to 2020 is loaded, cleaned up, and concatenated into a single `temperature` dataframe.
   - The `boston_row` dataframe is merged with the `temperature` dataframe based on the date, resulting in the `boston_temp` dataframe.
   - An algorithm is applied to compute the temperature for each hour of the day based on the temperature range and the given coldest and hottest hours of the day.

2. **Exploratory Analysis**:
   - The dataset is explored based on the severity of the crime (categorized by UCR Part). The categories are: `Part One` (Most Severe), `Part Two` (Moderate), and `Part Three` (Least Severe). The number of each category of crimes and shootings is printed out.
   - A bar chart is plotted to show the number of crimes by year and severity level for the years 2016-2019.

3. **Location Analysis**:
   - It's mentioned that some cases are missing location data. Therefore, a new dataframe, `boston_copy`, is created and rows with missing or out-of-bound latitude and longitude values are filtered out.
   - Crime counts are then aggregated based on specific latitude and longitude, giving a count of crimes at each location.
