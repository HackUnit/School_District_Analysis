# School_District_Analysis

##Analysis on a School District.

###Overview of the school district analysis:

This project began as a task from a School District that took in data from each of its schools in the district. The key metrics included each schools budget, size, academic performance per grade on reading and math, and type of school. This data was inspected, cleaned and sorted with a variety of code. These clean datasets were then used to generate a summary on the overall School District, and then specifically generated the School Summary. Further analysis was performed before sending in the completed dataset. This dataset was found to show acedemic dishonesty; specifically, reading and math grades for Thomas High School ninth graders seems to have been altered. To uphold state-testing standards the data was reparsed and analyzed to correct the problem and provide a final complete analysis.


##Results:

### Replacing the 9th grade scores for NaN

The second analysis to provide an actual complete analysis started with exchanging the incorrect values for NaN values in the ninth-grade reading and math scores. This was done using the `loc` method and various operators to retrieve and replace the necessary values.

![Image of the replaced THS performance NaN](/Resources/THS_ninth_grade_fix_NaN.png)

- Replacing the ninth graders’ math and reading scores dropped Thomas High School out of the top of the summary by overall passing percentage.

- Thomas High School's passing percentage dropped to 65%.

- The district summaries overall passing percentage dropped to 64.9%


### Removing the Thomas High School 9th grade scores

The data was then sorted to create a new DataFrames revolving around Thomas High School. To start, the number of 10th-12th grade students was collected, then new DataFrames were created that had all of those collected students passing reading, and math separately, and then passing reading and math together. These counts were then converted into percentages respectively. Using the `loc` method the "% Passing Math", "% Passing Reading", and "% Overall Passing" score for Thomas High School was replaced with the new calculated percentages.

![Image of the refactored Thomas High School without 9th grade scores](/Resources/THS_school_summary_analysis_post_removing_9th_grade.png)

- Removing the ninth graders' math and reading scores and refactoring the analysis showed that Thomas High School was back at the top of the overall passing percentage.

- Thomas High School's passing percentage raised to 90.6%.

- The district summaries overall passing percentage raised to 65.2%.

### Effects on High and Low Performing Schools

![Image of Top Five Schools Before](/Resources/Top_five_schools_before.png)

DataFrame of Top Five Schools Before re-analizing the data.

Since the data had been corrected, the dataset further needed to be re-analized. To start the highest and lowest performing schools was re-calculated.

- With the NaN values, Thomas High School's overall passing moved down in decimal points.

- Thomas High School's overall passing percentage moved just 0.317688% down.

![Image of Top Five Schools After](/Resources/Top_five_schools.png)

DataFrame of Top Five Schools After re-analyzing the data.

- Thomas High School was not part of the low performing schools and did not affect these metrics

### Effects on Math and reading scores by grade

The next step was to re-calculate the math and reading scores by grade.

- With the NaN value inserted, besides the "(9th)" grade, all of the other values remained the same in the re-analization.

![Image of post math scores](/Resources/Post_math_scores.png)
DataFrame of Math scores post re-analization.


![Image of post reading scores](/Resources/Post_reading_scores.png)
DataFrame of Reading scores post re-analization.

### Effects on School Spending Scores

![Image of School Spending Post and Original](/Resources/School_spending_post_original.png)
DataFrames of the post and original analization of School Spending.

- The differences between the original and post calculations on school spending per student is about 0.1%, which only really shows in the $630-$645 bin of the overall passing percentage. The data as a whole is not largely affected by the NaN values.


### Effects on School Size Scores

![Image of Shool Size Scores Post and Original](/Resources/School_size_post_og.png)
DataFrames of the post and original analization of School Sizes.

- No difference is found when the School Size scores are calculated.

### Effects on School Type

![Image of School Type Post and Original](/Resources/School_type_post_og.png)
DataFrames of the post and original analization of School Types.

- The only difference shows in the Charter type, since Thomas High School is a charter school type. This change is 0.1% of each Charter metric. The District type was not affected.


## Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs:

- The first change is the "9th" grade percentage has been replaced by NaN. With this change the Thomas High School's passing percentage dropped to 65% and the district summaries overall passing percentage dropped to 64.9%.

- The second change involved removing the ninth graders' math and reading scores and refactoring the analysis. This showed that Thomas High School's passing percentage raised to 90.6% and the district summaries overall passing percentage raised to 65.2%.

- The third change is in regards to the school spending. The change was nominal and only showed up as a 0.1% change in the $630-$645 bin of the overall passing percentage.

- The fourth change is the 0.1% difference between metric values of the original and post analized Charter data type. The Distric data type remained the same over both analysises.

