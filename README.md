# pandas-challenge

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

8)  Scores by School Size.
	Bins were made to segragate small, medium and large schools and then a groupby was done based on new bin names.

9)  Scores by School Type.
	There were only two types in the dataset:  Charter and District.  Since they were a string no bin was used and just a groupby was used.


