# Beginner's Python - Day 1 Homework Challenge

## Challenge Question 1

Create a for loop that will go through the example list given below. If the list item is a number below or equal to 10, add this number to another list for "odd" or "even" numbers. If it's a string, add it to another list.

Sort the contents of these three lists, then print the outputs of all three on separate lines.

An example of the list you might recieve is below, along with some code to help you get started. 

```python
list1 = [1,3.2,"Are you having a nice day?", 2,4,"Difficulty Increased!",10,15,11.5,5,6,9,8.2,7,14.8,13,["Nested list","What are you","gonna do about it?"]]

odd = []
even = []
stringList = []

for i in list1: #this needs to be edited
    # 4 spaces, or 1 tab, means that we're now inside the for loop
    if type(list1[i]) is int or type(list1[i]) is float:
        # similarly, another 4 spaces means we're inside the if statement
        
        # remember that converting a float to an int always causes it to round down?
        # remember our discussion about modulo, %, to test the remainder?
        if (condition):
            odd.append(list1[i])
    #now we're outside of the first if statement
    elif type(list1[i]) is (condition):
        #perform an action

# Now we're outside of the for loop
odd.sort()

```
---

Using this list, you should get an answer similar to this:


evens list is: [1,2,6,8.2,10]

odds list is: [1,3.2,5,7]

strings list is: ["Are you having a nice day?","Difficulty Increased!"]

---

Happy coding!

