```	
Notes on Error logs and Software development 
```	

Logs
==== 

Specific estimate
	1. Loc - Lines of Code  { definition is your rules, see rules} 
	2. How long in minutes
	3. number of errors 

time logs.
start stop reason #loc.

Error log,
================
what, when discovered, when corrected


Example of error log
=================
```
What | When discovered | when corrected
missing ;| complication | compile
illegal data | on execution
```
Common Errors Key 
=============
Key your common errors
IE: miss of semi colons and etc

-new 
-reused 
-new modified
-deleted

General
========
-Recommendation to get specifications and requirements. 	
-Finding requirements are easier than expected	
-Don't screw people, be genuinely with requirement 	
1. Would like to haves	
2. Optionals 	
3. If they doing math, can you write and convert the logic,
	-Do you have an algorthim, a solver, a methodology? 	
	-Test Cases
		-Limits
		-Cases
		-Bounds
4. Due in two Weeks from today
Assignments yo. 
	-Story card generation 	
	-6 or seven total	
	-identifying story cards.	 
	-word doc, two coumns	
		-Approximate what you can fit in a 3x5 card
	-story card for your estimate generations
5. google the waterfall model -> waterfall 
	80% costs is non-trivial cost is updating and modifying it 

Story cards requirements->

WaterFall 
```
R -Requirements
A -Analysis
D -Design
C -Coding 
T -Testing 
A -Acceptance 
```
Problem 
-------
Colinear it is a trangle formed colinear
If it is not display
Story Cards->	
```
	S1000 use is protect with a menu of options	 
	-------------------------------------------		
		1. enter known coordinates	
		2. generate randoms		
		3. quit	
```		
```
	-T1000 -(testing)		
	-------------------		
	-T1000 input the for #1	
	Out of range for menu 	
```

example
Story 
```
S1001 
	The user is prompted to enter three coordinates to a 3D (x,y,z) domain
	and the values are between -100 < x < 100
```
Testing

```
T1001
test often reliability of range data

```

S1001
````
The user enters the decimal 
coordinate of 3 points in 3rd space with value -100 < x, y,z <100

	Jump go to story card 
	(S1003) 
````

(S100)
`````
Once validated as described, a plan then the type of triangle is listed accoridng to design specs'

```

Recitations 
===============


Error Logs 
----------
Current Reports
--------------
-x
	1. actuals
	2. estimates
	3. rel errors
-y
	-actuals
	-estimates
	-rel errors

Grand totals
--------------
-x
	1. actuals
	2. estimates
	3. rel errors
y
-sum of all actuals
-estimates sums 
-relative errror toal


y=mx+b
Lines of code  (2200/5000(5250)

error formula = 
((estimate lines of code/estimates time )* actual lines of code) = estimate line of code

y = ((EL/ET)*AT)=PLOC margin of error 

Estimation = time 5000
Actual time = 5250 
Lines of Code estimate = 2310
Lines of code actual  = 2200