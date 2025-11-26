# Python Data Types

## Numeric Type
### Integer
### Float
### Complex

## Text Type
### String


## Sequence Type
### List

#### List Operations

### Tuple


### Range


## Mapping Type
### Dictionary
```python
Biodata ={
    "Name" :"Aravind",
    "Age" : 22
    }
print(Biodata)
```

## Set Type

## Boolean




## None Type



# Operators in Python

## Arithmetic Operators
- Addition
- Subtraction
- Multiplication
- Division
- Modulous
- Exponent
- Floor Division


## Assignment Operator
- =



## Comparison Operator
- \>
- <
- \>=
- <=
- ==
- !=

## Logical Operators
- AND
- OR
- NOT

## Membership Operator
- IN
- NOT IN

## Identity Operator
- is
- is not
  
It checks whether two variables refer to the same object in memory.
It's not concerned with the values inside the objects, but whether they are the exact same instance.


```python
a = [1, 2, 3]
b = a

print(a is b)  # Output: True (because both `a` and `b` refer to the same object in memory)

c = [1, 2, 3]
print(a is c)  # Output: False (because `a` and `c` are different objects, even though their values are the same)

```

# Print formatting
## Placeholder passing

```python
name="Aravind"
course='DSA'
print("Hello {1} Welcome To {0}".format(course,name))
```
## F-Strings
```python
name="Aravind"
course='DSA'
print(f"Hello {name} Welcome to {course}")
```

## Multiline Assignment



## Line-breaking

# Type Conversion and Casting

# Operator Overloading

