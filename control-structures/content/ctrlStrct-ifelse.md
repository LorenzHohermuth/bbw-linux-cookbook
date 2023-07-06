# If/Else Statements

The `if/else` statements are conditional statements in Bash scripting. They are used to execute specific sections of code based on whether a certain condition evaluates to true or false. When you use an `if` statement, the script will check a particular condition, and if it's true, it will execute a specific block of code. An `else` statement can be used to provide an alternative block of code that will be executed if the original condition is false. Let's get into details:

## Basic if statement

A simple `if` statement can be written in the following format:

```bash
if [condition]
then
   # Code to execute if condition is true
fi
```

For example:

```bash
if [ "$1" -gt "100" ]
then
   echo "The number is greater than 100."
fi
```

In the above script, the condition checks if the first command-line argument is greater than 100. If it is, the script will echo the message.

## If / Else statement

The `if/else` statement is used when you want to execute one block of code if a condition is true, and another block if the condition is false:

```bash
if [condition]
then
   # Code to execute if condition is true
else
   # Code to execute if condition is false
fi
```

For example:

```bash
if [ "$1" -gt "100" ]
then
   echo "The number is greater than 100."
else
   echo "The number is not greater than 100."
fi
```

In this script, if the first command-line argument is not greater than 100, a different message will be displayed.

## If / Else If / Else statement

This statement is used when you want to check multiple conditions and execute a different block of code for each. If none of the conditions are true, the script will execute the block of code in the `else` statement:

```bash
if [condition1]
then
   # Code to execute if condition1 is true
elif [condition2]
then
   # Code to execute if condition2 is true
else
   # Code to execute if none of the conditions are true
fi
```

For example:

```bash
if [ "$1" -gt "100" ]
then
   echo "The number is greater than 100."
elif [ "$1" -eq "100" ]
then
   echo "The number is equal to 100."
else
   echo "The number is less than 100."
fi
```

In this script, if the first command-line argument is not greater than 100 but is equal to 100, a specific message will be displayed. If the number is less than 100, yet another message will be displayed.

In all these examples, note the use of square brackets `[...]` for conditions. In Bash scripting, conditions are often expressed within these brackets. You can test a variety of conditions such as the value of variables, arithmetic comparisons, or the status of a file. The conditions in the examples are arithmetic comparisons. Other forms of conditions can be just as easily implemented in `if/else` statements.