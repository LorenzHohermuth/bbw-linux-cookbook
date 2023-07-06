# Loops

Loops in Bash scripting are used when you need to repeat a specific block of commands multiple times. They allow for repetitive tasks to be automated, making your scripts more efficient and easier to maintain. There are three types of loops commonly used in Bash: `for`, `while`, and `until`.

* ## [For Loop](#for "for loop")
* ## [While Loop](#while "while loop")
* ## [Until Loop](#until "until loop")

---

## For

The `for` loop is used when you want to execute a set of commands for a predefined number of times. The basic syntax is:

```bash
for variable in list
do
   # Commands to be executed
done
```

Here's an example:

```bash
for i in 1 2 3 4 5
do
   echo "Number is $i"
done
```

In this script, the `for` loop will iterate over the list of numbers (1, 2, 3, 4, 5), and for each iteration, it will echo the current value of `i`.

---

## While

The `while` loop is used when you want to repeat a set of commands as long as a particular condition is true. The basic syntax is:

```bash
while [condition]
do
   # Commands to be executed
done
```

Here's an example:

```bash
counter=1

while [ $counter -le 5 ]
do
   echo "Counter is $counter"
   ((counter++))
done
```

In this script, the `while` loop will continue to echo the value of `counter` and increment it as long as the counter is less than or equal to 5.

---

## Until

The `until` loop is used when you want to repeat a set of commands until a particular condition is true. It is the opposite of a `while` loop because it executes the code block as long as the condition is false. The basic syntax is:

```bash
until [condition]
do
   # Commands to be executed
done
```

Here's an example:

```bash
counter=1

until [ $counter -gt 5 ]
do
   echo "Counter is $counter"
   ((counter++))
done
```

In this script, the `until` loop will continue to echo the value of `counter` and increment it until the counter is greater than 5.