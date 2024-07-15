# msda-capstone
## Author: Nic Vetter

Hello and welcome to my GitHub repo for my Master's of Science in Data Analytics through Northwest Missouri State University. 
Throughout the capstone project, I will be using analyzing the trends of public high school spending and proficiency percentages using the following tools/skills:

SQL, Machine Learning in Python, Tableau, Overleaf, and LaTeX. 

My hope is to show the correlation between Iowa Public Schools $/pupil and Math/Reading proficiency scores on standardized tests. 

I will then forecast the minimum $/pupil schools should be spending to meet proficiency standards. 

I am happy you are reading through this project and have a great day!

## Data Sources:
[Data Source 1](https://data.iowa.gov/Primary-Secondary-Ed/Math-And-Reading-Proficiency-in-Iowa-by-School-Yea/f3h8-mnxi/about_data)

[Data Source 2](https://data.iowa.gov/School-Finance/Iowa-School-District-Expenditures-by-Fiscal-Year/uutu-bzs3/about_data)

This data set was collected from the Iowa.gov website as public information. The Iowa.gov website
has an ”Action Query” function that helps the writer filter the necessary data from the dataset. This
is called preliminary cleaning of the dataset and the dataset will be cleaned again in section 3 of this
report. The writer will only be using the reading proficiency rating of the 2017 11th-grade students in
each respective district. This is to shorten the report for the tight time window

## Data Cleaning/Manipulation using PostgreSQL and PgAdmin:

The below images show the cleaning SQL syntax within PgAdmin along with a JOIN function to create a singular CSV file.
This was joined because of the ease of reading/loading within Python/pandas. 

![Alt Text](clean1.png)

![Alt Text](clean2.png)

## Overview of Clean Data after PostgreSQL:

The attributes after the cleaning process was completed are as follows:
”fiscalyear”,”dist”,”district name”,”source”,”expenditures per pupil”,”amount”,”enrollment category”,”enrollment
category number”,”topic”,”proficient”,”total”,”percent proficient”,”proficient category”.

Below is a sample of the CSV’s first line of the cleaned data:
2017,”0009”,”AGWSR”,”Instruction”,7989,4997256,”600-999”,”3”,”Reading”,32,41,”78.00”,”70.1 - 80”.

If the data shown in the line above is surrounded by ””, it is a string/text data type. However, if
the data shown in the line above is surrounded by nothing, it is an integer data type.

To align with the goal of the report, the dependent variable of the project is ”percent proficient” and
the independent variables are all of the other attributes contained within the cleaned CSV file(outlined
above). However, the main independent variable that will be analyzed is ”expenditures per pupil”.


-Nic Vetter
