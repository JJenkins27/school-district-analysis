# School District Analysis

Using Python, Jupyter Notebook, and Pandas to analyze school district and student data

## Overview of Project

An analysis of school district and student data to provide insight and determine possible performance trends and patterns. Analysis includes finding the top and bottom schools by percentage of students passing math and reading, average math and reading scores by school, grade level, budget per student and type of school.

### Purpose

Maria is the chief data scientist for a city school district. She has asked for assistance with reporting on school district budget and standardized testing scores. Requested areas of analysis are:
- The district summary with budgeting information, average reading and math scores, and percentage of students passing reading, math, and overall passing rate which equates to passing both reading and math
- The school summary with budget by school, number of students per school, budget per student, and scores as described above
- The top 5 and bottom 5 performing schools based on the overall passing rate
- The average math score for each grade level from each school
- The average reading score for each grade level from each school
- The scores by school spending per student, by school size, and by school type
The information from this analysis will be used to determine school effectiveness, strategic budget planning, and create discussion of school priorities at both the school and district level.

Maria and her supervisor were given information about academic dishonesty at Thomas High School for 9th grade students. Therefore, Maria would like to drop the standardized test scores from the reporting above for all students who meet this criteria. Some information, like total budget and number of students per school will not change. However, scores and percentage of students passing reading, math, and overall passing scores will be affected. 

This analysis will reflect on how the academic dishonesty has changed the data from the original reporting.

## Results

Using the .loc method, the code was updated to replace all Thomas High School 9th graders with NaN or null values rather than just dropping the affected students from the file. This will ensure that the correct number of students for the district and per school will remain intact. 

### School District Summary
#### *Original DataFrame*
![school_district_summary_original](https://user-images.githubusercontent.com/108373151/182000248-e3714b8a-f496-409d-be70-3a0f18feee00.png)

#### *Updated DataFrame*
![school_district_summary](https://user-images.githubusercontent.com/108373151/181996680-381120dd-e322-416a-95d7-83504292318e.png)

As expected, the total number of schools, the number of students, and the total budget in School District Summary did not change. However, the average scores were reduced by eliminating the 461 Thomas High School 9th graders. The differences are not large, considering the eliminated data set is only approximately 1.2% of the total population of the school district.
- Average math score fell from 79.0% to 78.9%
- Due to rounding, average reading score remains the same at 81.9%
- Percentage of students who passed math fell from 75.0% to 74.8%
- Percentage of students who passed reading fell from 85.8% to 85.7%
- Percentage of students who passed both math and reading fell from 65.2% to 64.9%

### School Summary
#### *Original DataFrame*
![school_summary_original](https://user-images.githubusercontent.com/108373151/181996988-f907d501-85ed-4df5-a248-ec2db4235f0e.png)

#### *Updated DataFrame*
![school_summary](https://user-images.githubusercontent.com/108373151/181996688-3111c867-8612-4b6b-91bc-428028c37019.png)

Originally, the formulas were created to calculate percentage passing math, reading, and both math and reading with the total number of students in the school. With eliminating 461 students' testing scores from Thomas High School's data set, this change caused the percentage of students passing math, reading, and both math and reading to decline dramatically. So an update to the formulas was necessary for this school. The scores were recalculated using the reduced number of students. The recalculation brought the numbers back to expected levels for this school.  

![school_summary_revised](https://user-images.githubusercontent.com/108373151/181996691-98fab364-265b-4056-9bb8-06c6932e5bfb.png)

Again, the total number of students at Thomas High School remained at 1,635. Total budget and budget per student also did not change.
- Average math score fell from 83.42% to 83.35%
- Average reading score increased from 83.85% to 83.90%
- Percentage of studends who passed math fell from 93.27% to 93.19%
- Percentage of students who passed reading fell from 97.31% to 97.02%
- Percentage of students who passed both math and reading fell from 90.95% to 90.63%
All other school data remains the same as the other schools were not affected by the academic dishonesty.

### Top 5 Performing Schools
#### *Original DataFrame*
![top_five_original](https://user-images.githubusercontent.com/108373151/181997011-4e194e87-4dc3-4890-b7fe-480a72f1f7ca.png)

#### *Updated DataFrame*
![top_five](https://user-images.githubusercontent.com/108373151/181996707-d4a98bcc-6f56-4783-b314-f6aa0d2f698d.png)

Although the score metrics changed for Thomas High School, the changes were not significant enough to change the relative ranking amongst schools. Thomas High School is still in 2nd place in the top 5 performing schools with an overall passing rate of 90.63% among their 10th through 12th graders.
(One interesting thing to note is all top 5 performing schools are charter schools.)

### Bottom 5 Performing Schools
#### *Original DataFrame*
![bottom_five_original](https://user-images.githubusercontent.com/108373151/181996949-a0a4514b-57fa-4ce1-9e32-88266b920b1b.png)

#### *Updated DataFrame*
![bottom_five](https://user-images.githubusercontent.com/108373151/181996663-96190fb8-46c8-447a-b068-9ee68c30405a.png)

Thomas High school does not appear in this dataset, so there is no change to the bottom 5 schools. 
(One interesting thing to note is all bottom 5 performing schools are district schools.)

### Average Math Scores by Grade Level and School
#### *Original DataFrame*
![math_scores_by_grade_and_school_original](https://user-images.githubusercontent.com/108373151/181996964-c30ca6b8-72a7-4a81-9d1e-d1139b7a1a0f.png)

#### *Updated DataFrame*
![math_scores_by_grade_and_school](https://user-images.githubusercontent.com/108373151/181996670-d2326a9e-0124-471c-a87f-7416eb5fa416.png)

The only change to the average math scores by grade level and school is that NaN reflects in the 9th grade spot at Thomas High School. This is the expected results.

### Average Reading Scores by Grade Level and School
#### *Original DataFrame*
![reading_scores_by_grade_and_school_original](https://user-images.githubusercontent.com/108373151/181996972-4f05468e-552d-4d96-b74b-90d400c5e7a5.png)

#### *Updated DataFrame*
![reading_scores_by_grade_and_school](https://user-images.githubusercontent.com/108373151/181996674-a159c112-d164-4f0c-b4b1-d7df2e455b69.png)

The only change to the average reading scores by grade level and school is that NaN reflects in the 9th grade spot at Thomas High School. This is the expected results.

### Scores by School Spending per Student
#### *Original DataFrame*
![spending_ranges_original](https://user-images.githubusercontent.com/108373151/181997000-50b6db76-9db8-4d72-b08e-c381f5b6fedd.png)

#### *Updated DataFrame*
![spending_ranges](https://user-images.githubusercontent.com/108373151/181996702-e0271915-c8f8-4d87-b8ef-7dc22f9bd5c4.png)

Referring back to the School Summary DataFrame, Thomas High School spends $638 in their per student budget. This places them in the 3rd spending bucket $631-645 per student. Due to rounding, there is no change in the data reflected in the frame.

### Scores by School Size
#### *Original DataFrame*
![school_size_original](https://user-images.githubusercontent.com/108373151/181996980-a92e2e4f-cc7e-4738-b826-0f172c645195.png)

#### *Updated DataFrame*
![school_size](https://user-images.githubusercontent.com/108373151/181996683-26e57164-3ebb-45b4-95f2-f2db8d44969c.png)

Referring back to the School Summary DataFrame, Thomas High School has 1,635 students. This places them in the medium school size bucket. Again, due to rounding, there is no change in the scores.

### Scores by School Type
#### *Original DataFrame*
![school_type_original](https://user-images.githubusercontent.com/108373151/181996993-c5270224-5de3-4bcb-a5e5-b447bfa021e4.png)

#### *Updated DataFrame*
![school_type](https://user-images.githubusercontent.com/108373151/181996696-61226948-b2ce-4625-93d2-8d3916c9a4a6.png)

Referring back to the School Summary DataFrame, Thomas High School is a charter school. Again, due to rounding, there is no change in the dataframe that is reflected by using the reduced number of students.

## Summary

- To summarize, eliminating the 9th grade testing scores at Thomas High School made an impact on the results, but not a very large one. With the eliminated scores only being 1.2% of the total population of the school district, the changes were minimal. The biggest changes to the percentages were noted in the following DataFrames:
	- School District Summary average and passing percentages declined by 0.1-0.3%
	- School Summary average and passing percentages declined by 0.1-0.3% with the exception of average reading scores increased by 0.005%
	- Top 5 Performing Schools with the overall passing percentage changing from 90.95% to 90.63%
	- Math and reading scores by grade reflect NaN in the 9th grade spot at Thomas High School

To view the script in its entirety, please open PyCitySchools_Challenge.ipynb in Jupyter Notebook.
