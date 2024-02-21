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

## Decimal Precision

```C
#include <stdio.h>

int main() {
  float myFloatNum = 3.5;

  printf("%f\n", myFloatNum); // Default will show 6 digits after the decimal point
  printf("%.1f\n", myFloatNum); // Only show 1 digit
  printf("%.2f\n", myFloatNum); // Only show 2 digits
  printf("%.4f", myFloatNum);   // Only show 4 digits
  return 0;
}
```

# Basic format specifiers
|   Format Specifier    |	Data Type |
|-----------------------|-------------|
|%d or %i               |	int	      |
|%f or %F	            | float	      |
|%lf	                |double	    |
|   %c	                |   char	|
|   %s	                | strings (text) |

# Constants
declare the variable as "constant", which means unchangeable and read-only:

```C
#include <stdio.h>

int main() {
  const int myNum = 15;
  myNum = 10;
  
  printf("%d", myNum);
  return 0;
}
```

# Operators

```md
A list of all assignment operators:

| Operator |	Example |	Same As |
| -------- | ---------| --------|
|=	       |x = 5	    |x = 5	  |
|+=	       |	x += 3	|x = x + 3|	
|-=	       |	x -= 3	|x = x - 3|	
|*=	       |	x *= 3	|x = x * 3|	
|/=	       |	x /= 3	|x = x / 3|	
|%=	       |	x %= 3	|x = x % 3|	
|&=	       |	x &= 3	|x = x & 3|	
| |=	     |	x |= 3	|x = x | 3|	
|^=	       |	x ^= 3	|x = x ^ 3|	
|>>=	     |	x >>= 3	|x = x >> 3	|
|<<=	     |	x <<= 3	|x = x << 3|
```

## Boolean
You need to import the following header to use *bool* data type:
```C
#include <stdbool.h> 
```

The bool variable will return int, therefore we must use the %d format specifier to print a boolean value:

```C
#include <stdio.h>
#include <stdbool.h>  // Import the boolean header file 

int main() {
  bool isProgrammingFun = true;
  bool isFishTasty = false;
  printf("%d\n", isProgrammingFun);  // Returns 1 (true)
  printf("%d", isFishTasty);         // Returns 0 (false)
  
  return 0;
}
```

### Boolean Real life example :
```C
#include <stdio.h>

int main() {
  int myAge = 25;
  int votingAge = 18;

  if (myAge >= votingAge) {
    printf("Old enough to vote!");
  } else {
    printf("Not old enough to vote.");
  }
  
  return 0;
}
```

## C If ... Else

List of conditions
| Conditions |	Example |	Remarks |
| ---------- | ---------| --------|
| <          | a < b    | a less than b |
| <=         | a <= b   | a less or equal to b |
| >          | a > b    | a greater than b |
| >=         | a >= b   | a greater or equal to b |
| ==         | a == b   | a equal to b |
| !=         | a != b   | a not equal to b |

Example :
```C
#include <stdio.h>

int main() {
  if (20 > 18) {
    printf("20 is greater than 18");
  }  
  return 0;
}
```

```C
#include <stdio.h>

int main() {
  int x = 20;
  int y = 18;
  if (x > y) {
    printf("x is greater than y");
  }  
  return 0;
}
```

```C
#include <stdio.h>

int main() {
  int time = 20;
  if (time < 18) {
    printf("Good day.");
  } else {
    printf("Good evening.");
  }
  return 0;
}
```

```C
#include <stdio.h>

int main() {
  int time = 22;
  if (time < 10) {
    printf("Good morning.");
  } else if (time < 20) {
    printf("Good day.");
  } else {
    printf("Good evening.");
  }
  return 0;
}
```

### Ternary operator
```C
#include <stdio.h>

int main() {
  int time = 20;
  (time < 18) ? printf("Good day.") : printf("Good evening.");
  return 0;
}
```

### Real Life Examples
```C
#include <stdio.h>

int main() {
  int myAge = 25;
  int votingAge = 18;

  if (myAge >= votingAge) {
    printf("Old enough to vote!");
  } else {
    printf("Not old enough to vote.");
  }
  
  return 0;
}
```

## C Switch

Instead of writing many **if..else** statements, you can use the **switch** statement.

```C
#include <stdio.h>

int main() {
  int day = 4;
  
  switch (day) {
  case 1:
    printf("Monday");
    break;
  case 2:
    printf("Tuesday");
    break;
  case 3:
    printf("Wednesday");
    break;
  case 4:
    printf("Thursday");
    break;
  case 5:
    printf("Friday");
    break;
  default:
    printf("Weekend");
  }
  
  return 0;
}
```

## C While Loop

Loops can execute a block of code as long as a specified condition is reached.

Loops are handy because they save time, reduce errors, and they make code more readable.

```C
#include <stdio.h>

int main() {
  int i = 0;
  
  while (i < 5) {
    printf("%d\n", i);
    i++;
  }
  
  return 0;
}
```

## C Do/While Loop

The do/while loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.

```C
#include <stdio.h>

int main() {
  int i = 0;
  
  do {
    printf("%d\n", i);
    i++;
  }
  while (i < 5);
  
  return 0;
}
```

## C For loop