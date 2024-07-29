# Python for JS Devs

This repo contains the basics of python for my next job hunt.

1. [Fundamental unit in Python]
2. [Anatomy of an object in python]
3. [Assignment Operator]
4. [Comments]
5. [Identation]


---

[Fundamental unit in Python]: #fundamentals-unit-in-python
[Anatomy of an object in python]: #anatomy-of-an-object-in-python
[Assignment Operator]: #assignment-operator
[Comments]: #comments
[Identation]: #identation


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

### Identation
