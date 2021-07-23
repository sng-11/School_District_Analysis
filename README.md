# School District Analysis

## Overview of School District Analysis
The purpose of this project is to create a high-level snapshot of the district's school system to better inform discussions and decision-making for the State Board of Education. School performance trends are extracted from the source data using the Pandas library, in the Jupyter Notebook interface. For example, the education board would like to know how budget per student, school size, and type of school may influence the performance of students. In addition, the code written for this project takes into account the academic dishonety discovered in Thomas High School's 9th-graders. This report aims to investigate how this academic misconduct will affect the high-level school district analysis.

## Key Metrics of Interest to the School Board

- Total number of students
- Total number of schools
- Total budget
- Average math score
- Average reading score
- Percentage of students who passed math
- Percentage of students who passed reading
- Overall passing percentage

## Results

### District Summary Analysis

*District Summary Prior to Academic Dishonesty Adjustment (i.e. no NaNs):* 
<img width="906" alt="old district summary" src="https://user-images.githubusercontent.com/84816495/126802516-a56c24cc-4c8c-4f30-a77d-d24869e487bb.png">

*District Summary After Adjusting for Academic Dishonesty (i.e. reading and math scores for 9th grade at Thomas High School replaced with NaNs):*

<img width="913" alt="New District Summary" src="https://user-images.githubusercontent.com/84816495/126802587-1b5c2e48-f434-42e2-aaf6-7179c411ed0c.png">

As seen from the above dataframes, the removal of the scores of Thomas High School's 9th-graders pulled down slightly the average math scores (79.0 to 78.9) and the percentage of students passing math (75% to 74.8%) and passing overall (65% to 64.9%) across the district. This can be attributed to substitution of higher-than-average scores by NaNs in the math category, subsequently changing the percentages of passing students. There was no noticeable change in the average reading score, hence, no noticeable change in percentage of students passing reading.


### School Summary Analysis

*School Summary Prior to Academic Dishonesty Adjustment (i.e. no NaNs):* <img width="991" alt="old school summary" src="https://user-images.githubusercontent.com/84816495/126833417-27e6b510-e814-45b1-b10b-f7cae9cf658a.png">


*School Summary After Adjusting for Academic Dishonesty (i.e. reading and math scores for 9th grade at Thomas High School replaced with NaNs):* <img width="984" alt="new school summary" src="https://user-images.githubusercontent.com/84816495/126833437-9e09ed13-a342-4dfd-aae8-d1554881feaf.png">

As seen from the above dataframes, the removal of the scores of Thomas High School's 9th-graders changed the average math scores and the average reading scores of the entire school. And these changes are more drastic compared to the district summary because we are looking at a smaller school population. The average math score of THS dropped (83.42 to 83.35) while the average reading score increased (83.85 to 83.90). This is most likely due to higher math scores and lower reading scores being removed. The percentages of students passing math and those passing reading both decreased though, indicating that more "above or equal to 70" scores were removed by the academic dishonesty adjustment. Overall, the passing percentage across the school did slightly decrease from 90.95% to 90.63%.


### Thomas High School's Performance Compared to Others'

THS remained in the top 5 performing schools even after the academic dishonesty adjustment. Although there was a slight decrease in the overall passing percentage (90.95% to 90.63%), it did not move THS from it's spot as the 2nd-highest-performing school.

*Top 5 Schools Prior to Academic Dishonesty Adjustment (i.e. no NaNs):* <img width="987" alt="old top schools" src="https://user-images.githubusercontent.com/84816495/126838132-6817e199-39c0-492b-86af-7c886bf384ce.png">

*Top 5 Schools After Adjusting for Academic Dishonesty (i.e. reading and math scores for 9th grade at Thomas High School replaced with NaNs):* <img width="981" alt="new top schools" src="https://user-images.githubusercontent.com/84816495/126838179-8742ffa0-2e6d-43e8-9592-b5af7f1df0dd.png">

THS did not rank in the bottom 5 performing schools so no changes were observed in that school list after the academic dishonesty adjustment: <img width="987" alt="bottom schools" src="https://user-images.githubusercontent.com/84816495/126838408-1d5b0271-0c2c-4a3a-80f1-d037d7eebbbf.png">


### Math & Reading Scores by Grade Analysis

#### Math Scores By Grade Results

*Math Scores by Grade Prior to Academic Dishonesty Adjustment (i.e. no NaNs):*

<img width="304" alt="old math" src="https://user-images.githubusercontent.com/84816495/126843321-9a5a99a3-a2b6-4e07-950f-8947629f8911.png">

*Math Scores by Grade After Adjusting for Academic Dishonesty (i.e. reading and math scores for 9th grade at Thomas High School replaced with NaNs):* 

<img width="299" alt="new math" src="https://user-images.githubusercontent.com/84816495/126843201-a561de08-2662-49dc-9c34-68e541151d55.png">

As seen from the above dataframes, all math scores by grade remained the same EXCEPT for Thomas High School's 9th grade, which had "nan" replaced for its value. This is because the academic dishonesty adjustment nullified those scores to not be accounted for in the district analysis.

#### Reading Scores by Grade Results

A similar story is observed for the reading scores, where all scores by grade remained the same EXCEPT for Thomas High School's 9th grade, which had "nan" replaced for its value. Again, this is because of the academic dishonesty adjustment. 

*Reading Scores by Grade Prior to Academic Dishonesty Adjustment (i.e. no NaNs):*

<img width="296" alt="old reading" src="https://user-images.githubusercontent.com/84816495/126843603-d73396a1-0dff-478c-8da1-47a0faa885bc.png">

*Reading Scores by Grade After Adjusting for Academic Dishonesty (i.e. reading and math scores for 9th grade at Thomas High School replaced with NaNs):*

<img width="301" alt="new reading" src="https://user-images.githubusercontent.com/84816495/126843615-014bef07-1565-4ef6-b423-eaab667cc246.png">


### Scores by School Spending Analysis

No changes were observed after Thomas High School 9th grade scores were replaced with NaNs. This can be due to the large sample population analyzed within the $630-644 bin (as THS spends $638/student on average), so the changes in grade scores were negligible in the grand scheme of things. The following chart was created in the old and updated school district analysis:

<img width="794" alt="old and new spending same" src="https://user-images.githubusercontent.com/84816495/126844279-29024d49-45be-4b1a-bce4-f1b4b92d9e84.png">


### Scores by School Size Analysis

Similar to the school spending analysis, no changes were observed after Thomas High School 9th grade scores were replaced with NaNs. This can be due to the large sample population analyzed within the Medium bin (as THS has 1636 students), so changes in grade scores were negligible. The following chart was created in the old and updated school district analysis:

<img width="757" alt="old and new size same" src="https://user-images.githubusercontent.com/84816495/126845199-28e9965d-a3fb-40c8-9001-e681a80bc5a9.png">


### Scores by School Type Analysis

Similar to the school spending and school size analyses, no changes were observed after Thomas High School 9th grade scores were replaced with NaNs. This will most likely be due to the extremely large student population and scores taken into account (as THS is a charter school along with eight others), so changes in grade scores were negligible. The following chart was created in the old and updated school district analysis:

<img width="709" alt="old and new type same" src="https://user-images.githubusercontent.com/84816495/126845944-a66e820d-18f9-4049-bd88-9608805476c4.png">


## Summary

To summarize, the following list includes four major changes in the updated school district analysis after reading and math scores for Thomas High School's 9th grade have been replaced with NaNs:

1. Removal of the scores of Thomas High School's 9th-graders pulled down slightly the average math scores (79.0 to 78.9) and the percentage of students passing math (75% to 74.8%) and passing overall (65% to 64.9%) across the district.
2. The average math score of THS dropped (83.42 to 83.35) while the average reading score increased (83.85 to 83.90) after removal of scores of THS 9th-graders. Percentages of students passing math and those passing reading both decreased though, indicating that more "above or equal to 70" scores were removed by the academic dishonesty adjustment. 
3. Overall, the passing percentage across Thomas High School did slightly decrease from 90.95% to 90.63% after taking into account the academic dishonesty.
4. All math and reading scores by grade remained the same EXCEPT for Thomas High School's 9th grade, which had "nan" replaced for those score values (in order to discount them).
