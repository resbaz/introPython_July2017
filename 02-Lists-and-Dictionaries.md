
# Lists and Dictionaries in Python

### Learning Objectives

- Lists:
    - To understand the basic structure of a list
    - To know how to create, index and subset a list
    - Learn the difference between mutable and immutable objects
    - Adding and deleting list elements
        - Describe the difference between append(), insert(), del, remove() & pop()
    - List functions
- Dictionaries
    - Understand the underlying structure of a dictionary
    - Know how to access dictionary elements
    - Adding and deleting dictionary elements
        - Describe the difference between del & pop()
- Be able to describe when a situation is best suited for a dictionary vs. a list


## Lists

A list allows you to store many different values, of many different data types, in the same structure. 

We can make a list by putting the values into square brackets, []



```python
#we can make empty lists
print(list(), [])
```


```python
#Or lists with things inside them
[1,2,3,4]
```


```python
#To save this list though we need to assign it to a variable

```

### Indexing a list
Sometimes we only want to access certain *elements*, or data, inside a list. We can do by callingthe list *index*, or the position of the data element, from inside the list


```python
temp_list = [1,2,3,4]

temp_list[1]
```

Wait, but that's given us the number 2? Why?

---

This is because Python actually works based on 0-indexing, meaning that it starts counting from 0 instead of 1. 

This means that if we want to get the first element of our list, we actually have to call list[0], instead of list[1]


```python
temp_list[0]
```

You can also use negative index numbers to start counting from the end of the list instead


```python
print('first and last:', temp_list[0],"and", temp_list[-1])
```


```python

```


```python

```

### Changing list items

One of the properties of lists is that you can over-write data inside the list with new values. This means that lists are **_mutable_**, or changeable.

In contrast, strings are actually immutable. If you want to change something inside a string, you have to replace it with a whole new one.



```python
characters = []
```


```python
print("characters was:", characters)



print("characters is now:",characters)
```


```python
# Let's try this with a string



```

### Slicing

Slicing allows us to access *sections* of the list, instead of the whole thing, or only a single element.

Slicing can be used on a variety of python data structures, such as strings.


```python
odds = [1, 3, 5, 7]

print('Index 1 to 3 is', odds[1:3])

```


```python
print('Index 2 to end is', odds[2:])
```


```python
# but don't go over the edge!

odds[4]
```


```python
print('Index 1 to -1 is', odds[1:-1])
```


```python
print("Start to index 2 is:", odds[:2])
```


```python
print('Index start to end is', odds[:])
```


```python
# You can do the same thing on strings
```


```python

```

### Adding and Deleting List Elements

#### Append
To add a new variable into a list, we can use the `.append()` method. This adds the newest variable onto the *end* of the list.



```python
print("Odds before:", odds)

odds.append(9)

print("Odds after:", odds)
```

#### Insert

`insert()` lets us put a new item into your list at the location of your choosing. 

The basic structure of this is list.insert(list index,variable)


```python
odds.insert(5,11)
print(odds)
```


```python
odds.insert(0,0)
print (odds)
```

#### Deleting items

There are three options when deleting items from your list. 

The first is `del`, which removes the item at a specific index location and returns your modified list back to you. This works based on this kind of format, `del list[index]`


```python
del odds[5]
print (odds)
```


```python
#Error
del odds[12]
```

The second is `remove()`. Rather than deleting from a specific list index, `remove()` will find and delete the first matching *value* from your list, and return your modified list back to you.

It's typically used list this: `list.remove(variable)`


```python
odds.remove(11)
print(odds)
```


```python
#Error
odds.remove(12)
```

Lastly we have `.pop()`. 

Like `del`, `pop()` is index based. However, while your list is still modified, `pop()` actually gives you back the value that you've removed. 


```python
odds.pop(0)
```


```python
print("Odds before pop:,"odds)

odds.pop(4)

print("Odds after pop:", odds)
```


```python
# Error
odds.pop(5)
```


```python

```

#### Other list functions

More useful list functions are `list.sort()`, and `list.reverse()`

`list.sort()` will sort your list based on "lexicographic order". This means that capital A-Z are sorted before lower-case a-z. 

However, sort() will not work if you have both strings and numeric data types in your list. It can only work if they are all strings, or all numeric (a combination of int and float).


```python
names = ["Kahli", "Errol", "Mohsen","Hao"]
```


```python
names.sort()
print(names)
```


```python
names.append(3)
print("New names:", names)
```


```python
#Doesn't work with a mixture of data types
names.sort()
```


```python
# But is fine with both ints and floats
nums = [1,2.5,1.25,8,4]

nums.sort()

print(nums)

```

`reverse()` will take your list and reverse the order of the elements. 

So a list that was [1,2,3], would become [3,2,1]


```python
nums.reverse()
print(nums)
```


```python
#the list doesn't have to be sorted either
nums = [1,3,2,6,4,9,6]

nums.reverse()

print(nums)

```

### Challenge

So far, most of the elements that we have added to our collections have been string, float, or integer data types. However, the elements of a list can also be a list, or another storage type. This process is called nesting and it is a bit like Russian dolls. 


```python
pets = ['dogs', 'cats', 'fish']
print( pets )
pets.pop(0)   # Get rid of dogs
dog_breeds = ['bulldog', 'terrier', 'greyhound']
pets.append(dog_breeds)  # append list of dog breeds available
pets
```

With your team mates, work out how to index the nested list so you can sort it, and then return the greyound string

Hint: if you index a list like this, `list[0]`, how might you index a list inside a list?


```python

```


```python

```


```python

```


```python

```

## Dictionaries

Dictionaries are another kind of data type used by Python.

A dictionary is an associative array (also known as hashes, for those who have programmed before). 

rather than using an index, like a list, a dictionary uses "keys", typically strings or numbers, that you define. Each "key" of this dictionary is mapped to a value. 

Like a list, a dictionary can contain any kind of data type for it's values. 

Dictionaries consist of key-value-pairs, and as they can only be accessed using the 'key' names, they are unordered. 



You can make a dictionary by using `dict()`, or `{}`


```python
# An empty dictionary

```


```python
# An example of a dictionary with keys and values

```

    {'iphone': 2007, 'iphone 3G': 2008, 'iphone 3GS': 2009, 'iphone 4': 2010, 'iphone 4S': 2011, 'iphone 5': 2012}
    


```python
# Accessing your dictionary



```


```python
# Dictionaries are mutable (they can be changed)



```

#### Adding and deleting from your dictionary

Adding to your dicitonary is simple - you just "call" your dictionary with a new key name, and assign it a value.



```python
# Adding new elements


```


```python
# Deleting elements
# same as lists, "pop" gives you the deleted element



```


```python
# While del removes the key and value from the dictionary. 


```
