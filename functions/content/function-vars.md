
## Variables in Functions

Variables are used in functions to store and manipulate data. They allow you to work with dynamic values within the function's scope. Let's explore how to use variables in the context of functions:

### Variable Naming

In Linux, variables are typically named using lowercase letters and underscores. They can contain letters, digits, and underscores, but must start with a letter or underscore.

### Local Variables

Local variables are variables that are defined and used within the scope of a specific function. They are declared using the `local` keyword. Here's an example:

```bash
greet() {
    local name="John"  # Declare and assign a local variable named 'name'
    echo "Hello, $name!"
}

greet  # Call the 'greet' function
```

In this example, the `local` keyword is used to declare the `name` variable within the `greet` function. The value "John" is assigned to the `name` variable, and it is printed within the function.

### Function Parameters

Function parameters are variables that allow you to pass values to a function. They are accessed using special variables such as `$1`, `$2`, and so on. Here's an example:

```bash
greet() {
    local name=$1  # Assign the value passed as the first argument to the 'name' variable
    echo "Hello, $name!"
}

greet "Alice"  # Pass the value "Alice" to the 'greet' function
```

In this example, the `name` variable within the `greet` function is assigned the value passed as the first argument (`$1`). The value "Alice" is then printed within the function.

### Returning Values

Functions can return values using the `return` statement. The returned value can be captured by assigning the function call to a variable. Here's an example:

```bash
multiply() {
    local result=$(( $1 * $2 ))  # Multiply the first and second arguments and store the result
    return $result  # Return the result
}

product=$(multiply 5 3)  # Call the 'multiply' function and store the returned value in the 'product' variable
echo "The product is: $product"
```

In this example, the `multiply` function multiplies the first and second arguments (`$1` and `$2`) and stores the result in the `result` variable. The `return` statement is used to return the value of `result` from the function. The returned value is then captured in the `product` variable using the assignment `$(multiply 5 3)`. Finally, the value stored in `product` is printed.

Using variables in functions allows you to store, manipulate, and return data as needed. They provide flexibility and enable you to perform various operations based on input values, making your functions more powerful and reusable.
