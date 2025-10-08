# function performs a job
```py
def greet():
    print("hi")
```

# function returns a value
```py
def greet(name):
    return ("hi {name}")


A parameter is a piece of information that a function needs. 
And you specify the parameter in the function definition. 
For example, the greet() function has a parameter called "name".

def greet(name):
    return f"Hi {name}"


An argument is a piece of data that you pass into the function while calling. 
For example, the text string 'John' or the variable jane is the function argument.

greet('John') 

or

first_name = 'Jane'
greet(first_name)
```


# Python provides a built-in function called help() 
# that allows you to show the documentation of a function.
```py
help(greet)
```