# Week1 - Day 4

## Problems
#####  - Problem 1
What will be the output?
```
	#include<stdio.h>
	int f(int n, int k)
	{
		if(n==0) return 0;
		else if(n%2) return f(n/2, 2*k)+k;
		else return f(n/2, 2*k)-k;
	}
	int main()
	{
		printf("%d",f(20,1));
		return 0;
	}
```
	

 #####  Steps
 ```
 f(20, 1)

-   n = 20 → even → go to: `f(10, 2) - 1`
    

f(10, 2)

-   n = 10 → even → go to: `f(5, 4) - 2`
    
 f(5, 4)

-   n = 5 → odd → go to: `f(2, 8) + 4`
    

f(2, 8)

-   n = 2 → even → go to: `f(1, 16) - 8`
    
f(1, 16)

-   n = 1 → odd → go to: `f(0, 32) + 16`
    
 f(0, 32)

-   n = 0 → base case → return 0

----------
Now backtrack with values:

-   `f(0,32)` = 0
    
-   `f(1,16)` = 0 + 16 = 16
    
-   `f(2,8)` = 16 - 8 = 8
    
-   `f(5,4)` = 8 + 4 = 12
    
-   `f(10,2)` = 12 - 2 = 10
    
-   `f(20,1)` = 10 - 1 = 9
 ```
 ##### Solution
 

 - [x] 9
 - [ ] 12
 - [ ] 6
 - [ ] 3

 
##### - Problem 2
What will be output for  n = 5?
```
int f(int n)
{
	static int r=0;
	if(n<=0) return 1;
	if(n>3)
	{
		r=n;
		return f(n-2)+2;
	}
	return f(n-1)+r;
}
```
##### Steps
```
f(5):

-   `n > 3`, so:
    
    -   `r = 5`
        
    -   return `f(3) + 2`
        
f(3):

-   `n <= 3`, so:
    
    -   return `f(2) + r` → `f(2) + 5`
        
f(2):

-   return `f(1) + r` → `f(1) + 5`
    
f(1):

-   return `f(0) + r` → `f(0) + 5`
    
 f(0):

-   base case → return `1`
    

----------
Backtrack with values:
-   `f(0) = 1`
    
-   `f(1) = 1 + 5 = 6`
    
-   `f(2) = 6 + 5 = 11`
    
-   `f(3) = 11 + 5 = 16`
    
-   `f(5) = 16 + 2 = **18**`
```
##### Solution

 - [ ] 11
 - [ ] 12
 - [x] 18
 - [ ] 20
##### - Problem 3
What will be output for n = 173?
```
void f(int n)
{
	if(n<=1)
	{
		printf("%d",n);
	}
	else
	{
		f(n/2);
		printf("%d",n%2);
	}
}
```
##### Steps
```
-   `f(1)` prints `1`
    
-   Back to `f(2)`: print `2 % 2 = 0`
    
-   Back to `f(5)`: print `5 % 2 = 1`
    
-   Back to `f(10)`: print `10 % 2 = 0`
    
-   Back to `f(21)`: print `21 % 2 = 1`
    
-   Back to `f(43)`: print `43 % 2 = 1`
    
-   Back to `f(86)`: print `86 % 2 = 0`
    
-   Back to `f(173)`: print `173 % 2 = 1`
```
##### Solution

 - [ ] 10111001
 - [x] 10101101
 - [ ] 10101111
 - [ ] 10111001

##### -Problem 4
What will be output for foo(135, 10)?
```
unsigned int foo(unsigned int n, unsigned int r)
{
	if(n>0) return((n%r)+foo(n/r,r));
	else return 0;
}
```

##### Steps
```
-   Call: `foo(345, 10)`
    
    -   `n > 0`, so compute:
       
    -   → `345 % 10 = 5`
        
    -   → `foo(345 / 10, 10)` → `foo(34, 10)`
        
    -   So: `foo(345, 10) = 5 + foo(34, 10)`
        
-   Call: `foo(34, 10)`
    
    -   `n > 0`, so compute:
        
    -   → `34 % 10 = 4`
        
    -   → `foo(34 / 10, 10)` → `foo(3, 10)`
        
    -   So: `foo(34, 10) = 4 + foo(3, 10)`
        
-   Call: `foo(3, 10)`
    
    -   `n > 0`, so compute:
        
    -   → `3 % 10 = 3`
        
    -   → `foo(3 / 10, 10)` → `foo(0, 10)`
        
    -   So: `foo(3, 10) = 3 + foo(0, 10)`
        
-   Call: `foo(0, 10)`
    
    -   `n == 0`, return `0`
```

##### Solution

 - [ ] 9
 - [ ] 15
 - [x] 12
 - [ ] 14

##### -Problem 5
What will be output for foo(513, 2)?
```
unsigned int foo(unsigned int n, unsigned int r) {
	if(n>0) return((n%r)+foo(n/r,r));
	else return 0;
}
```
##### Steps
```
-   Call: `foo(513, 2)`
    
    -   `n > 0`, so compute:
       
    -   → `513 % 2 = 1`
        
    -   → `foo(513 / 2, 2)` → `foo(256, 2)`
        
    -   So: `foo(256, 2) = 0 + foo(128, 2)`
        
-   Call: `foo(128, 2)`
    
    -   `n > 0`, so compute:
        
    -   → `128 % 2 = 0`
        
    -   → `foo(128 / 2, 10)` → `foo(64, 2)`
   And so on
```
##### Solution
 
 - [ ] 5
 - [ ] 4
 - [ ] 3
 - [x] 2
