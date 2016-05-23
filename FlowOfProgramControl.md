##Flow of Program Control##

The flow of program control in R has all the common statements with relatively logical syntax.

**If/Else**  
x<-5;  
if(x==5){print("x = 5!")}  

if (x<0){print("x is negative!")  
} else if (x<5){print("x is pretty small")  
} else {print("x is pretty big!")}   

R uses the if/else if/else for conditional statements.  An important note is that R handles the dangling else by requiring a closing bracket just prior.  "if" statements should habitually be written with the closing bracket on the following line.  
EX.  
if(condition){statement  
} else{statement  
}  

**Multi Condition If/Else**  
if(x>5 && x<10){print("x is between 5 and 10")}  

Also relavent to conditional statements is short-circuit evaluation in multi-condition if/else.  Like in Java, && and || denotate short circuit "and" and "or" where both conditions will not be evaluated.  Short-circuit logic operates where if the left hand side of the statement is true, the whole statement is true under the logic for a statement to be true, only a part of the statement needs to be true, or else the statement could not be any part true.

###Loops###  
With regard to loops, R has all of the standards; while, do/while, for, and for each.  

**While**  
y<-0  
while(y<10){print(y)  
y = y+1}  

While can be executed similar to a Java while with a condition and a series of statements.

**Do/While**  
y<-0  
repeat{y = y+1  
print(y)  
if(y==10){  
break  
}  
}  

Do/while requires the use of the repeat and break operators built into R.  As in any do/while loop, an action occurs (do) and then a condition is checked (while something is true).  Repeat executes the action prior to the conditional check each time it loops through, while if executes the conditional check.  Because the check happens after the action occurs, there is no way to use less than conditionals.  Instead, the if clause is set to the target and once it is met, exits out of the loop using the break statement.  Without the inclusion of an if target clause and break, there would be an infinite loop.

**For**  
for (i in 1:10){  
print(i)  
}  

For loops in R operate in much the same way as Java.  A helpful exception is in how the conditionals are set up.  Instead of a series of less than/greater than conditions, a singlar conditional statement can be written. "i in 1:10" notes the parameter i between 1 and 10 and includes the upper and lower listed limits.

**For Each**  
library(foreach)  
x<-foreach(i=1:3) %do% sqrt(i)  
x  

Unlike for loops which can be initiated directly from original code, for each utilizes the power of packages.  R has a very dedicated and active community constantly generating new packages for analyzing various types of data.  The foreach loop can be utilized by loading the foreach package into the library.  Differing from the for loop, for each applies an action (%do%) to each of the values within its condition.  In this code block, x represents the name of the function and for each value of i between 1 and 3, including one and three, reduce it to its square root.

**Switch Case**  
switch(3, "one", "two", "three")  

Switch cases allow the selection of a particular outcome from a predefined list.  In R, the switch statement is required to have the selected outcome listed first and will then automatically continue through the clauses until it reaches the desired clause, which it will return.

**Break**  
y<-0  
repeat{print(y)  
if(y<10){y=y+1  
next  
}  
print("done")  
break  
}  

In R, break is used to exit loops particularly in do while.  Break is however criticized as bad practice as a method of exiting loops.
