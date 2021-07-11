# City School Analysis with Pandas

Pandas Library for Python, provide extremely streamlined forms of Data representation with less writing and more work done. It can efficiently handles large data and makes data flexible and customizable. Pandas also provides several methods for reading data in different formats. 

Jupyter notebooks are great for showcasing your work. You can see both the code and the results, which is helpful while sharing the work with other people. Its very easy to host server side, which is useful for security purposes.

## Overview of Project

Maria is doing the City School System Analysis with students **Standardized Math and Reading Test scores, Budget** for each school under the district. This Analysis will help the School Board to decide on the Budget and Priorities. Maria is interested to find the below details out of the City School Analysis.

  *	The district summary
  *	The school summary 
  *	Top and bottom 5 performing schools, based on the overall passing rate
  *	Average math score for each grade level from each school
  *	Average reading score for each grade level from each school
  *	The scores by school spending per student, by school size, and by school type
 
### Purpose

Maria wants to perform the Analysis based on many criterias with Large number of data and it will be easy to do it with Pandas in Jupyter Notebook. He need to submit the Analysis Report to School Board, to make a clear decision about student funding and standardized test scores. 

Also, she wants to know what happens to all the above analysis results if reading and math grades for one particular school have been replaced with NaNs due to academic dishonesty. 

## Analysis 

Before we start doing our Analysis, we need to setup the depencies Panda and Numpy libraries in our code to work with Data and Calculations.To load the file we are going work with, we can use the path and .read function of Panda. After that cleaning up the data is very important to start the Analysis.

* Replacing Math & Reading Scores with NaN

As there are some academic dishonesty found with 9th graders of Thomas High School, we need to replace the Math and Reading scores with NaN 

![PyCitySchools_THS_Replace](.png)

* Merge the two datasets School Data and Student Data to view all the informations together and for easy calculations. So, we have to calculate the District Summary with the new student count as we replaced the 9th graders scores of Thomas High School with NaN. Below is the step to calculate the new student count.

![PyCitySchools_New_Student_Count](.png)

* After finding the New student count, we have to find "The District Summary" to see the impact after changing the Math, Reading scores of Thomas High School

* We are finding the School Summary with the original school counts and then with the modified school counts (Excluding 9th graders of Thomas High school) to check the impact.

Get the number of 10th-12th graders from Thomas High School (THS).
school_data_complete_ths_df = school_data_complete_df[(school_data_complete_df["school_name"] == "Thomas High School") & 
                    ((school_data_complete_df["grade"] != "9th"))]

student_complete_count_ths = school_data_complete_ths_df["school_name"].value_counts()

school_complete_count_ths = student_count_ths + student_complete_count_ths

	
* With the new count of Thomas High School, we need to find the Math, Reading and over-all percentages of it for the School Summary Analysis.

Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.350937	83.896082	66.911315	69.663609	65.076453

Thomas High School	Charter	1635	$1,043,130.00	$638.00	83.350937	83.896082	93.185690	97.018739	90.630324

* Then finally we need to find the High & Low Performing Schools, Math & Reading Scores by Grade, Scores by School Spending, School Size & School Type. 


## Results

Below is the full Pandas code to determine the City School Analysis. 

![PyCitySchools_Challenge](.ipynb)

Herewith we are comparing the Original value with the New value which we got with the 10th, 11th, & 12th students count of Thomas High School
 
#### The District Summary

Original Value
![image](https://user-images.githubusercontent.com/85472349/125211129-cdf8a500-e269-11eb-9cf3-c406dc47b36d.png)

New Value
![image](https://user-images.githubusercontent.com/85472349/125211151-04cebb00-e26a-11eb-912a-0e395ef6e641.png)

