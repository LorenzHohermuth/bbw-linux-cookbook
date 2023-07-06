# Case Statements

A `case` statement, often referred to as a `switch` statement in other programming languages, allows for the execution of different code blocks based on the value of a certain variable or expression. It is more efficient and readable than using a complex combination of `if/elif/else` statements, especially when dealing with multiple possible values.

Here is the basic structure of a `case` statement in Bash:

```bash
case expression in
    pattern1 )
        # Commands to be executed if pattern1 matches
        ;;
    pattern2 )
        # Commands to be executed if pattern2 matches
        ;;
    * )
        # Default case, commands to be executed if no pattern matches
        ;;
esac
```

The `case` statement evaluates the given `expression` against the patterns provided. Each pattern can be a literal value or a regular expression. The code block for the first pattern that matches the expression will be executed. After each block of code, the double semicolons `;;` are used to denote the end of that section.

Here's an example:

```bash
read -p "Enter a fruit name: " fruit

case $fruit in
    "Apple" )
        echo "Apple is tasty."
        ;;
    "Banana" )
        echo "I like Banana."
        ;;
    * )
        echo "Unknown fruit."
        ;;
esac
```

In this script, the `case` statement checks the inputted fruit name. If it is "Apple", it will echo "Apple is tasty." If it is "Banana", it will echo "I like Banana." For any other input, it will echo "Unknown fruit."

The `case` statement is useful when you need to perform different actions for different possible values of a variable. It is a key control structure that can significantly enhance the flexibility and readability of your Bash scripts.

It's also worth mentioning the use of the `esac` keyword. In Bash, the `esac` keyword is used to terminate the `case` statement. It is essentially the reverse spelling of `case`. For example:

```bash
case $variable in
    pattern1 )
        # Commands for pattern1
        ;;
    pattern2 )
        # Commands for pattern2
        ;;
esac
```

The `esac` keyword denotes the end of the `case` statement block.

Including the `esac` keyword is important to ensure the proper syntax and termination of the `case` statement.