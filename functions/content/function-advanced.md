# Advanced Syntax

In addition to the basic syntax of functions, Linux provides advanced features that allow for more flexibility and control within functions. In this section, we will explore some of these advanced syntax options, including:

- Passing arguments by reference
- Using local and global variables
- Handling variable scope
- Returning values from functions

Let's dive into each of these topics:

### Passing Arguments by Reference

By default, arguments passed to a function in Linux are passed by value, which means that the function receives a copy of the argument's value. However, it is also possible to pass arguments by reference, which allows the function to directly modify the original value of the argument.

To pass an argument by reference, you can use the `&` symbol before the argument name when defining the function. Here's an example:

```bash
increment() {
    local -n num_ref=$1  # Create a reference to the variable passed as the first argument
    ((num_ref++))  # Increment the value of the referenced variable
}

count=5
increment count
echo "New count value: $count"
```

In this example, the `increment` function takes an argument `num_ref` that is a reference to a variable. The `local -n` syntax is used to create a reference to the variable passed as the first argument (`count`). The `((num_ref++))` statement increments the value of the referenced variable, which directly modifies the original value of `count`. As a result, the output will be `New count value: 6`.

Passing arguments by reference can be useful when you need a function to modify the value of a variable outside its scope.

### Using Local and Global Variables

In functions, you can use both local and global variables. Local variables are declared within the function's scope and are accessible only within the function. Global variables, on the other hand, are declared outside any function and can be accessed by all functions in the script.

To access a global variable within a function, you can simply refer to it by its name. Here's an example:

```bash
global_var=42

print_global() {
    echo "Global variable value: $global_var"
}

print_global
```

In this example, the `print_global` function accesses the value of the global variable `global_var` and prints it.

Local variables, on the other hand, are declared using the `local` keyword inside the function. They have a separate scope within the function and do not affect variables with the same name outside the function. Here's an example:

```bash
print_local() {
    local local_var="Hello, local!"
    echo "$local_var"
}

print_local
```

In this example, the `print_local` function declares a local variable `local_var` and assigns it a value. The value is then printed within the function. The local variable `local_var` does not affect any variable with the same name outside the function.

### Handling Variable Scope

Variable scope refers to the portion of the script where a variable is visible and can be accessed. In Linux, variables declared outside any function have global scope and can be accessed by all functions. Variables declared inside a function have local scope and are accessible only within that function.

It's important to note that local variables take precedence over global variables with the same name. If a local variable with the same name as a global variable is declared within a function, the local variable will be used instead of the global one.

Here's an example to illustrate variable scope:

```bash
global_var=42

change_var() {
    local local_var=10
    echo "Local variable value: $local_var"
}

echo "Global variable value: $global_var"
change_var

In this example, we have a global variable `global_var` with a value of `42`. The `change_var` function declares a local variable `local_var` with a value of `10` and prints its value within the function. Outside the function, we print the value of the global variable. The output will be:

```
Global variable value: 42
Local variable value: 10
```

As you can see, the local variable `local_var` is accessible only within the `change_var` function, while the global variable `global_var` is accessible both inside and outside the function.

### Returning Values from Functions

Functions in Linux can return values using the `return` statement. The returned value can be captured by assigning the function call to a variable. Here's an example:

```bash
multiply() {
    local result=$(( $1 * $2 ))  # Multiply the first and second arguments and store the result
    return $result  # Return the result
}

product=$(multiply 5 3)  # Call the 'multiply' function and store the returned value in the 'product' variable
echo "The product is: $product"
```

In this example, the `multiply` function multiplies the first and second arguments (`$1` and `$2`) and stores the result in the `result` variable. The `return` statement is used to return the value of `result` from the function. The returned value is then captured in the `product` variable using the assignment `$(multiply 5 3)`. Finally, the value stored in `product` is printed, resulting in the output: "The product is: 15".

Returning values from functions allows you to perform calculations or operations within the function and obtain results that can be further used in your script.

With the advanced syntax options discussed above, you can leverage the power of functions in Linux to create more flexible and reusable code. These features provide greater control over variable handling and enable you to design functions that can modify variables, access global values, and return results.