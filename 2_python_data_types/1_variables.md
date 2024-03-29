# Python variables

In any programming language, variables are one of the most important basic-concept. Variables are used to hold/reference the data. In a few languages, variables can be considered as the box containing a value or data. But in Python, the variable does not hold the value itself, but they hold the reference to that value.

## Variables in Python don't hold the data, they reference to the location of the data

We can confirm this by using the `id()` function, which returns the memory address of the object.

For example, for two different variables the location of the stored value is different, but if two variables have the same values then the `id()` function will print out the same memory address for both the variables, indicating that they are references to the same object.

```python
# Declare a list
a = [3, 4, 5]

# Declare another list
b = [7, 8, 9]

# Print memory address for both 'a' and 'b'
print(id(a))
print(id(b))

# Output (Different memory location for both the variables):
140188289375280
140188290635632

# But if we do:
a = [3, 4, 5]
# Assign the variable 'a' to the variable 'b'
b = a

print(id(a))
print(id(b))

# Output (Same memory location for both the variables):
139761911799488
139761911799488

```

Examples of different types of variable declaration in Python.

```python
developer_name = "John"            # string
age = 30                            # int
experience_in_years = 5.8           # float
programming_language = "Python"     # string
is_on_leave = False                 # boolean
```

Here, 👆 `developer_name`, `age`, `experience_in_years`, `programming_language` and `is_on_leave` are a few examples of variables in Python

Check the ids of the variables above

```python
developer_name = "John"
print(id(developer_name))       # 140549527402160

age = 100
print(id(age))                  # 9804416

experience_in_years = 150.25
print(id(experience_in_years))  # 140118263398640

is_on_leave = False
print(id(is_on_leave))          # 9486304

# But in case of a list.

b = [1, 2, 3, 4, 5]
print(id(b))                    # 140118263437440

# if we append the list the id remains same and the list get appended to the same memory location
b.append(6)
print(id(b))                    # 140118263437440
```

## Dynamic typing nature of Python

Python is called a dynamically typed language which means variables are created without type hinting the variable name. This means variables can reference any type of object. Therefore, if we do the following, Python does not complain:

```python
a = 'Python'             # referencing string
a = 100                 # referencing int
a = 150.25              # referencing float
a = [1, 2, 3, 4, 5]     # referencing list
```

Python creates the variable whenever we assign any type of object to it. We read it as the variable 'a' is assigned to the object 'John', as an object is created first and then it is available to be assigned to any variable.

## Id, Type and Values

In Python, everything is an object and every object has an identity, value and type.

**ID**: An id is the object's address in the memory and it never changes once it is created. Use the in-built function id() to check the identity of any object. It returns an integer. And, the `is` operator compares the identity of two objects

```python
language = "Python"
print(id(language))     # 140549527402160
```

**Type**: The operations that an object supports are determine by an object’s type. The type also defines the possible values for that object. Use in-built function `type()` to check an object’s type.

```python
a = 'Python'
print(type(a))          # <class 'str'>

a = 100
print(type(a))          # <class 'int'>

a = 150.25
print(type(a))          # <class 'float'>

a = [1, 2, 3, 4, 5]
print(type(a))          # <class 'list'>
```

Even the `type` function is an object of some type. Let's check this:

```python
print(type(type))       # <class 'type'>
```

## More in type()

```python
print(type({}))
# Output: <class 'dict'>

print(type([]))
# Output: <class 'list'>

print(type(()))
# Output: <class 'tuple'>

print(type(set()))
# Output: <class 'set'>
```

**Like an object's identity, the type is also unchangeable.**

**Value**: The value of some objects is changed. The objects whose values can be changed are called **mutable**, and the objects whose values can not be changed are called **immutable**. There is a separate tutorial for immutable and mutable data types.

## Single line assignment

```python
a, b, c = 4, 5, 6
```

## Constants

While declaring a variable value as constant, python convention is to use variable names in capital.

```python
PI = 3.14
INCREMENT = 7
```

## Protected and Private variables

```python
# Protected variable: starting with single underscore('_')
_student_name = 'John'

# Private variable: starting with double underscore('__')
__company_name = 'XYZ Company'
```
