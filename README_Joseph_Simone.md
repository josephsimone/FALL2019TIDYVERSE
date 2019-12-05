CUNY DATA 607 Fall 2019 Tidyverse recipes
@author: Joseph Simone

### Airline Data Selection & Import 

When I was in High School, the Television show that everyone could not stop talking about was "Lost". This famous show, created by J.J. Abrams, depicted a fictional plane crash and what happened subsequently to the passengers and crew. In real life, and it seems a lot more in recent history than ever, planes have been crashing or vanishing at sea at an alarming rate. Personally, my father travels about 25 weeks out of the year. Coming from a computer science background and not an engineering one. How can I give  my father and the rest of the traveling community, some sort of "advise" for flying safe within the means of my area of expertise. Here is where this project can come into play. I found this dataset off of Kaggle's GitHub page that was the data behind a very powerful article, [Should Travelers Avoid Flying Airlines That Have Had Crashes in the Past?](https://fivethirtyeight.com/features/should-travelers-avoid-flying-airlines-that-have-had-crashes-in-the-past/). For now, let's create a "Tidy Recipe" for this dataset.

##### Kaggle's GitHub Repo for Airline Saftey Data
https://github.com/fivethirtyeight/data/tree/master/airline-safety

##### Airline Saftey CSV RAW
https://raw.githubusercontent.com/fivethirtyeight/data/master/airline-safety/airline-safety.csv

### First Look 
We can obserse above, that thi dataset provides both the date-ranges : 85-99 and 00-14 in a row. 

First we will want to convert this dataset into a format in which, for each airline there will be 2 rows: one for 85-99 and another row for 00-14.

From here, this will allow for each date range within an airline, where 1 row store the "count" which are accrued from - "incidents", "fatal_incidents" and "fatalities".

By doing so, this will create a new working data-frame that will be clean and easier to perform analysis on. 




### Tidying -r 
Using the $tidyr$ package, we will convert this data into a long dataset using the $gather$ function.

This will count variables "type" and "date_range" in a column.

In addition, the value of this count will be placed into another column.




From here, we split the date range and type into two different columns

Furthermore, eliminating columns which hasthem both together:

### Splitting the Range


Using the $spread$ function and using  the variables, “incidents”, “fatal_incidents” and “fatalities”, while counting the occurences to create a value.

This is to convert back into a dataset, however, creating a date range wise split in the process. 


Now the data is fully ready with each airline and a date range having 1 row each

### Sorting Quick


You can see from a "quick" sort using the $order$ plus a $-$ before the variable to create a  descending DataFrame based on incidents



### FURTHER MY EXAMPLE

Feel Free to use my recipe to do some futher analysis ! 






