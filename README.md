# VPD_Analysis
##Vapour Pressure Deficit Analysis and Forecasting for Six Cities in United States

##Introduction 

Environmental Conditions and Health an Analysis of VPD and Humidity in 6 Student Athlete Suicides.
Recent the Journal of the American Medical Society September 2022, published an urgent plea for action to combat the delirious effects of Global Warming and health.  We started the process of studying VPD in the Winter of 2018.  We were motivated by an outbreak of C. Auris which took the lives of four patients in a nursing home in New Jersey.   Our approach was to find a method of measuring humidity that could explain the mysterious occurrences of C. Auris infections.   We decided that the common index used in greenhouses could be a valuable index of patterns of humidity and temperature.  
What we found was that VPD changed significantly during certain months.  For example, in 2019 the VPD for October was significantly lower than in September, Average 1.441 vs 1.1212, t=5.09 p value <.001.  We conducted several other t-tests on our data set and substantiated the findings that VPD fluctuates significantly on a month-to-month basis.  Furthermore, given its ability to cause the propagation of vegetation we hypothesize that it also can encourage the growth of fungi and mold (see references).
In March and April (2019 to 2022) there were three student Athlete Suicides:
•	Katie Meyer (March 11th, 2022)
•	Robert Martin (April 1st, 2022)
•	Jayden Hill (April 3rd, 2022)
•	Sarah Shulze (April 13th, 2022) 
•	Kelly Caitlin (March 7th, 2019)
•	Lauren Bernett (April 26th, 2022) 

Katie Meyer was born on January 20, 2000. She was an American Soccer player who played as a goalie for Stanford University’s Cardinal Women’s soccer team. She started at Stanford University in 2018, getting her degree in International Relations with a minor in History. The 22-year-old was found dead in her on-campus residence, and authorities determined she died by suicide. Mr. and Mrs. Meyer believed that a pending disciplinary hearing may have been a factor.

Robert Martin was a graduate student at SUNY Binghampton New York. He played Lacrosse for his University as a Goalkeeper. He earned first team all leagues honor. He died on April 1st, 2022.

Jayden Hill age 19 died on April 3rd, 2022. She was born in Monrovia, Liberia. She was pursuing a degree in Political Science with a concentration in pre-law at Northern Michigan University. She was a Track Athlete for NMU Wildcat Athletics.

Sarah Schulze committed suicide this spring was age 21 on April 13th, 2022.  She ran indoor and outdoor tracks.  She attended the University of Wisconsin in Madison. She earned Academic big ten honors in 2020 and 2021.  She was an intern for the Wisconsin legislature and volunteered as a poll worker for the 2020 presidential elections. While attending Oak Park High School in California she won the Division 3 1600- and 3200-meter finals at El Camino College.

Catlin Kelly died on March 7th,2019 by suicide at age 23.  She was born in St. Paul Minnesota. She died in her dorm at Stanford University.  She studied computational and mathematical engineering. She played the violin.  She won 34 medals, 34 gold, 7 silver and 1 bronze in major international competitions.  On January 5th, 2019, Kelly had a concussion due to a fall during training.  

As a result of these mysterious suicides in the Spring of 2019 and 2022, we began investigating the VPD in the cities where these high-profile suicides occurred. 

Lauren Bernett is a Softball Player representing her University James Madison University in Wisconsin. She was born in Virginia, United States. She was a Standout player for the University and was awarded the CAA softball player of the year. She died of a heart attack on April 26th, 2022.

What is VPD?

VPD stands for Vapor Pressure Deficit, i.e., difference or deficit between the amount of moisture in the air and how much moisture the air can hold when it’s saturated 
In simple words we use VPD to determine if the weather is too moist or too dry.

Keys Highlights of VPD: 
VPD is calculated using two important factors viz. Temperature and Relative Humidity.
Temperature is Directly Proportional to VPD Score and Humidity is Inversely Proportional to VPD Score.
Formula:
(6.1078*exp (Temp/(234.175 + Temp)*17.08085)*(1- Humidity/100))/10
VPD Score Range:
0.8 - 1.2 Kilo Pascal: Ideal Range 
Below 0.8 Kilo Pascal: Too Moist
Above 1.2 Kilo Pascal: Too Dry 

VPD Analysis for all Six Cities
•	Palo Alto
•	Johnson City
•	Marquette
•	Madison
•	Weyers Cave 
•	Philadelphia 

VPD Actual Dataset:
https://wwo-bulk.s3.amazonaws.com/hwd_order_2487.zip

Code Explanation: (Only Explaining for Palo Alto City Cause Code is similar for other Cities too, The Whole Project is Done in Python Language, Jupyter Notebook)

Data Extraction:

This is Data Extraction Part where we Read the Data from an Excel File

Over here we have only extracted Important Features required to build the Model

We have used VPD Formula, Inserted VPD as an Extra Feature in the Dataset for the Model 

Data Description:

This is a Brief Summary of our Data. Over here we can see all the Ranges of Quantiles for VPD score. Mean and the Median for VPD score. Min Max and Standard Deviation for VPD score.

Data Visualization:

These are the Yearly Averages for VPD for all Years Data

We have now Displayed Yearly Averages for VPD for all Years Data

This is the Rate of Change of VPD per Year which shows a Line Plot on each Scattered Values Present in Dataset  
 
This is the Box Plot for the Dataset
 
This is a Correlation Heat Map where we have Displayed the Correlation between All Important Features

This is a Relational Plot which indicates the Rate of Change of VPD per Year for Specific Months where Lighter Shades are earlier Months of the Year and Darker Shades are Later Months of the Year

Data Analytics Using Linear Regression Model:

Here, we have used VPD as our Target or Dependent Variable and Temperature and Humidity as our Independent Variables. In short, we are going to use Temperature and Humidity Features to Predict VPD Outcomes in the Linear Model. Over Here we are going to use Linear Regression Model.
 
What is Liner Regression?
Linear regression analysis is used to predict the value of a variable based on the value of another variable.

Why do we use it? 
To Determine the Strength of the Predictor Variable (e.g., VPD in this case scenario) 

Where do we use it?
Forecasting an event or Trend Forecasting (e.g., Weather Forecasting in this case scenario)

Linear Regression Formula:
y = m * x + c
where,	y is the Outcome Variable 
	x is the Independent Variable 
	m is the Slope 
	c is the y Intercept

How Linear Regression Model is used in our Project?

We have two Independent Variables Temperature and Humidity, and we have One Outcome Variable VPD. So, the Formula is,
y = m1 * x1 + m2 * x2 
where, y is the VPD prediction
	x1 is Temperature Variable
	x2 is Humidity Variable 
	m1 is Temperature Coefficient
	m2 is Humidity Coefficient

Verification of the Model:
Given: 	x1 = 75 
	x2 = 60
	m1 = 0.0289
	m2 = -0.0169
	c = 0
To Prove: y = 1.154
Proof:
y = m1 * x1 + m2 * x2
   = 75 * 0.0289 + 60 * (-0.0169)
   = 2.1675 – 1.014
   = 1.154 
Note:	 x1 and x2 are Values obtained from x_test table
m1 and m2 are Values obtained from OLS Regression Table
y is obtained from prediction table 

Results: 
There is a Linear Growth in VPD every year for Palo Alto and Philadelphia.
This means that, Temperatures are rising every year in these 2 cities and Humidity is decreasing Significantly. 
In the above Pages or Slides we Proved that Global Warming is Linearly Increasing every year in these 2 Cities.
We do not see any Significant Change in VPD for other Cities.
What did I Learn?
I Learned what is it meant to do a Research Project and Dive Deep into every aspect or Features that are Important. 
I Learned that I don’t know a lot of stuff in my own field and realized that I have a lot of scope to Learn and Practice for the rest of my Life. 
I learned that we cannot neglect Global Warming Trends and we should care about Climate Change.
 I realized that VPD is a very Significant Factor to Forecast Global Warming Trends.
 My Data Visualization Skills improved in this Project. 
I learned that the ability to explain your Project by giving simple analogy to 15 years old is Far Greater than What Skillsets you Possess.    
Was I Successful?
I would say Partially Successful. 
Yes, I was Successful in getting an Output. 
I was Successful in showing a trend and Proving my Point.
 But this Project felt like an Incomplete Project. 
I hardly few months to execute this project. 
What I did was Normal Weather Forecasting, but I wanted to do something more beyond that. 
My purpose in this Project was to show what factors affect Suicide in Professional Athletes, but I was able to work on only one factor viz, VPD or Global Warming Factor but couldn’t involve other Important Factors that do cause Suicides.
 If I didn’t have any Time Constraints, I would have tried to add a minimum of 5-6 more features that cause Suicides. 















