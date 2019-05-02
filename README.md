### Where should the money go? 
### An analysis of school district fiscal data and student dropout rate
Chun Xie, Xuehan Chen, Yimin Xiao, Yue Wang

#### First part: project description

1.  Area: Education finance
    
2.  Problem: There is a persisting inequality of school funding in the United States (NCES) and the student dropout is also a crucial issue. There has been analysis on whether education finance can affect student achievement (Neymotin, 2010) and cause resource disparity in different races (NBC), but few studies tried to look at how it affects students’ continuity in education.
    
3.  Importance: Understanding the influence of fiscal factors on student dropout rate can help make better government funding decisions and school district budget plans to support students’ continuity in education and increase policy efficiency.
    
4.  Objective: Predict school district’s dropout level based on its fiscal information.
    
5.  Expected result: A 4-year prediction model of grade 9-12 dropout level in U.S. school districts based on its fiscal data. A classification model of whether a school district will have a high or low dropout rate based on its fiscal data.
    
6.  Relevance: The result can be used to help school district take precautions in budgeting if dropout rate is estimated high. It can also help government to make better fiscal policy to support school districts facing student dropout problems.
    

#### Second part: more details about the goals of the project

 1. Data preparation 
	
	Tasks:

	-   Find school-district-level fiscal and dropout data
    
	-   Understand the data content and perform a preliminary data exploration
    
	-   Clean the data and join data from different sources so that it is ready for analysis
    
    Expected results:
	-  A cleaned data set with fiscal data as input values and a certain measurement of dropout level as the output value 
	
	Expected problems:

	-   How to deal with missing values and outliers
    
	-   How to deal with special labels used in the source data
    
	-   How to join data gathered from different sources
    

 2. Model building, cross-validating, and testing 
	
	Tasks:

	- Separating the data into training, validating, and testing part
    
	-   Data modeling, cross validation and model selection, model testing 
	
	Expected results:
    

	-   Different models for prediction and classifying
    
	-   Choosing the most optimal model based on validation performance
    
	-   Testing result of the model chosen
    
    Expected problems
    
	-   Noise in the data: can the models capture the relationship
    
	-   Trade-off between accuracy interpretability: can we get a model that can give an accurate estimation of the relationship and also can be inferenced?
    
	-   Feature selection: Too many features in fiscal data, and some are intercorrelated
    

 3. Inference and prediction 
	
	Tasks:

	-   Understanding the relationship between fiscal factors and student dropout rate
    
	-   Interpreting models or analysis result in the context of education and fiscal policy making and making actionable suggestions 
	
	Expected results:
    
	-   Explanation on how school district revenue and expenditure affect dropout rate
    
	-   Suggestion for government on what types of districts to give more funding
    
	-   Suggestion for school districts on where to spend the money
    
    Expected problems:
    
	-   Difficulty to extract actionable suggestions from the analysis result
    
	-   Lack of domain expertise, an understanding of education and finance for public institutions
    
   #### Third part: data set, tools, models, model selection
 
1. Data set: We have two types of dataset. One is for fiscal data, and the other one is for dropout data. They can be joined by “LEAID”, a local education agency id, which is a unique number given by national center for education statistics. The fiscal dataset has more than 80,000 observations and 256 variables, categorized by district basic information, different types of revenue, different types of expenditures, salaries, textbooks, etc. The drop out dataset has 10 variables, which is mainly about drop out information. The data is retrieved from the National Center for Education Statistics Website (https://nces.ed.gov/).
    
2.  Tools: Spark MLlib
    
3.  Models: Linear regression, logistic regression, svm, random forests
    
4.  Criteria for model selection: Cross-validation, mse, confusion matrix, precision, recall, f score
    

#### References:

1. NBC News. 2018. ‘Segregation, school funding inequalities still punishing Black, Latino students’, NBC, Retrieved online on 02/19/2019 via https://www.nbcnews.com/news/latino/segregation-school-funding-inequalities-still-punishing-black-latino-students-n837186.

2. Neymotin, F. 2010. ‘The relationship between school funding and student achievement in Kansas public school’. Journal of Education Finance: 36-1, pp. 88-108. Retrieved online on 02/19/2019 via https://www.jstor.org/stable/40704407.

3. NCES (National Center for Education Statistics). ‘Education equity in the States’.Inequalities in public school district revenues, Chapter IV. Retrieved online on 02/19/2019 via https://nces.ed.gov/pubs98/inequalities/chapter4.asp

<!--stackedit_data:
eyJoaXN0b3J5IjpbNTU3MjkzMDIyXX0=
-->
