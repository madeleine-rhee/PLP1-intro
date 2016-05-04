##Variables in R
**Integer**  
x <- 5;  
x

**String**  
msg <- "Hello World!";  
msg

**Float**  
y <- 27.888888;  
y

**Boolean**  
a<-1  
b<-3  
if (b!=a){  
print("b is not equal to a!")}  

**Array/List**  
vec <- c(1,2,3,4,5);  
vec2 <- c(6,7,8,9,10);  
vec3 <- c(11,12,13,14,15);  
rbind(vec,vec2,vec3);  

**Hash/Dictionary**  
ex <- list(first = "harry", last = "potter", num = 1);  
ex2 <- list(first = "hermione", last = "granger", num = 2);  
ex3 <- list(first = "ron", last = "weasley", num = 3);  
dict <- list(hp = ex, hg = ex2, rw = ex3)

##Data Types and Naming Conversions
R is a dynamic, strongly typed language.  Its has very minimal naming requirements dictate names can be any alphanumeric string including underscores so long as it starts with a character.  Variables are assigned using "<-" or "=" and do not require any special prefixes to designate types. As a dynamic language, the value of a variable can be reassigned at will however, as a static language there are strong distinctions for numeric and non-numeric variables and their interactions.

For example, in order for a line such as

x = "5" + 6

to compile, the string "5" must first be converted to a numeric value.

In R this can be achieved by assigning each value of the equation to a variable.
a = "5"  
b = 6

The numeric value of a can then be accessed through the built in function "as.numeric()" which asks the program to use the numeric value of the variable

x = as.numeric(a) + b

which allows the string "5" and integer 6 to be added.

On a related note, a similar function as.integer() can be used to assign integers.  While R will automatically cast any numeric values according to their type(int, float, ect.), the function as.integer() can force the storage or use of a integer.  This can be useful as conversions in R are widening.

##Conversions

Variables can be converted through a variety of functions.  The numeric value of strings can be acquired and integers can be stored as strings through concatenation.

The ability to acquire the numeric values from strings and easily convert numeric values to strings is extremely useful and necessary considering R's extensive use fo dataframes.  A key appeal in the statistical modeling using R is its great capacity to handle and store large and various types of data.  However with any dynamically typed language, you run the risk of accidentally reassigning variables and errors due to incorrectly assignment as the program will not catch them until execution later in the code not in the compiler as would be in statically typed languages.  Also worth noting is the ability to use strings as numeric values and vice versa without changing the value stored in the originally cast variable and if the value need be saved a new variable can be cast using the same method plus assignment.

