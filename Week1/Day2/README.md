# Week1 - Day 2

## Problems
#####  - Problem 1
What will be the output?
```
	Integer a,b,c;
	Set a = 2, b = 6, c = 8;
	a = (10 + 9) + c
	if((b + c) > (a - c))
		a = b + c
		b = b + b
	End if
	Print a + b + c
```
	

 #####  Steps
 ```
	 Initialize a = 2,b = 6 and c = 8
	 a = 19 + c => 19 + 8 => 27
	 b + c = 14, a - c = 19
	 if condition failed 
	 a + b + c = 41
 ```
 ##### Solution
 

 - [ ] 23
 - [ ] 31
 - [x] 41
 - [ ] 53

 
##### - Problem 2
What will be output for a = 0, b = 2, c = 10?
```
	Integer funn(Integer a, Integer b, Integer c)
		b = 7 + a
		a = (a + c) + a
		b = (b + b) + c
		c = 1 + b
		return a + b + c
	End function funn()
```
##### Steps
```
	Get a = 0, b = 2 and c = 10 
	b = a + 7 => 7
	a = (a + c) + a => 10
	b = (b + b) + c => 24
	c = 1 + b => 25
	a + b + c => 59
```
##### Solution

 - [x] 59
 - [ ] 68
 - [ ] 70
 - [ ] 39
