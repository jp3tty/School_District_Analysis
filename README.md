# School_District_Analysis
## Overview
A school district requested a snapshot of their high school test results and would like to see the metrics presented in the following ways:

* Top 5 and bottom 5 performing schools, based on the overall passing rate.
* The average math score received by students in each grade level at each school.
* The average reading score received by students in each grade level at each school.
* School performance based on the budget per student.
* School performance based on the school size.
* School performance based on the type of school.

The district provided their data via two CSV files, "schools_complete.csv" and "students_complete.csv." The analysis, conducted through a Jupyter notebook, began by fixing student name entries in the "students_complete.cvs" file and then merged the CSVs in order to sort through the data keys to provide the desired metrics.

After the our initial analysis was completed, the district determined that all 9th grade math and reading scores from Thomas High School (THS) was inaccurate and asked to have it withdrawn. Using the Jupyter notebook, the reading and math scores values for Thomas High School's 9th grade population (461 students) was located and remove. Below we will disclose the results of the analysis and discuss the impact that removing the scores had overall.

## Results

As seen below, there was little impact to the scores, percentages, and overall passing rate for the 15 schools. 

The initial district summary: 
![initial district summary](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/initial_district_summary.PNG)

Removing THS's 9th grade:
![adjusted district summary](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_district_summary.PNG)

The result gives sense to the weight that 461 students can have over a sample of 39,170. Based on the score removals, it's safe to assume that Thomas' 9th grade, on average, scored higher than the overall district.

The affect of excluding THS 9th grade from the complete data set can have an enormous impact on how the school is considered overall. If THS 9th grade is included in the data but all of their scores are set to null, the overall results drop significantly. As shown here:
'![THS exclude]()
To prevent THS 10th, 11th, and 12th grades from being penalized, it's best to completely remove both the 9th grade's scores and poplultion when considering the schools scores, percentages, and overall passing rate.
'![THS 9th completely excluded]()
Comparing this to the previous results, we can see a signification improvement to THS's performance.

In the school summary 

* How is the school summary affected?
+++Show how top and bottom 5 has changed+++

Removing Thomas High School's 9th grade
![adjusted school summary](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_school_summary.PNG)

* How does replacing the ninth graders' math and reading scores affect Thomas High School's performace to the other schools?
By removing Thomas High School's 9th grade population from the moves the school from 2nd overall in our initial analysis to 13th overall.

* How does replacing the ninth-grade scores affect the following:
  * Math and reading scores by grade
  * Scores by school spending
  * Scores by school size
  * Scores by school type

Adjusting the data after the discrepencies were found in Thomas High School 9th grade.
@Image of Thomas High School before
@Image of Thomas High School after

Original Analysis:
@ Analysis on 15 schools



Adjusted Analysis:


## Summary
1. The overall passing rate for Thomas High School dramatically changed from 91% to 65% after the questionable 9th grade data was removed.
2. Thomas High School's rank dropped from 2nd to 8th due to the 
3. After the data correction, Thomas High School's 9th grade math and reading scores show NaN.
4. In addition to the overall passing rate, the districts math and reading percentages shifted. 
