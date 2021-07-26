# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Civic data analyses

## Due July 26th @ 9am

## Problem Statement and Business Case for the Mayors of California

As you know,the mayors of California have hired me to answer the question of how to move the needle on high school education outcomes. Today I am focusing on the ACT versus SAT and how it affects you. Standardized tests provide only a snapshot of student performance. These snapshots often define whether the educational agenda of each of your programs is successful. With this in mind, this data analysis seeks to benchmark which test the state of California should institute as a requirement for its high school students. The SAT and ACT  are compared to determine which test best reflects the achievement of California's students and which test results should be promoted to support your political agenda.

Recommendation:the ACT should be the required test.

## Table of Contents in the Repository

A Jupyter Notebook: showing the detailed calculations and analysis.

Data Sets: this is the data received from the state of CA that was used as the basis for analysis. They include the original CA datasets. It also includes my copy and alteratioons.

Slides for this presentation

And this Readme.md

---

## Analysis and Conclusions

The ACT should be the required test that we tout. While this is the bottom line, I must share that these are inferences based one snapshot of CA detail. The same testtakers may score differently on each test. Moreover, small school data was held back because disclosing the data would disclose the identity of the children who took these tests. Moreover, there is no way to be sure whether the people who took the SAT and ACT were the same children. It could be different populations taking different tests. A future scientist might take the ACT as there is a science section whereas SAT has no section labeled science. Furthermore, I had difficulty slicing county, district, and aggregate data. The results I report are based on individual high schools. According to a google search of the number of high schools in CA, there are 3,892 high schools there. This dataset started at about 2500 and that included repeated county data. Moreover, there were missing values that were dropped or hidden for privacy reasons.

Even with these limitations, the data support my initial statement regarding the ACT. While there are differences in the tests, it should not surprise us that they are related. A measure of how directly or inversely related the tests are is correlation .899 is the correlation between the percent that score 21 or above on the ACT and the percent that meet the minimum standard or above on the SAT. The highest correlation can be is 1.000 or -1.000. The least would be 0.. This is a relatively high number. This is not surprising as both are measures of academic knowledge.

Here are the differences. In looking at the histograms, SAT is skewed positively while the ACT has no real skew. The ACT does appear to have larger ends. The ACT has a higher mean or average, 52%,for percentages of passage than the SAT mean or average of 45%. This would suggest that the 'easier' number to achieve is the ACT since more students reach it. If you can tout a higher average, you will have greater credibility. Another observation is that the passage rates for the SAT have lower variance or to state otherwise, ACT has more variance. The standard deviation of approximately 26 and the variance of 676 for the ACT compared to 23 and 529 for the SAT. In laymen's terms this suggests a greater spread between the testakers in the achieved amount. This observation means that the ACT does a better job of separating students, showing their difference.This helps educators categorize. In addition, the higher variance suggests risk evaluation should be a key element in your decision. If you wish to be aggressive and are committed to massive educational policy change, the ACT is better as you could be further away from the mean. It will allow you to show a greater change, assuming the program is succesful in comparison to the rest of the state. However, if you wish to be conservative and are not as interested or don't believe there will be much progress, the SAT is better. It is more likely that it will hug the center. Given your desire to move the needle, I would recommend that you mandate the ACT. It seems to be easier test or the standard is less than the SAT. If progress is more finely measured as suggested by the ACT's variance, this would give you the chance to show your education rogram will make progress. Either way, politically, you would win and increase your political capital.

In conclusion, I urge you to mandate and tout the ACT.
   

### Data Dictionary

Variable/Feature	             Type	         Dataset	              Description
county_district_school_code	=   float64	         ACT	   This is a unique identifier for each school by county, district, and school codes in California.

county_code	=                   float64          ACT       This is the unique identifier for counties in California.

district_code=	                float64	         ACT	   This is the unique identifier for each school district in California.

school_code	=                   float64	         ACT	   This is the unique identifier for each school.

record_type	=                   object	         ACT	   The four values are C,D,S, & X, signifying where the information came in the data set. There is duplicate data as the schools are listed, then by county, and finally the state of California aggregate. C=County D=District S=School X=State

school_name	=                   object	         ACT	   This is the school's name
district_name	                object	         ACT	   This is the school district's name. If N/A is there, it may be a county level record.

county_name=                    object	         ACT	   This is the county's name.

_12th_grade_enrollment=    	    float64	         ACT	   The number of students enrolled in 12th grade in each unit whether it be school, county or state.*

test_taker_count=               float64	         ACT       The number of test takers at each unit.

average_reading_score=          float64	         ACT	   The average score on the reading section of the ACT at the school, county, or state level.

average_english_score	        float64	         ACT	   The average score on the English section of the ACT at the school, county, or state level.

average_math_score	            float64	         ACT	   The average score on the math section of the ACT at the school, county, or state level.

average_science_score	        float64	         ACT	   The average score on the science section of the ACT at the school, county, or state level.

number_of_composite_results_21andup=float64	     ACT	   There are four sections on the ACT:reading, English, math, and science. These four sections are added together for the composite result. This lists the number of students who scored 21 and up.*There are four sections on the ACT:reading, English, math, and science. These four sections are added together for the composite result. This lists the number of students who scored 21 and up.

percent_of_composite_results_21andup=float64	 ACT	    There are four sections on the ACT:reading, English, math, and science. These four sections are added together for the composite result. This lists the number of students who scored 21 and up.*There are four sections on the ACT:reading, English, math, and science. These four sections are added together for the composite result. This lists the percent in decimal value of students who scored 21 and up.

county_district_school_code	   float64	         SAT	    This is a unique identifier for each school by county, district, and school codes in California.

county_code	                   float64	         SAT	    This is the unique identifier for counties in California.

district_code	               float64	         SAT     	This is the unique identifier for each school district in California.

school_code	                   float64	         SAT	    This is the unique identifier for each school.

record_type	                   object	         SAT	    The four values are C,D,S, & X, signifying where the information came in the data set. There is duplicate data as the schools are listed, then by county, and finally the state of California aggregate. C=County D=District S=School X=State

school_name	                   object	         SAT	    This is the school's name or a county or district record.

district_name	               object	         SAT	    This is the school district's name. It may be a county level record.

county_name	                   object	         SAT	    This is the county's name.

_12th_grade_enrollment	       float64	         SAT	    The enrollment of Grade 12.

test_taker_count_12thgrade	   float64	         SAT	    The number of 12th Grade test takers.

number_that_passed_reading_writing_standard_12thgrade
                               float64	         SAT	    The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 12.

percent_that_passed_reading_writing_standard_12thgrade	
                               float64	         SAT	    The percent in decimal value of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12.

number_that_passedorabove_math_standard_12thgrade	
                               float64	         SAT	    The number of students who met or exceeded the benchmark for the New SAT Math test format as of March 2016 for Grade 12.

percent_that_passedorabove_math_standard_12thgrade	
                               float64	         SAT	    The percent in decimal value of students who met or exceeded the benchmark for SAT Math test for Grade 12.
                               
_11th_grade_enrollment	       float64	         SAT	    Enrollment of Grade 11

test_taker_count_11thgrade	   float64	         SAT	    Number of Test Takers Grade 11

number_that_passed_reading_writing_standard_11thgrade	
                               float64	         SAT	    The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 11.
                               
percent_that_passed_reading_writing_standard_11thgrade	
                               float64	         SAT	    The percent in decimal value of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 11.
                               
number_that_passedorabove_math_standard_11thgrade	
                               float64	         SAT	    The number of students who met or exceeded the benchmark for SAT Math test for Grade 11.
                               
percent_that_passedorabove_math_standard_11thgrade	
                               float64	         SAT	    The percent in decimal value of students who met or exceeded the benchmark for SAT Math test for Grade 11.

number_that_passed_both_12thgrade	
                               float64	         SAT	    The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.

percent_that_passed_both_12thgrade	float64	     SAT	    The percent in decimal value of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.

number_that_passed_both_11thgrade	float64	     SAT	    The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.

percent_that_passed_both_11thgrade	float64	    SAT	        The percent in decimal value of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.

---
