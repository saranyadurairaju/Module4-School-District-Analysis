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

![image](https://user-images.githubusercontent.com/85472349/125236251-43d03100-e2a9-11eb-84a9-84b90df33688.png)
	
* With the new count of Thomas High School, we need to find the Math, Reading and over-all percentages of it for the School Summary Analysis.

Impacted values due to the Full school count

![image](https://user-images.githubusercontent.com/85472349/125236484-ab867c00-e2a9-11eb-8f70-f47453f718c6.png)

Corrected values with the updated number of students (10th, 11th, 12th)

![image](https://user-images.githubusercontent.com/85472349/125236514-bf31e280-e2a9-11eb-9578-27c849772889.png)

* Finally we need to find the High & Low Performing Schools, Math & Reading Scores by Grade, Scores by School Spending, School Size & School Type with the updated DataFrame. 

## Results

Below is the full Pandas code to determine the City School Analysis. 

![PyCitySchools_Challenge](.ipynb)

Herewith we are comparing the Original value with the New value which we got with the 10th, 11th, & 12th students count of Thomas High School
 
#### The District Summary

Below are the district summary before and after changing the Math & Reading scores of 9th grade Thomas High school. If we compare the results, we couldn't find much difference and we are calculating the data with right number of students. Means, total Number of students minus 9th grade Thomas High School students. 

Original Value

![image](https://user-images.githubusercontent.com/85472349/125211129-cdf8a500-e269-11eb-9cf3-c406dc47b36d.png)

New Value

![image](https://user-images.githubusercontent.com/85472349/125211151-04cebb00-e26a-11eb-912a-0e395ef6e641.png)


#### The School Summary

We are calculating the remaining students count of Thomas High School and replacing the School summary for those students. So, Passing Math, Reading and Overall Scores are replaced for this particular school.

![image](https://user-images.githubusercontent.com/85472349/125233872-171a1a80-e2a5-11eb-823c-7660af7729fd.png)

Original Value

![image](https://user-images.githubusercontent.com/85472349/125235509-2f3f6900-e2a8-11eb-9ed8-b33d4e71c6d0.png)


New Value

![image](https://user-images.githubusercontent.com/85472349/125233966-4f215d80-e2a5-11eb-99f0-a229260e4d99.png)

### School Performance impact after changing the Math & Reading scores

There is no much difference in the school performance after the change as the data set is huge and the total number of students from Thomas High School has been replaced with the School Students from 10th, 11th and 12th grades.

#### High and Low Performing Schools

No change in any schools after the value change. And Thomas High School managed to attain the same 2nd position after the change too.

![image](https://user-images.githubusercontent.com/85472349/125234310-12099b00-e2a6-11eb-93d6-dcec142530fd.png)

#### Math and Reading Scores by Grade

Since 9th grade scores are changed to NaN, only the Reading & Math scores of "Thomas High School" 9th grade values are changed to NaN compare to the original values.

![image](https://user-images.githubusercontent.com/85472349/125234619-ad9b0b80-e2a6-11eb-9d6b-b6e0777d59a4.png)
![image](https://user-images.githubusercontent.com/85472349/125234677-c73c5300-e2a6-11eb-8e1a-d06f8e2598fa.png)

### Score Values

The bins have been created and Valued based on many criteria like School Spending, School Size and School Type. But since the change in the values are very very minimal after the update of Reading & Math Scores, there is no impact in any Score Values.

#### Scores by School Spending

![image](https://user-images.githubusercontent.com/85472349/125235082-81cc5580-e2a7-11eb-8934-20930b78bf7d.png)

#### Scores by School Size

![image](https://user-images.githubusercontent.com/85472349/125235128-914b9e80-e2a7-11eb-8f6c-ee48147f4647.png)

#### Scores by School Type

![image](https://user-images.githubusercontent.com/85472349/125235157-9f012400-e2a7-11eb-9828-aa8f2f8c07e6.png)


## Summary

* There is a very minimal change in Passing Percentages in the district summary report.

* Same way in the School Summary report, the values are impacted little bit.

* Math and Reading scores by Grade is replaced with NaN for Thomas High School.

* After the changes in Data, there is no impact in Top Performing schools and Score Values. 

* But we need to find the right number of Students during every Value calculation is important. 

_Maria and her team can provide a nice and perfect **City School Analysis Report** with Clean Data to the School Board. Hurry!!!_



