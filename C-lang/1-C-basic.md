# C syntax

```C
#include <stdio.h>

int main() {
  printf("Hello World!");
  return 0;
}
```

## Explain:
- **#include <stdio.h>** is a header file library that lets us work with input and output functions, such as printf() (used in line 4). Header files add functionality to C programs.

- A blank line. C ignores white space. But we use it to make the code more readable.

- Another thing that always appear in a C program is **main()**. This is called a function. Any code inside its curly brackets {} will be executed.

- **printf()** is a function used to output/print text to the screen. In our example, it will output "Hello World!".

- Note that: Every C statement ends with a semicolon ;

- **return 0** ends the main() function.

- Do not forget to add the closing curly bracket **}** to actually end the main function.

# C Variables
there are different types of variables (defined with different keywords), for example:

- **int** - stores integers (whole numbers), without decimals, such as 123 or -123
- **float** - stores floating point numbers, with decimals, such as 19.99 or -19.99
- **char** - stores single characters, such as 'a' or 'B'. Characters are surrounded by single quotes

## Declaring variables

```C
type variableName = value;
```

## Change Variable Values
If you assign a new value to an existing variable, it will overwrite the previous value:

```C
#include <stdio.h>

int main() {
  int myNum = 15; // myNum is 15
  myNum = 10; // Now myNum is 10
  
  printf("%d", myNum);
  return 0;
}
```

## Assign the value of one variable to another:

```C
#include <stdio.h>

int main() {
  int myNum = 15;
  
  int myOtherNum = 23;

  // Assign the value of myOtherNum (23) to myNum
  myNum = myOtherNum;

  // myNum is now 23, instead of 15
  printf("%d", myNum);
  
  return 0;
}
```

## Copy values to empty variables:

```C
#include <stdio.h>

int main() {
  // Create a myNum variable and assign the value 15 to it
  int myNum = 15;
  
  // Declare a myOtherNum variable without assigning it a value
  int myOtherNum;

  // Assign value of myNum to myOtherNum
  myOtherNum = myNum;

  // myOtherNum now has 15 as a value
  printf("%d", myOtherNum);
  
  return 0;
}
```

## Add variable together:

```C
#include <stdio.h>

int main() {
  int x = 5;
  int y = 6;
  int sum = x + y;
  printf("%d", sum);
  return 0;
}
```

## Declare Multiple Variables

```C
#include <stdio.h>

int main() {
  int x = 5, y = 6, z = 50;
  printf("%d", x + y + z);
  return 0;
}
```


# C Format Specifiers

```C
#include <stdio.h>

int main() {
  // Create variables
  int myNum = 15;              // Integer (whole number)
  float myFloatNum = 5.99;     // Floating point number
  char myLetter = 'D';         // Character
  
  // Print variables
  printf("%d\n", myNum);
  printf("%f\n", myFloatNum);
  printf("%c\n", myLetter);
  return 0;
}
```

# Data types
Basic Data Types
The data type specifies the size and type of information the variable will store.

The most basic ones:

|Data Type |	Size      |	Description |	Example   |
|----------|--------------|-------------|-------------|
|int       | 2 or 4 bytes |	Stores whole numbers, without decimals |	1|
|float     | 4 bytes      |	Stores fractional numbers, containing one or more decimals. Sufficient for storing 6-7 decimal digits |	1.99|
|double    |8 bytes       |	Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits | 1.99|
|char      |1 byte	      | Stores a single character/letter/number, or ASCII values	|'A'|

# Basic format specifiers
|   Format Specifier    |	Data Type |
|-----------------------|-------------|
|%d or %i               |	int	      |
|%f or %F	            | float	      |
|%lf	                |double	    |
|   %c	                |   char	|
|   %s	                | strings (text) |