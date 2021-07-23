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

As seen from the above dataframes, the removal of the scores of Thomas High School's 9th-graders pulled down slightly the average math scores (79.0 to 78.9) and the percentage of students passing math (75% to 74.8%) and passing overall (65% to 64.9%). This can be attributed to substitution of higher-than-average scores by NaNs in the math category, subsequently changing the percentages of passing students. There was no noticeable change in the average reading score, hence, no noticeable change in percentage of students passing reading.


### School Summary Analysis

### Thomas High School's Performance Compared to Others'

### Math & Reading Scores by Grade Analysis

### Scores by School Spending Analysis

### Scores by School Type Analysis


## Summary

To summarize, the following lists four major changes in the updated school district analysis after reading and math scores for Thomas High School's 9th grade have been replaced with NaNs:

1. 
