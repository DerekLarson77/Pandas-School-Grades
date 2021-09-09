# Pandas-School-Grades

Two CSV files were used.  One file contained information about different schools.  The other file was at the student level and had every student at every school.

1)  Building a dataframe of the district summary with only one row of data.
	Each column value was calculated from the CSV file and then saved to a variable to then be used to create the value of our one row dataframe.

2)  Building a dataframe of the school summary.  This consisted of a row for each school.
	A dataframe was created with all the columns that were already in the csv file at the school level.  
	The student level values were done by group bys and various math equations and then reformatted for currency values, percentages and rounding.

3)  The top 5 best performing school by Percent Overall passing.
	The School Summary dataframe was taken and then used sort_values with ascending=False.

4)  Top 5 worst performing school by Percent Overall passing.
	The School Summary dataframe was taken and then used sort_values with True.

5)  Math scores broken down by grade for each school.
	A group by of school and grade was done to create two indexes.  Then iloc was used to find each schools average value for math and reading by each grade
		to create a new dataframe.  The four dataframes of each grade were then merged together by school name.
	From the merged dataframe the math score columns were extracted to create the math scores by grade dataframe.

6)  Reading scores broken down by grade for each school.
	From the same merged dataframe the reading score columns were extracted to create the reading scores by grade dataframe.

7)  Scores by School Spending.
	Bins were made to segragate four levels of average school spending per student, and then a groupby was done based on new bin names.
	![image](https://user-images.githubusercontent.com/80318883/132770806-0faf3559-4e7d-464d-a692-a5ea65a6e96d.png)


8)  Scores by School Size.
	Bins were made to segragate small, medium and large schools and then a groupby was done based on new bin names.
	![image](https://user-images.githubusercontent.com/80318883/132770769-bb8a7c2e-71fc-4e81-bd58-6dc6a327236d.png)


9)  Scores by School Type.
	There were only two types in the dataset:  Charter and District.  Since they were a string no bin was used and just a groupby was used.
	![image](https://user-images.githubusercontent.com/80318883/132770740-c8fce91a-96fd-47c1-8e2d-8d5a493c2ab8.png)


The average reading score was higher than the average math score in almost every school and grade.
Both the math and reading average scores stayed roughly the same between grades.  There tended to be a tiny decline in the higher grades compared to 9th grade.
	
Contrary to the expectation, but both math and reading had higher average scores and much higher % passing in the bins with fewer spending per student.
The small and medium sized schools had simiar scores and passing % across the board, but the large schools were lower in averages due to having a much lower % passing.

The Charter and District schools were fairly close in average reading score, but a good distance from average math scores.  The % passing math and reading were a complete landslide in favor of Charter schools.


