
# Functions

Learning Objectives
- Define a function that takes parameters.
- Return a value from a function.
- Test and debug a function.
- Set default values for function parameters.
- Explain why we should divide programs into small, single-purpose functions.



Imagine now that you're writing a piece of code...and you're writing up the exact same `if` statements, and the same loops, in multiple areas inside your program.

Instead of doing this, what we can do is make our own **functions** - where we can define our own command that performs the actions that we want it to. 

We've already encountered functions before - list.sort(), for example, is a function that takes your list, reorders the data inside it, and then gives it back to you.

Similarly, type() is a function that takes the data that you give it, tests which data type it is, and then prints out a statement that tells you what it is.

We can make a function using the `def`, or "definition" command, followed by what we would like our function to be called.

For example:


```python
def functionName(): #we also need these bracket on the end
    print("let's make some code")
```


```python
# I can then run this code inside the function by "calling" the function
functionName()
```

    let's make some code
    


```python

```

We can also make it so that our function has to take some *parameters* when we call it.

Parameters are variables that we use inside the function while writing our code. For example, if I were to make a function that adds two numbers:


```python
def add(x,y):
    x = x + y
    print(x)
```

x and y would be the variables that I use inside the function, and are thus the *parameters* of the `add()` function.

However, if your function uses parameters, when calling your function you have to include data that could represent those parameters. Try calling `add()` below without any numbers


```python
add()
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-13-09e9fb56b0a4> in <module>()
    ----> 1 add()
    

    TypeError: add() missing 2 required positional arguments: 'x' and 'y'



```python
#but if I include two numbers inside it, add will work
add(2,3)
add(1,2)
```

    5
    3
    


```python
# what if I define an "x" outside of the function though?
x = 1
print("Add(1,2) makes x:")
add(1,2)
print("but x is still", x )


```

    3
    Add(1,2) makes x:
    3
    but x is still 1
    

This is because the parameter names that we define inside the function **only exist inside the function**

If I make a new variable inside add, for example, that variable will not exist outside that function


```python
def add2(x,y):
    new = x + y
```


```python
add2(1,2)

new
```


```python
#Let's try assigning the value of add2 to a variable

temp = add2(1,2)

print(temp)
```

    None
    

Why?






So far, add2 is only performing some math inside itself. It's not actually giving you back any data.

To do this, we have to tell the function what data to give back when we run it. We can do this with a `return` statement


```python
def add2(x,y):
    
    new = x + y
    
    return new


```


```python
add2(1,2)
```




    3




```python
new
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-31-9cd599a35238> in <module>()
    ----> 1 new
    

    NameError: name 'new' is not defined


As you can see, this doesn't change the fact that "new", as a variable name, only exists within that function. However the *value* of new, 3, is now being given back to us.

Now let's try to write a function that converts temperatures from Fahrenheit to Kelvin, and run it on a couple of different temperatures.

The math invovled in this is:
`(temperature - 32) * (5/9) + 273.15`



### Mini Challenge 1

Write the function fahr_to_kelvin that successfully gives you the value 273.15 when we give it a temperature of 32.


```python
def fahr_to_kelvin(temp):
    
```


```python

```




    273.15



Now that we've seen how to turn Fahrenheit into Kelvin, it's easy to turn Kelvin into Celsius - just take the temperature and minus 273.15

celsius = `kelvinTemperature - 273.15`


```python
def kelvin_to_celsius(tempk):
    
```


```python

```

What if we then want to turn fahrenheit into celsius?

We could write out the math for the whole thing...but we already have some functions that do that for us!

A cool thing about making a function is that we can actually use a function inside another function.

If you think about it, we already are. If we were to make a function and use `list.reverse()` inside it, then we're using a *function inside your function*.

### Mini challenge 2

Write a function that takes a temperature in fahrenheit, and outputs a temperature in celsius.


```python

```


```python

```


```python

```

## Function Defaults

When you are defining your functions, you can actually set your parameters to have default values. 

You can do this by making your parameter '=' to something inside your function definition.


```python
def HelloWorld(message,times = 1):
    print (message * times)
```


```python
HelloWorld("this")
```

    this
    


```python

```


```python

```

## User Input

You can also program your code so that it can prompt a user for input.

Imagine, for example, programming your `HelloWorld` function to ask the user how many times they want to print the message. Or even what the message is.

To program a user input, you simply need to do:

```python

variableName = input()
```

You can also choose to include a message that displays when prompting the user, like this:

```python

variableName = input("This will display a message:")
```


```python
variable = str(input("Display this message: "))
```

    Display this message: HI
    


```python
variable
```




    'Hello'



#### Mini Challenge

Make another function called HelloWorld, which prints the phrase "Hello World!", on separate lines, for as many times as the user tells it to.


```python
def HelloWorld(message = "Hello world!", times):
    
```

## Challenge 1

Remember our homework challenge, where we run through a list and then separate it's contents into separate lists?

This time, your challenge is to write a function that takes "list1", and separates it into the same lists as previously. However, this time, the numeric cut-off for sorting is now going to be determined by the user, instead of being <= 10.

**Hint:** How might we return all three of our lists? What kind of data structure could we use?


```python

```


```python

```


```python

```


```python

```
