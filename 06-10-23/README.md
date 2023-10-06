Stuff done on 06-10-23.
# Calculations in Tableau                                   06-10-23
  ## General operators:
  | General Operator | Description                                                      | Example                               |
|------------------|------------------------------------------------------------------|---------------------------------------|
| + (Addition)     | It can perform multiple operations like adding numbers, concatenating strings, and adding days to dates. | 2+3=5, #May 15, 2014# + 17 = #June 1, 2014# |
| - (Subtraction)  | It can also perform multiple operations like subtracting numbers and subtracting days from dates. | 8-5=3, #July 16, 2000# - 10 = #July 6, 2000# |

## Arithmetic Operators:
 | Arithmetic Operator | Description                                                      | Example                               |
 |------------------|------------------------------------------------------------------|---------------------------------------|
 | * (Asterisk) | Numeric Multiplication | 4*5=20 |
 | / (Forward slash) | Numeric Division	| 50/5=10 |
 | % (Percentage sign) | A reminder of the numeric division	| 25/2=1 |
 | ^ (Caret) | Raised to the power	| 5^2=25 |

 ##  Relational Operators:
 | Relational Operator | Description                  | Example    |
|---------------------|------------------------------|------------|
| >                   | Greater than                 | 5 > 8 = False |
| >=                  | Greater than or equal to     | 4 >= 4 = True |
| <                   | Less than                    | 4 < 10 = True |
| <=                  | Less than or equal to        | 1 <= 0 = False |
| ==                  | Equal to                     | 8 == 8 = True |
| !=                  | Not equal to                 | 7 != 7 = False |

## Logical Operators:
#### Logical AND:
  | AND   | TRUE | FALSE |
|-------|------|-------|
| TRUE  | TRUE | FALSE |
| FALSE | FALSE| FALSE |
#### Logical OR:
|  OR   | TRUE  | FALSE |
|-------|-------|-------|
| TRUE  | TRUE  | TRUE  |
| FALSE | TRUE  | FALSE |
#### Logical NOT:
| NOT   | TRUE  | FALSE |
|-------|-------|-------|
| TRUE  | FALSE | TRUE  |
| FALSE | TRUE  | FALSE |

## Number Functions
These are the functions used for numeric calculations. They only take numbers as inputs.
| Function       | Description                                                | Example                      |
|-----------------|------------------------------------------------------------|------------------------------|
| CEILING(number) | Rounds a number to the nearest integer of equal or greater value. | CEILING(2.145) = 3         |
| POWER(number, power) | Raises the number to the specified power.                 | POWER(5,3) = 125            |
| ROUND(number, [decimals]) | Rounds the number to a specified number of digits.      | ROUND(3.14152,2) = 3.14      |

## String Functions
String Functions are used for string manipulation.
| Function              | Description                                                                                     | Example                                |
|-----------------------|-------------------------------------------------------------------------------------------------|----------------------------------------|
| LEN(string)           | Returns the length of the string.                                                                | LEN("Tableau") = 7                    |
| LTRIM(string)         | Returns the string with any leading spaces removed.                                                | LTRIM(" Tableau ") = "Tableau"        |
| REPLACE(string, substring, replacement) | Searches the string for substring and replaces it with a replacement. If the substring is not found, the string is not changed. | REPLACE("GreenBlueGreen", "Blue", "Red") = "GreenRedGreen" |
| UPPER(string)         | Returns string, with all characters uppercase.                                                    | UPPER("Tableau") = "TABLEAU"          |

## Date Functions
Tableau has a variety of date functions to carry out calculations involving dates. All the date functions use the date_part which is a string indicating the part of the date such as - month, day, or year.
| Function          | Description                                                                        | Example                                              |
|-------------------|------------------------------------------------------------------------------------|------------------------------------------------------|
| DATEADD(date_part, increment, date) | Returns an increment added to the date. The type of increment is specified in date_part. | DATEADD('month', 3, #2004-04-15#) = 2004-07-15 12:00:00 AM |
| DATENAME(date_part, date, [start_of_week]) | Returns date_part of date as a string. The start_of_week parameter is optional.  | DATENAME('month', #2004-04-15#) = "April"            |
| DAY(date)         | Returns the day of the given date as an integer.                                      | DAY(#2004-04-12#) = 12                              |
| NOW()             | Returns the current date and time.                                                   | NOW() = 2004-04-15 1:08:21 PM                        |

## Logical Functions
These functions evaluate some single value or the result of an expression and produce a boolean output.
| Function         | Description                                                                                 | Example                            |
|------------------|---------------------------------------------------------------------------------------------|------------------------------------|
| IFNULL(expr1, expr2) | Returns expr1 if it is not null, and expr2 if expr1 is null.                              | IFNULL([Sales], 0) = [Sales]       |
| ISDATE(string)   | Returns TRUE if the string can be converted to a date, and FALSE if it cannot.               | ISDATE("11/05/98") = TRUE<br>ISDATE("14/05/98") = FALSE |
| MIN(expression)  | Returns the minimum of an expression across all records or the minimum of two expressions for each record. | MIN([Sales]) = Minimum sales value |

## Aggregate Functions
| Function         | Description                                                                                        | Example                                                |
|------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| AVG(expression)  | Returns the average of all the values in the expression. AVG can be used with numeric fields only. Null values are ignored. | AVG([Sales]) = Average sales value                      |
| COUNT(expression) | Returns the number of items in a group. Null values are not counted.                                 | COUNT([Items]) = Number of items in the group          |
| MEDIAN(expression) | Returns the median of an expression across all records. Median can only be used with numeric fields. Null values are ignored. | MEDIAN([Scores]) = Median score                         |
| STDEV(expression) | Returns the statistical standard deviation of all values in the given expression based on a sample of the population. | STDEV([Data]) = Standard deviation of the given data    |

## Calculations
*Numeric Calculations
