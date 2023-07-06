# Common Functions

Common functions in Linux refer to frequently used functions that provide essential operations for various tasks. These functions cover different domains such as math, string manipulation, array handling, and file operations. By leveraging these common functions, you can perform common tasks efficiently and effectively in your Linux scripts.

* ## [Math](#math-functions "math functions")

* ## [String](#string-functions "string functions")

* ## [Array](#array-functions "array functions")

* ## [File](#file-functions "file functions")

---

<!-- ====================== Math ====================== -->
## Math Functions

Math functions in Linux provide a set of operations to perform mathematical calculations. Here are some commonly used math functions:

### Arithmetic Operations

Linux provides various arithmetic operations that you can use in your scripts. These operations include addition, subtraction, multiplication, division, modulus, and exponentiation. Here's an example of using arithmetic operations:

```bash
# Addition
result=$((5 + 3))
echo "Addition: $result"

# Subtraction
result=$((10 - 4))
echo "Subtraction: $result"

# Multiplication
result=$((2 * 6))
echo "Multiplication: $result"

# Division
result=$((10 / 2))
echo "Division: $result"

# Modulus (remainder)
result=$((15 % 4))
echo "Modulus: $result"

# Exponentiation
result=$((2 ** 3))
echo "Exponentiation: $result"
```

### Comparison Operators

In addition to arithmetic operations, Linux also provides comparison operators to compare values. These operators include equal to (`-eq`), not equal to (`-ne`), greater than (`-gt`), greater than or equal to (`-ge`), less than (`-lt`), and less than or equal to (`-le`). Here's an example:

```bash
value1=5
value2=10

# Equal to
if [ "$value1" -eq "$value2" ]; then
    echo "Values are equal"
else
    echo "Values are not equal"
fi

# Greater than
if [ "$value1" -gt "$value2" ]; then
    echo "Value 1 is greater than value 2"
else
    echo "Value 1 is not greater than value 2"
fi

# Less than
if [ "$value1" -lt "$value2" ]; then
    echo "Value 1 is less than value 2"
else
    echo "Value 1 is not less than value 2"
fi
```

### Mathematical Functions

Linux provides several mathematical functions that allow you to perform complex mathematical calculations. These functions include `sqrt()` (square root), `sin()` (sine), `cos()` (cosine), `tan()` (tangent), `exp()` (exponential), `log()` (natural logarithm), and more. Here's an example:

```bash
# Square root
result=$(echo "sqrt(25)" | bc)
echo "Square root: $result"

# Sine
result=$(echo "s(0)" | bc -l)
echo "Sine: $result"

# Cosine
result=$(echo "c(0)" | bc -l)
echo "Cosine: $result"

# Tangent
result=$(echo "s(0) / c(0)" | bc -l)
echo "Tangent: $result"

# Exponential
result=$(echo "e(1)" | bc -l)
echo "Exponential: $result"

# Natural logarithm
result=$(echo "l(10)" | bc -l)
echo "Natural logarithm: $result"
```

These are just a few examples of the math functions available in Linux. You can explore the `bc` command and other mathematical libraries to perform more

complex calculations and utilize advanced mathematical functions.

---

<!-- ====================== String ====================== -->

## String Functions

String functions in Linux provide a variety of operations to manipulate and analyze strings. Here are some commonly used string functions:

### String Length

To determine the length of a string, you can use the `expr` command or the `${#string}` syntax. Here's an example:

```bash
string="Hello, World!"

# Using expr
length=$(expr length "$string")
echo "String length: $length"

# Using ${#string}
length=${#string}
echo "String length: $length"
```

### String Concatenation

You can concatenate strings using the concatenation operator `+` or by simply placing the strings together. Here's an example:

```bash
string1="Hello"
string2="World"

# Using concatenation operator
concatenated1=$string1" "$string2
echo "Concatenated string: $concatenated1"

# Using string concatenation
concatenated2="$string1 $string2"
echo "Concatenated string: $concatenated2"
```

### Substring Extraction

To extract a substring from a string, you can use the `${string:start:length}` syntax, where `start` is the starting index and `length` is the number of characters to extract. Here's an example:

```bash
string="Hello, World!"

# Extracting a substring
substring=${string:7:5}
echo "Substring: $substring"
```

### String Manipulation

Linux provides various string manipulation functions, such as converting to uppercase, converting to lowercase, and replacing substrings. Here's an example:

```bash
string="Hello, World!"

# Converting to uppercase
uppercase=${string^^}
echo "Uppercase string: $uppercase"

# Converting to lowercase
lowercase=${string,,}
echo "Lowercase string: $lowercase"

# Replacing substring
replaced=${string/Hello/Hi}
echo "Replaced string: $replaced"
```

### String Comparison

You can compare strings using various comparison operators, such as equal to (`==`), not equal to (`!=`), less than (`<`), and greater than (`>`). Here's an example:

```bash
string1="Hello"
string2="World"

# Equal to
if [ "$string1" == "$string2" ]; then
    echo "Strings are equal"
else
    echo "Strings are not equal"
fi

# Greater than
if [ "$string1" > "$string2" ]; then
    echo "String 1 is greater than string 2"
else
    echo "String 1 is not greater than string 2"
fi
```

These are just a few examples of the string functions available in Linux. You can explore other string manipulation commands and techniques to perform more advanced operations on strings.

---

<!-- ====================== Array ====================== -->

## Array Functions

Arrays in Linux allow you to store multiple values in a single variable. Here are some commonly used array functions:

### Array Declaration

To declare an array in Linux, you can use the following syntax:

```bash
array=(value1 value2 value3)
```

Here's an example:

```bash
# Array declaration
fruits=("Apple" "Banana" "Orange")

# Accessing array elements
echo "First fruit: ${fruits[0]}"
echo "Second fruit: ${fruits[1]}"
echo "Third fruit: ${fruits[2]}"
```

### Array Length

To determine the length of an array, you can use the `${#array[@]}` syntax. Here's an example:

```bash
fruits=("Apple" "Banana" "Orange")

# Array length
length=${

# Array length
length=${#fruits[@]}
echo "Array length: $length"
```

### Adding Elements to an Array

You can add elements to an array using the `+=` operator. Here's an example:

```bash
fruits=("Apple" "Banana" "Orange")

# Adding elements to the array
fruits+=("Mango" "Grapes")

# Printing the updated array
echo "Updated array: ${fruits[@]}"
```

### Looping through an Array

You can loop through an array using a `for` loop. Here's an example:

```bash
fruits=("Apple" "Banana" "Orange")

# Looping through the array
for fruit in "${fruits[@]}"; do
    echo "Fruit: $fruit"
done
```

### Removing Elements from an Array

To remove elements from an array, you can unset the specific array indices using the `unset` command. Here's an example:

```bash
fruits=("Apple" "Banana" "Orange")

# Removing an element from the array
unset fruits[1]

# Printing the updated array
echo "Updated array: ${fruits[@]}"
```

These are just a few examples of the array functions available in Linux. You can explore more array manipulation techniques and functions to work with arrays effectively.

---

<!-- ====================== File ====================== -->

## File Functions

File functions in Linux provide operations to interact with files, such as creating, reading, writing, and manipulating file contents. Here are some commonly used file functions:

### Creating a File

To create a file in Linux, you can use the `touch` command. Here's an example:

```bash
filename="example.txt"

# Creating a file
touch "$filename"
echo "File created: $filename"
```

### Reading a File

To read the contents of a file, you can use the `cat` command or read the file line by line using a `while` loop. Here's an example:

```bash
filename="example.txt"

# Reading the file using cat command
echo "Reading the file using cat:"
cat "$filename"

# Reading the file line by line
echo "Reading the file line by line:"
while IFS= read -r line; do
    echo "$line"
done < "$filename"
```

### Writing to a File

To write to a file, you can use the `echo` command or redirect output to a file using the `>` or `>>` operators. Here's an example:

```bash
filename="example.txt"

# Writing to a file using echo
echo "Hello, World!" > "$filename"

# Appending to a file using echo
echo "Additional content" >> "$filename"

# Displaying the updated file contents
cat "$filename"
```

### Renaming or Moving a File

To rename or move a file, you can use the `mv` command. Here's an example:

```bash
oldname="example.txt"
newname="new_example.txt"

# Renaming or moving a file
mv "$oldname" "$newname"
echo "File renamed/moved to: $newname"
```

### Deleting a File

To delete a file, you can use the `rm` command. Here's an example:

```bash
filename="example.txt"

# Deleting a file
rm "$filename"
echo "File deleted: $filename"
```

These are just a few examples of the file functions available in Linux. You can explore more file manipulation commands and techniques to work with files efficiently.