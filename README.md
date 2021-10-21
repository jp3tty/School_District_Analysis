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
### Global Impact
As seen below, removing THS's 9th grade scoresmakes little impact to the scores, percentages, and overall passing rate for the 15 schools. 

The initial district summary: 
![initial district summary](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/initial_district_summary.PNG)

Removing THS's 9th grade:
![adjusted district summary](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_district_summary.PNG)

Globally, the result gives a sense to the weight that 461 students can have over a population of 39,170. Based on the reduced overall passing percentage, it's safe to assume that THS's 9th grade, on average, scored higher overall than the district.

### Local Impact
Focusing down to the school level, the affect of excluding THS's 9th grade scores from the complete data set can have a significant impact on how the school is considered overall. If the 9th grade population is included in the data but all of their scores are set to null, the overall results drop significantly. As shown here:
![THS exclude](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_THS_exclude.PNG)

To prevent THS 10th, 11th, and 12th grades from being penalized, it's best to completely remove both the 9th grade's scores and poplultion when considering the schools scores, percentages, and overall passing rate.
![THS 9th completely excluded](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_THS_results_(9removed).PNG)

Comparing this to the previous results, we see a signification improvement to THS's scores, percentages, and overall passing rates. The average math and reading scores remain the same but, because we excluded THS's 9th grades population, the passing percentages have all improved.
* Passing math from 66.9% to 93.2%.
* Passing reading from 69.7% to 97.0%.
* Overall Passing from 65.1% to 90.6%.

This result gives the district a better view of THS's performance when compared to the other schools, as long as it's noted that the 9th grade population and their grades were not included in the analysis.

### Top 5 performing schools
![Top 5 schools](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_top5.PNG)

THS is in th top 5 with 90.6% overall passing. If we included their 9th grade population, their overall passing of 65.1% would have placed the below the top 5.


### Bottom 5 Performing Schools
![Bottom 5 schools](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_bottom5.PNG)


### Average Math Score For Each Grade
![Ave math by each grade](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_school_math_scores.PNG)

Removing THS's 9th grade math scores is shown as "nan."


### Average Reading Score For Each Grade
![Ave reading by each grade](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_school_reading_scores.PNG)

Removing THS's 9th grade reading scores is shown as "nan."


### School Performance Based On Budget Per Student
![School performance based on budget](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_spending_per_student.PNG)

Excluding THS's 9th grade population, due to issues with that groups data, helps justify their per student spending ($638.00) due to the schools high performance level (Overall Passing at 90.6%). If their 9th grade population remained in the analysis but their scores were null, their poor performance (as shown in the Local Impact section above) could cause the district to question the schools service to their students.


### School Performance Based On Size
![School performace based on size](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_scores_per_school_size.PNG)
The adjust the THS data also keeps their performance in range with what is expected in performance for it's school size. With a population of 1635 students, we see that its scores, percentages, and overall passing rates are close to what is on average for a medium sized school.


### School Performance Based On School Type
![School performance based on type](https://github.com/jp3tty/School_District_Analysis/blob/main/Images/adjusted_scores_per_school_type.PNG)
As a charter, THS is also preforming close to the average base on the table above.

## Summary
1. The overall passing rate for Thomas High School dramatically changed from 65% to 91% after the questionable 9th grade data was removed.
2. Thomas High School's overall rank (based on the overall passing percentage) rose from 8th to 2nd. 
3. After the data correction, Thomas High School's 9th grade math and reading scores show NaN.
4. In addition to the overall passing rate, the districts math and reading percentages on a global scale have minimally. 
