
# Conditionals

In this session we are going to learn how to program your computer to make choices about which action it should perform


### Learning Objectives

- Write conditional statements including `if`, `elif`, and `else` branches
- Correctly evaluate expressions containing `and` and `or`
- Correctly write and interpret code containing nested conditionals


Conditionals allow you make the computer or program perform a certain action depending on particular conditions.

But to assess a condition, we first need to understand how we can test them.

These tests are usually done using "equality operators". Things like:

- `<`, less than
- `>`, greater than
- `<=` less than or equal to
- `>=` greater than or equal to
- `==`, equals
- `!=`, does not equal
- `is`, `in` and `not`

Let's try using these in our cells


```python
print(5 > 3)
print(4 <= 3)
```

    True
    False
    


```python
print(3 == 3)
print(2 != 6)
```

    True
    True
    


```python
# Can use in to test whether something exists in a data structure
# like a list

```




    True




```python
# or a dictionary
temp_dict = dict()
print(temp_dict)


```

    {}
    




    False




```python
# or if it is not in a data structure



```




    True



These conditonal statements are returning True and False when you run this code. These just so happen to be another data type, **booleans**. These are the simplest ones, as they can only be `True` or `False`. You can also make vairables have boolean values, and test those.


```python
#example
test = True

# Can test True/False in a few ways. Using ==, or is/not.
```




    True



Now that we've got some basics down, let's try to use these inside something a bit more complicated

Take a situation like this for example - 

It's early morning. I wake up, and need to get ready for the day. What decisions should I make? What should I check before I leave?

Firstly, let's say that it's winter.


```python
winter = True #this is a Boolean type. Booleans are True or False.
```

I can now use the function, `if`, to test something and then perform an action based on that.


```python
if winter is not True:
    print("Oh good, I can wear a dress again")

print("That's some interesting weather we're having")
```

    That's some interesting weather we're having
    


```python

```


```python

```


```python

```


```python

```


```python

```

We can also place conditional statements within a conditional statement. This is known as nesting.


```python

```


```python

```

### Challenge 2

Together with your team mates, come up with your own morning routine. Try to use as many of the conditional testers as you can, without nesting more than 2-3 if statements.




```python

```


```python

```


```python

```

# For Loops

- Explain what a for loop does.
- Correctly write for loops to repeat simple calculations.
- Trace changes to a loop variable as the loop runs.
- Trace changes to other variables as they are updated by a for loop.




Suppose we want to print each character in the word "lead" on a line of its own. One way is to use four print statements:


```python
element = "lead"
print(element[0])
print(element[1])
print(element[2])
print(element[3])
```

    l
    e
    a
    d
    

But that's a bad approach. Firstly, you're doing a lot more typing than you need to, and it doesn't scale well. If you wanted to print every single letter in a sentence, or paragraph, you'd spend more time programming it than if you had just copied it out yourself. 

Secondly, if you were trying to automate something - so that it does something without you needing to be there every step of the way - this approach wouldn't work at all. Not every string, or list, or dictionary, is going to be the exact same size. You would need to program a new code every time you got new data.

Instead, we can use `for` loops. This is a function that lets us "iterate" over your strings and other data structures.


```python
for char in element:
    print(char)
```

    l
    e
    a
    d
    

The general structure of a `for` loop looks like this

```python
for variable in collection:
    do a thing
```


```python
length = 0
for vowel in 'aeiou':
    length = length + 1
print 'There are', length, 'vowels'
```


```python

```


```python

```

Note that a loop variable is just a variable that's being used to record progress in a loop. It still exists after the loop is over, and we can re-use variables previously defined as loop variables as well:


```python
letter = 'z'
print("Before the loop, letter is", letter)
for letter in 'abc':
    print (letter)
print ('after the loop, letter is', letter)
```

    Before the loop, letter is z
    a
    b
    c
    after the loop, letter is c
    

We can naturally loop over each of the elements of a string because strings are actually an example of a sequence data type. Generally speaking, we can only use a **collection**, as defined earlier, to loop over if it is an *iterable*. 

An example of data types which are inherently iterable are lists and strings


```python
for i in [1,2,6,4]:
    print (i)
```

    1
    2
    6
    4
    

For everything else, we need to create or use an iterator


```python
tempDict = {"key1":"value1","key2":"value2","key3":"value3"}

print (tempDict)

for k,v in tempDict:
    print(k,v)
```

#### Range

The `range()` function allows us to create our own iterator when using loops.


```python
# from 0 to 3 (non inclusive)
range(3)
```




    range(0, 3)




```python
#start and end
range(2,5)
```




    range(2, 5)




```python
# from 2 to 7 (non inclusive), stepping by two
range(2,7,4)
```




    range(2, 7, 5)




```python

```

    True
    

### Challenge 3

In your teams, write a loop that calculates the same result as 5 \*\* 3 using multiplication, without using exponentiation.

**Extra points**: try to make the loop use variables defined outside the loop, instead of explicitly programming 5 and 3.


```python




```


```python

```


```python

```

# While Loops

The while statement allows you to repeatedly execute a block of statements as long as a condition is true. A while statement can have an optional else clause.




```python
n = 0

while n < 5:
    n = n+1
    print("loop number:", n)
else: 
    print("end of the line, sucker")
```

    loop number: 1
    loop number: 2
    loop number: 3
    loop number: 4
    loop number: 5
    end of the line, sucker
    

How we could use a while loop to do the exponential calculations earlier


```python
power = 3
n = 5
start = None

while power > 0:
    if start is None:
        start = n
    else: 
        start = start * n
    power -= 1
    

print (start)
```

    125
    


```python

```


```python

```

Let's get a bit more complicated.

This code inputs an integer n for which it computes and prints the nth Fibonacci number. Remember that Fibonacci sequence is that every number after the first two is the sum of the two preceding ones, and goes approximately like:
**1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...**



```python
# Make the fibonacci sequence
```

    Fn = 1
    

Here is how the algorithm works in a bit more detail:

- We first initialize (set to their starting values) variables f0 and f1 to 0 and 1 respectively.
- Then we run a loop as long as n > 1. 
- In that loop, we compute the sum f0 + f1 and save it for later in the variable nxt (short of "next", which we don't use because next is a built-in Python function).
- We assign f0 = f1 and f1 = nxt. In other words, the new value of f0 is equal to the old >value of f1 and the new value is equal to the sum of old >values of f0 and f1.
- We reduce n by 1.


```python

```


```python

```

### Challenge 4

Write a `while` loop that takes a string, and produces a new string with the characters in reverse order, without using the `.reverse()` function:
i.e. 'Newton' becomes 'notweN'.


```python

```
