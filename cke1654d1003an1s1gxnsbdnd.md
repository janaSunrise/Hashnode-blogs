## 🔗 Making ZIP in Python Easy.

The concept of zipping is not properly understood by a lot of people! Especially because of it's working, parameters and such. Today, I'll make it easy to understand and work with it, in an easy and simple manner. 😁

So, Let's Start!

### What is Zipping?
So, basically Let's say I have a List of Numbers, and A List of Numbers in Words, and I want each of the integer numbers, to be paired to it's respective word format, But I have no idea how, so, This is the Place Where **Zipping** Comes into Play!

In general, **Zipping** Is a concept Which is used to pair two or more kind Similar kind of related values, or iterables, And Connect them to be paired as a single value, which can be in Any Format which is accessible, like
- A Dictionary
- A List of Tuples
- Other datatypes

### Definition
The `zip()` function in Python takes iterables as it's input parameter, which can be anything such as zero, or more, and aggregates into a tuple, and Returns it to the User.

### Syntax
```python
zip(*iterables)  # takes in argument *iterables, which is parsed as a list.
```

### What's iterables?
Iterables are a special data type, that you can iterate through, or move through using a loop, or a special function.

For example, **List** is an Iterable.

Method 1: **Using a Loop**
```python
numbers = [1, 2, 3, 4, 5]  # Define a list of numbers

for number in numbers:  # access each number using a for loop
    print(number)  # print the number
```

**Output of the code**:
```
1
2
3
4
5
```

Method 2: **Using a Special Function**
```python
# Create a list with my name split.
myname = ["Sunrit",  "Jana"]

# Get full name using join method.
full_name = " ".join(myname)

print(full_name)  # print my full name
```

**Output of the code**:
```
Sunrit Jana
```

### Return value from `zip()`
Basically, the `zip()` function returns an iterator of tuples based on the iterable objects, But still there are some rules or constraints, they are:
- If no parameter is passed, An Empty iterator is returned.
- If single iterable is passed, `zip()` returns an iterator of tuples, with each tuple having an single element.
- If multiple iterables are passed, `zip()` returns an iterator of tuples, with each tuple containing elements from all the amount of iterables passed
- **Exception Case**: let's assume, 2 iterables are passed, with 3 elements in first one, and 4 elements in second one. Then the returned iterator will be containing 3 tuples, since it doesn't have more elements to pair the rest equally.

### Examples
#### 1. No Parameter Passed.
```python
result = zip()

result_list = list(result)

print(result_list)
```

**OUTPUT:**
```
[]
```

#### 2. Double parameter Passed
```python
numbers = [1, 2, 3, 4]
numbers_in_words = ["one", "two", "three", "four"]

# Zip them altogether
result = zip(numbers, numbers_in_words)

# Make it set, to prevent duplicates
result_set = set(result)

print(result_set)
```

**OUTPUT:**
```
{(1, 'one'), (2, 'two'), (4, 'four'), (3, 'three')}
```

#### 3. Unpacking the Zipped Values
```python
angles = ["x", "y", "z"]
values = [1, 2, 3]

result_list = list(zip(angles, values))  # Zip them, then make it a list

print(result_list)

# Now start unpacking
ang, val = zip(*result_list)

print(f"Angles = {ang}")
print(f"Values = {val}")
```

**OUTPUT:**
```
[('x', 1), ('y', 2), ('z', 3)]
Angles = ('x', 'y', 'z')
Values = (1, 2, 3)
```

So, I guess You got the concepts to understand, and next time, be sure to use these while working, instead of Looping over them, and joining the values, this is a quite useful method, and thanks for stopping by, and Learning a New Concept! 🎉

As a developer, you must experiment and build to figure out new things and learn more! That's the beauty of code.

Stay tuned for new Guides on various topics! 😄
See you next time! 👋
