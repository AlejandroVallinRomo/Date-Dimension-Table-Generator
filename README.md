# Date-Dimension-Table-Generator

## Overview
This project generates a comprehensive Date Dimension Table in a CSV format, which includes various attributes for dates ranging from January 1, 2023, to December 31, 2023. The date range can be easily changed to the needs of the used by modifying the variables start_date and end_date. After running the program, a CSV with the name "date_dimension.csv" is generated on the curent working directory, and it can be visualized on Excel or PowerBI as a table where each row is a day, and each column is a different characteristic of that day. 
The table is designed for use in data warehousing and business intelligence applications for companies that do business both in Mexico and in the United States, so it provides both date formats used in Mexico (DD/MM/YYYY) and in the USA (MM/DD/YYYY), as well providing a list of holidays celebrated in both Mexico and the USA. 

## Columns Generated
- Date ID (YYYYMMDD format)
- Date (ISO format)
- DateMex (DD/MM/YYYY)
- DateUSA (MM/DD/YYYY)
- DayNum (ISO day number)
- DayName (e.g., Monday)
- Weekday (1 if weekday, 0 if weekend)
- Week (ISO week Number)
- Month (ISO month number)
- MonthName (e.g., January)
- Quarter (number of quarter on the year)
- QuarterName (e.g., Q1)
- Year (YYYY format)
- MonthYear (Month-Year format)
- Day of the month
- IsHoliday (1 if Holiday, 0 if not)
- HolidayName (if applicable)

## Holidays Included
The table includes the following holidays:
- New Year's Day (January 1)
- Mexico's Independence Day (September 16)
- Christmas Day (December 25)
- Labor Day in Mexico (May 1)

## Output
"date_dimension.csv" will be generated on current working directory.

The csv file can be opened with Excel if you like to inspect it, but is not meant to be used as an Excel file.
Here are the first 3 lines of the table as an example of the formatting:

|DateID|Date|DateMex|DateUSA|DatNum|DayName|Weekday|Week|Month|MonthName|Quarter|QuarterName|Year|MonthYear|IsHoliday|HolidayName|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|20230101|2023-01-01|01/01/2023|01/01/2023|1|Sunday|0|52|1|January|1|Q1|2023|Jan-2023|1|New Year's Day|
|20230102|2023-01-02|02/01/2023|01/02/2023|2|Monday|1|1|1|January|1|Q1|2023|Jan-2023|0|NaN|
|20230103|2023-01-03|03/01/2023|01/03/2023|3|Tuesday|1|1|1|January|1|Q1|2023|Jan-2023|0|Nan|

## Future
A few holidays still need to be added, as well as "dynamic" holidays such as Labor day un the USA (The first Monday of September).
I plan to have two tables, one for Holidays in Mexico, and another one for Holidays in the USA. This means that the column "IsHoliday" will have to be divided into something like "IsHolidayMex" and "IsHolidayUSA", and the column "HolidayName" will probably have to be modified in some way as well.

Finally, other additional columns could be added if some unexpected necessities arise after I start to use these dimension tables on PowerBI projects.
