# School District Analysis

The challenge of this week is related to the analysis of *School District Data* for finding insights about performance trends of schools within the district.   The data is collected from different sources and formats and the findings of the analysis helps the School Board to design strategies and decisions regarding the school budgets and priorities.

## Overview

An initial analysis on student funding and students standarized test scores has been carried out.  However, the school board suspect some reading and math scores have been altered and they fear this alteration may affect the initial analysis.  This data corresponds to the scores of the 9th grade at the **Thomas High School**.  We need to ignore these data, perform again the analysis and present the new findings contrasting them with the initial ones.

## Results

In order to handle this possible academic dishonesty, we need to replace with `NaN` all math and reading scores for *Thomas High School* and then repeat the initial school district analysis. Here it is a glimpse of the dataframe showing the `NaN` values replacing the scores for *9th grade* at *Thomas High School*.  

![Nan_in_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_NaNs.png)

As an general overview, we need to notice that the total of students in the distric is 39,170 and the total students with `Nan` as score values is 461.  Below it is our findings that give  answers to some questions:

1. How is the distict summary affected?

To see how the district scores were affected, we need to compare the scores before the replacement of 9th grade students at Thomas High School and the same scores after the replacement.  In the below table, there are the scores before replacement: 

| Average Math Score | Average Reading Score | Passing Math (%) | Passing Reading (%) | Overall (%) |
| :-----: | :------: | :-----: | :-----: | :-----: |
| 79 | 81.9 | 75 | 86 | 65 | 

There is a difference of &pm;1 point in the tenths for the math and reading passing scores and their associate percentages as it is shown in the bellow dataframe.  This small difference may not have any big impact in the further analysis since it seems to be statistical insignificant.

### District Summary:
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_districtSummary.png)

2. How is the school summary affected?:

In general only *Thomas High School* was affected for the change in the scores. Its  *Overall Passing %* before was 90%.  If in our analysis we don't consider any of the students from 9th grade at Thomas High School, the overall passing percentage for this school drops to 65%, as it can be seen in the below dataframe:

### School Summary using All students from all schools:
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_schoolSummary.png)

If we compute for the Thomas High School its scores and percentages for math and reading using only the students from 10th to 12th grades as the total number of studentes, the school summary dataframe does not change much respect to the results that we got before (in the module).

### School Summary using only Students from Thomas High School:
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_schoolSummary_noninthTHS.png)

3. How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Based on the second dataframe in the previous question. The replacing of math and reading scores does not affect the order of the school ranking, as we can see in the top 5 and the last 5 schools.  The ranking respect to the *Overall passing %* does not change.

### Top 5 Schools based on the Overall Passing: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_topschools.png)

### Bottom 5 Schools based on the Overall Passing: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_bottomschools.png)

4. How does replacing the ninth-grade scores affect the Math and reading scores by grade

The replacement did not change the math and reading scores by grade as it is shown in the above dataframe.  The summary tables display `NaN` for 9th grade at Thomas High School but the remaining data is intact.

### Average Math Scores by Grade and School: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_mathscores_grade.png)

### Average Reading Scores by Grade and School: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_readingscores_grade.png)

5. How does replacing the ninth-grade scores affect the scores by school spending

Thomas High School is categorized in the range of spending between $630 - $644 per student, and as it is display in the above dataframe, the scores for this range of spending does not change.

### Math and Reading Scores by School Spending: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_schoolspendingSummary.png)

6. How does replacing the ninth-grade scores affect the scores by school size

As it was shown in the previous dataframes, the Medium school size range is not affected by the replacement of the scores for the 9th grade of Thomas High School.

### Math and Reading Scores by School Size: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_schoolsizeSummary.png)

7. How does replacing the ninth-grade scores affect the scores by school type

Regarding the School type, there are only two types: Charter and District. Thomas High School is a Charter school and as it is shown below, the scores does not change.

### Math and Reading Scores by School Type: 
![district_df](https://raw.githubusercontent.com/LeidyDoradoM/School_district_Challenge/main/Images/df_schooltype.png)

## Summary

This new analysis after the replacement of math and reading scores for the 9th grade at Thomas High School shows that this replacement has a very minimum impact on the scores and percentages for all schools in the district. The replacement makes that the overall percentage for the entire district drops 0.1 units, which is expected since the universe of samples, i.e. the total number of student in the school district is 39,170 and the number of data samples we are not considered in the analysis is only 461.  Likewise, when we do the same analysis for the specific school, *The Thomas High School*, we found that the overall passing percentage drops from 90% to 65%. This drastic change, is explained also following the same thinking, but in this case the students considered in the computation are the ones from the Thomas High School, which is only 1,635. Therefore, the 461 students whose scores are not considered has a major impact on the results.  
On the other hand, when we perform the analysis for the Thomas High School considering that its total number of students are those only in 10th-12th grades, its math and reading scores and their respective percentage are back at the same range of values and percentages as before the replacement, which makes that the other comparatives such as: **average scores by school size, school type, school spending**  do not change at all.