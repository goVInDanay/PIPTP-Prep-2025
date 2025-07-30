# Week1 - Day 3

## Problems
#####  - Problem 1
What will be the output for n = 2?
```
	function mystery(n):
		if n == 0:
			return
		mystery(n - 1)
		mystery(n - 1)
		print(n)
		mystery(2)
```
	

 #####  Steps
 ```
	 mystery(2)

-   calls `mystery(1)`
	    
	    -   calls `mystery(0)` → returns
	        
	    -   calls `mystery(0)` → returns
	        
	    -   prints `1`
	        
	-   calls `mystery(1)`
	    
	    -   calls `mystery(0)` → returns
	        
	    -   calls `mystery(0)` → returns
	        
	    -   prints `1`
	        
	-   prints `2`
 ```
 ##### Solution
 

 - [ ] 1 1 2 1 1 2
 - [ ] 1 2 1 2
 - [x] 1 1 2
 - [ ] 1 2 2

 
##### - Problem 2
What will be output for  n = 2?
```
	function loopRec(n):
		if n == 0:
			return
		for i = 1 to 2:
			loopRec(n - 1)
		print(n)
```
##### Steps
```
	loopRec(2)
	-calls loopRec(1)
		-loopRec(0) -> return
		-loopRec(0) -> return
		print(1)
	-calls loopRec(1)
		-loopRec(0) -> return
		-loopRec(0) -> return
		print(1)
	print 2
```
##### Solution

 - [x] 1 1 2
 - [ ] 1 2 1
 - [ ] 2 1 1
 - [ ] 1 1 1 2
