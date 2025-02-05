# Python for JS Devs

This repo contains the basics of python for my next job hunt.

1. [Fundamental unit in Python]
2. [Anatomy of an object in python]
3. [Assignment Operator]
4. [Comments]
5. [Mutable & Immutable Objects in Python]
6. [Operators in Python]
7. [Types of errors]
8. [venv module]

---

[Fundamental unit in Python]: #fundamentals-unit-in-python
[Anatomy of an object in python]: #anatomy-of-an-object-in-python
[Assignment Operator]: #assignment-operator
[Comments]: #comments
[Mutable & Immutable Objects in Python]: #mutable--immutable-objects-in-python
[Operators in Python]: #operators-in-python
[Types of errors]: #types-of-errors
[venv module]: #venv-module


### Fundamentals unit in Python

Token is a **smallest** and **fundamental** unit of a python script.

Types of tokens:
- **Punctuators** - `[]`, `{}`, `()` 
- **Literals** - "hello" is a string literal, 5 is a integer literal, 3.0 is a flot literal and so on which basically means a single thing in a program
- **Keyword** - think of it as predefined "words" in the python language which we cannot use anywhere in a script.
- **Identifier** - Name(s) that we provide for a variable
- **Operators** - Basic operators like `+`, `-`, `*`, `\`, `\\`, `%` and advanced operators like `and`, `or`, `not`, `in`, and `not in` etc.

Finally, I feel liberated because Everything in python is an `object`, every JavaScript developer can understand the feeling of objects 😆
Check this out -> [Is Everything an object in python ?](https://stackoverflow.com/questions/865911/is-everything-an-object-in-python-like-ruby)

To view all the keywords in python3 follow the below steps:
- Run `python3` command in your terminal
- Import the keyword module -> `import keyword`
- Finally run -> `print(keyword.kwlist)`

  <img width="1438" alt="image" src="https://github.com/user-attachments/assets/91b56572-8426-430b-aa83-c86011b8dd65">

---

### Anatomy of an object in python

<img width="804" alt="image" src="https://github.com/user-attachments/assets/192cd799-6bcc-4677-b3ad-bf05d96a4a0b">

Any variable we define is a reference to the memory address of the object which holds the actual value in python.

#### Few escape sequences in python

| Token       | Category | 
| ----------- | --------------------- | 
| \\          | Backslash             |
| \'          | Single quote (')      |
| \"          | Double quote (")      |
| \b          | Backspace             |
| \n          | New line              |
| \t          | Horizontal Tab        |

### How to get the type of a variable and what is an ID of an object ?

We can use `type()` function to get variable data type as shown below. `id()` is used to get the unique value assigned to an object, in the example below `x` and `y` hold the same integer value and hence they have the same object id.
```python3
x=30
print(type(x)) # <class 'int'>

x=30
print(id(x)) # 4344671440
y=50-20
print(id(y)) # 4344671440
```
---

### Assignment operator 

The assignment operator `(=)` can be used assign value(an object reference to memory address) to an identifier.

> The assignment of a value to a variable happens from RHS to LHS.
>
> LHS <- RHS
>
> Variable Name(Identifier) <- value 

Example:

```python3
name='Bruce Wayne' # String data type 
super_powers=['rich','always has krypton in his suite','discipline','marial arts'] # List data type
```

In python we can also assign multiple values to multiple variables in a single statement and same value to multiple variables as shown below

```python3
name,place,age="Thor","Asgard",1500
iron_man = hulk = captain_america ="avenger"
```

**NOTE: In python variable names are case-sensitive meaning `age` and `AGE` are completely different variables with unique object id**

---
### Comments 

#### Single line comment:

```python3
# This is a single line comment
```

#### Multi-line comment:

Pro-tip from the creator of python => [pro-tip](https://x.com/gvanrossum/status/112670605505077248)

```python3
'''
This is a multi-line comment 
which involves multiple lines of instructions
'''
```
---

### Mutable & Immutable Objects in Python:

Mutable objects -> list, dictionaries, set, byte array

<img width="974" alt="image" src="https://github.com/user-attachments/assets/0577286e-199f-4cc3-8770-c4ec06dc57a0">

Immutable objects -> Tuples, Strings, integers, floats, Boolean, Bytes and Frozensets

<img width="1071" alt="image" src="https://github.com/user-attachments/assets/8c097d47-7359-4d8a-bc1b-12b3de9c4906">

---

### Operators in Python

#### Arithimetic operators:

- `+` for addition operation
- `-` for substraction operation
- `*` for multiplication operation
- `**` for exponential operation
- `/` for floating point division which returns quotient in floating point
- `//` for floor division which returns quotient in integer
- `%` for modulo division

  <img width="488" alt="image" src="https://github.com/user-attachments/assets/33fa249d-86c8-4a77-8ab6-4f94ba2707ed">

#### Relational operators:

- `>` for checking if LHS operand is greater than RHS operand
- `<` for checking if LHS operand is less than RHS operand
- `>=` for checking if LHS operand is greater than or equal to RHS operand
- `<=` for checking if LHS operand is less than or equal to RHS operand
- `==` for checking if LHS operand is equal to RHS operand
- `!=` for checking if LHS operand is not equal to RHS operand
  <img width="477" alt="image" src="https://github.com/user-attachments/assets/cace17cd-83e9-4db1-ae3c-cd8b45f7d620">

#### Logical operators:

- `not` operator is similar to boolean `NOT` gate used for negation
- `or` operator is similar to boolean `OR` gate used for checking if either of two values are `True`
- `and` operator is similar to boolean `AND` gate used as a hard rule for both two values to be `True`

#### Short-hand operators:
- `+=` is a shorthand for `x=x+1` which can be written as `x+=1`
- `-=` is a shorthand for `x=x-1` which can be written as `x-=1`
- `*=` is a shorthand for `x=x*1` which can be written as `x*=1`
- `/=` is a shorthand for `x=x/1` which can be written as `x/=1`
- `%=` is a shorthand for `x=x%1` which can be written as `x%=1`
- `**=` is a shorthand for `x=x**1` which can be written as `x**=1`
- `//=` is a shorthand for `x=x//1` which can be written as `x//=1`

#### Membership operators
- `in` operator is used for checking if a character or substring exists in a string and return `True` else `False`
  Example:
  ```python
    name='Bruce Wayne'
    print('Bruce' in name) // True
  ```
- `not in` operator is used for checking if a character or substring does not exist in a string and return `True` else `False`
  Example:
  ```python
    name='Bruce Wayne'
    print('Robin' in name) // True
  ```

#### Identity operators
- `is` operator is used to check if two objects point to the same memory address and return `True` else `False`
  Example:
  ```python
    a=100
    b=a
    print(a is b) // True
  ```

- `is not` operator is used to check if two objects do not point to the same memory address and return `True` else `False`
  Example:
  ```python
    a=100
    b=500
    print(a is not b) // True
  ```
---

### Types of errors

- Logical
  ```python3
  print(10+4/2) # output is 12 which is wrong.
  print((10+4)/2) # 7 is the correct output in this case.
  ```  
- Semantic
- Syntax
  ```python3
  # example of a syntax error
  Print("hello world")
  ```
- Runtime
  ```python3
  # example of a runtime error
  print(10/0)
  # calling an a function which is not declared
  getExpense()
  ```

  ---

### venv module

`venv` module helps us maintain the python and application dependancies version self-contained within a directory which means we can create unique venv environment for each python applications with desired version and dependancies.

A good example of venv is when we have multiple applications and when all the applications require specific version of a python library then for each application we can isolate the dependacies with venv

Create a venv directory:

`python3 -m venv <directory-name>`

Activate the venv: (macOS or Linux)

`source <directory-name>/bin/activate`

Deactivate the venv: (macOS or Linux)

`deactivate`



