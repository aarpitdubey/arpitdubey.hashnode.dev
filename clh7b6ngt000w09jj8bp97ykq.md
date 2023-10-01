---
title: "Python For Data Science - I"
seoTitle: "Python For Data Science - I"
datePublished: Wed May 03 2023 06:19:55 GMT+0000 (Coordinated Universal Time)
cuid: clh7b6ngt000w09jj8bp97ykq
slug: python-for-data-science-i
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683094435231/5dff6129-4a2f-4ab7-85ce-ddd5b659add2.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1683094553194/693992ab-75ce-4386-9e7d-12827e7397ce.gif
tags: python, data-science, ineuron, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline-lco-css-learncodeonline-cssselectors-hiteshchoudharylco-code-with-hitesh-choudhary, ineuron-shashankmishrasunny-savita

---

# Why Python?

* It is a very simple language to learn
    
* Rich Libraries / Best Packages for AI such as
    
    matplotlib, numpy, pandas, scipy, scikit-learn, Tensorflow etc.,
    
* iPython Notebooks for interactive data analysis and modeling
    
* Extensively used in the industry
    

| **Features by Software** | **Python** | **R** | **Java** | **C++** |
| --- | --- | --- | --- | --- |
| **Speed** | Slower | Depends on configuration and add-ons | Faster | Very fast |
| **Accessibility** | Easy to learn | Complex | Easy to learn | Complex |
| **Variable** | Dynamic | Dynamic | Static | Declarative |
| **Data science focus** | Machine learning and automated analysis | Exploratory data analysis and building extensive statistical libraries | Used across projects with open-source assets | Not as widely used but very powerful implementations |
| **Programming Paradigm** | Object-oriented | Functional language | Object-oriented | Multi-paradigm (imperative & object-oriented) |

1. ## Keywords
    
    * <mark>Keywords are the </mark> **<mark>reserved words</mark>** <mark>in Python.</mark>
        
    * <mark>We cannot use the </mark> **<mark>variable name</mark>**<mark>, </mark> **<mark>function name</mark>**<mark>, (or) any </mark> **<mark>other identifier</mark>** <mark>as a keyword.</mark>
        
    * Keywords are **case-sensitive**.
        
    
    ```python
    import keyword as kwd
    print(kwd.kwlist)
    print('\nTotal number of keywords: ', len(kwd.kwlist))
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682354075016/642b06cd-f5d8-497d-9094-d19b3deb232c.png align="center")
    
    we can see there are **36** keywords in this Python version (3.9.16).
    

```python
# for checking the python version in jupyter notebook use this code snippet.
from platform import python_version
print(python_version())
```

we can also see the keywords one by one using a simple for loop :

```python
import keyword as kwd

for i in kwd.kwlist:
    print(i, end="\n")
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682354216830/693fdd79-8773-48cc-a0f3-7816830ae7c8.png align="left")

1. ## Identifiers
    
    Identifier is the name given to entities like classes, functions, variables etc., python helps in differentiating one entity from another.
    

### **Rules for Writing Identifiers**

Identifiers can be a combination of letters in lowercase (a to z) or uppercase (A to Z) or digits (0 to 9) or underscore (-).

* An identifier cannot start with a digit (or) number like, `1variable` is invalid, but `variable1` is perfectly fine.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682362061577/7c772c68-6fa5-41e8-8533-71acac7a8ce0.png align="left")
    
* Keywords cannot be used as identifiers
    
    ```python
    abc_12 = 12
    print(abc_12)
    
    global = 1
    print(global)
    
    12_abc = 12
    print(12_abc)
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682362409457/b8274ae0-9341-4de9-bfd7-3b2cbb9bd7e0.png align="center")
    
* Cannot use special characters (or) symbols like `!, @, #, $, %` etc., in our identifier.
    

Python syntax includes words that represent objects and commands, as well as punctuation that gives the words structure, hierarchy, and context. Together, the words and punctuation communicate ideas and processes; this is known as semantics.

Semantics is the meaning conveyed by the syntax. The best way to learn syntax and semantics is through exposure. Practice coding and become familiar and comfortable with reading other people’s code. In addition, there are some general conventions that practitioners use to help maintain stylistic uniformity within the language.

Coding languages are similar to spoken languages in that they have a way to classify words according to their function. For example, English sentences are composed of nouns, verbs, prepositions, etc.

Here are some of the basics:

* **Variables:** Represent data stored as strings, tuples, dictionaries, lists, and objects (note: future readings explain these categories)
    
    * Example: **student\_name**
        
* **Keywords:** Special words that are reserved for specific purposes and that can only be used for those purposes
    
    * Examples:
        
        * `in`
            
        * `not`
            
        * `or`
            
        * `for`
            
        * `while`
            
        * `return`
            
* **Operators:** Symbols that perform operations on objects and values
    
    * Examples:
        
        * `+`
            
        * `-`
            
        * `*`
            
        * `/`
            
        * `**`
            
        * `%`
            
        * `//`
            
        * `>`
            
        * `<`
            
        * `==`
            
* **Expressions:** A combination of numbers, symbols, and variables to compute and return a result upon evaluation
    
* Example: `[1, 2, 3] + [2, 4, 6]`
    
* **Functions:** A group of related statements to perform a task and return a value
    
* Example:
    
    ```python
    def to_celsius(x):
       '''Convert Fahrenheit to Celsius'''
       return (x-32) * 5/9
    
    to_celsius(75)
    ```
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683032679765/a2842524-f513-4269-9aca-9ffd1cadf816.png align="center")
    
    * **Conditional statements:** Sections of code that direct program execution based on specified conditions
        
        * Example:
            
            ```python
            number = -4
            
            if number > 0:
               print('Number is positive.')
            elif number == 0:
               print('Number is zero.')
            else:
               print('Number is negative.')
            ```
            
        * ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683032731133/d7c92d8e-823b-4dbc-b39f-3cee3746cb48.png align="center")
            

## **Naming rules and conventions**

When assigning names to objects, programmers adhere to a set of rules and conventions which help to standardize code and make it more accessible to everyone. Here are some naming rules and conventions that you should know:

* Names cannot contain spaces.
    
* Names may be a mixture of upper and lower case characters.
    
* Names can’t start with a number but may contain numbers after the first character.
    
* Variable names and function names should be written in snake\_case, which means that all letters are lowercase and words are separated using an underscore.
    
* Descriptive names are better than cryptic abbreviations because they help other programmers (and you) read and interpret your code. For example, student\_name is better than sn. It may feel excessive when you write it, but when you return to your code you’ll find it much easier to understand.
    

Tim Peters, a Python programmer, wrote this now-famous “poem” of guiding principles for coding in Python:

```python
import this
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683032867129/737a88ae-2be9-49ec-9369-e8d4b715a75f.png align="center")

1. ## Comments
    

* Comments are lines that exist in computer programs that are ignored by compilers and interpreters.
    
* Including comments in programs makes code more readable for humans as it provides some information (or) explanation about what each part of a program is doing
    
* In general, it is a good idea to write comments while you are writing (or) updating a program as it is easy to forget your thought process later on and, the comments written layer may be less useful in the long term.
    
* we use the hash(#) symbol to start writting a comment
    

```python
# Print Hello, World! to console
print('Hello, World!')
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682366641017/c3ddee06-bb61-4d36-afc1-4a16e55f2c13.png align="center")

**Multi-line Comments :**

If we have comments that extend multiple lines, one way of doing it is to use hash (#), at the beginning of each line.

```python
# This is a long comment
# and is extends
# Multiple lines
```

Another way of doing this is to use triple quotes, either ''' or """.

```python
"""This is also a
perfect example of
multi-line comments"""
```

**Python Indentation :**

* Most programming languages like C, C++ and, java use braces { } to define a block of code.
    
* A code block (body of the function, loop etc.,) starts with indentation and ends with the first un-indented line. The amount of indentation is up to you, but it must be consistent throughout that block.
    
* Generally, four whitespaces are used for indentation and are preferred over tabs.
    

## **Function syntax**

Define functions using the following syntax and format:

```python
def my_function(parameters):
    '''
    Docstring.
    Summarize the function's behavior and explain its arguments and return values.
    '''
    code block

    return value
```

1. Begin with the def keyword followed by the function’s name, then put its parameters/arguments in parentheses, ending with a colon.
    
    * Python convention is to use snake\_case (lowercase words separated by underscores) for function names.
        
2. For important functions or functions whose purposes or operations are not very obvious, include a docstring. Write the docstring between three opening and closing quotation marks.
    
    * The docstring should be in the form of a command (e.g., “Add two numbers” as opposed to “Adds two numbers”).
        
    * The docstring should summarize the function’s behavior and explain its arguments and return values.
        
    * The docstring should be indented four spaces from the definition statement.
        
3. Write the body of the function.
    
    * All code should be indented at least four spaces from the definition statement, but there can be many levels of indentation depending on the complexity of the code.
        
4. Finally, use a return statement to return a value or a print statement to print something to the console and complete the function. This line should also be indented four spaces.
    

## **return vs print**

* Sometimes the difference between return statements and print statements isn’t clear to new learners of Python. It’s important to understand what each action is and when to use it. Return statements give you a result that you can use for something else. It doesn’t have to be something that prints when the function is run. Print statements print something to the console and nothing more. Think of it like this: a return statement is like your brother going to the market and bringing you back a bag of potatoes. A print statement is like your brother going to the market, coming home, and telling you what kind of potatoes were for sale. With the return statement, you have some potatoes to cook. With the print statement, you just know what potatoes are available, but you don’t have any potatoes.
    

## **Functions vs. methods**

Functions and methods are very similar, but there are a few key differences. Methods are a specific type of function. They are functions that belong to a class. This means that you can use them—or “call” them—by using dot notation.

```python
my_string = 'The eagles filled the sky.'
my_string.split()
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683033555457/c70d8090-f72a-418c-a6b8-9889047bbcfd.png align="center")

The split method is a function that belongs to the string class. It splits strings on their whitespaces.

Standalone functions do not belong to a particular class and can often be used on multiple classes.

```python
 sum([6, 3])
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683033634439/8b798781-a0fc-425a-bd8c-97c877f4cab2.png align="center")

# Python operators

You’ve encountered many Python operators already. Many of them likely feel very familiar to you. After all, there’s nothing novel about addition and subtraction in Python. But there are many more operators than the ones used for basic arithmetic! Operators are characters that enact specific arithmetic, logical actions, or processes. Data professionals use operators all the time in their work, and they’re a rudimentary part of Python programming, so it’s important to learn them. This reading is a guide to the various operators available to you in Python.

### **Comparators**

In Python, you can use comparison operators to compare values. When a comparison is made, Python returns a Boolean result—True or False. Python uses the following comparators:

| **Operation** | **Operator** |
| --- | --- |
| greater than | **\&gt;** |
| greater than or equal to | **\&gt;=** |
| less than | **&lt;** |
| less than or equal to | **&lt;=** |
| not equal to | **!=** |
| equal to | **\==** |

**Notes:**

* The single equals sign (**\=**) is reserved for assignment statements. If you use a single equal sign to make a comparison, the computer will return a **SyntaxError**.
    
* If you try to compare data types that aren’t compatible, like checking if a string is greater than an integer, Python will throw a **TypeError**.
    

## **Logical operators**

* Python also has three logical operators that can be combined with comparators to create more complex statements.
    

These operators are:

* `and`
    
    * evaluates to True only if both statements are true
        
* `or`
    
    * evaluates to True if one or both of the statements are true
        
* `not`
    
    * reverses the evaluation
        
    * If the statement evaluates to True, returns False; if the statement evaluates to False, returns True
        
    
    ```python
    x = 3
    my_list = [3, 4, 6, 10]
    print(x < 3 and x != 0)
    print(x >= len(my_list) or x == min(my_list))
    print(x not in my_list)
    ```
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683033877109/624d6ae9-600f-4a0d-97b8-247ec9e76ae7.png align="center")
    

## **Arithmetic operators**

* Python is also capable of performing mathematical operations using a set of built-in operators. These arithmetic operators are:
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683034451157/d78772c5-fcc5-411d-82a7-cacfc1357f10.png align="center")
    
    | **Operation** | **Operator** | **Example** |
    | --- | --- | --- |
    | Addition | **+** | **\[IN\]  5 + 2** |
    | Subtraction | **\-** | **\[IN\] 5 - 2** |
    | Multiplication | **\*** | **\[IN\] 5 \* 2** |
    | Division | **/** | **\[IN\] 5 / 2** |
    | Modulo (the remainder of a division) | **%** | **\[IN\] 5 % 2** |
    | Exponentiation | **\*\*** | **\[IN\] 5 \*\* 2** |
    | Floor division | **//** | **\[IN\] 5 // 2** |
    

# Object-oriented programming

Object-oriented programming is a programming schema that is based around objects, which can contain both data and code that manipulates that data.

Class is an object’s data type that bundles data and functionality together, and class-specific functionality is in the form of methods and attributes.

**Attributes and methods**

Python classes are powerful and convenient because they come with built-in features that simplify common data analysis tasks. These features are known as attributes and methods.

* **Attribute**: A value associated with an object or class which is referenced by name using dot notation.
    
* **Method**: A function that belongs to a class and typically performs an action or operation.
    

A simpler way of thinking about the distinction between attributes and methods is to remember that attributes are *characteristics* of the object, while methods are *actions* or *operations*.

For example, if the class were Spaceship, then attributes might be:

`name`

`kind`

`speed`

`tractor_beam`

These attributes could be accessed by typing:

`Spaceship.name`

`Spaceship.kind`

`Spaceship.speed`

`Spaceship.tractor_beam`

Notice that these characteristics are accessed using only a dot.

On the other hand, the methods of the Spaceship class might be:

`warp()`

`tractor()`

These methods could be used by typing:

`Spaceship.warp()`

`Spaceship.tractor()`

Notice that methods are followed by parentheses, and they can take arguments. For example, `Spaceship.warp(7)` could change the speed of the ship to warp seven.

## **Defining classes with unique attributes and methods**

Python lets you define your own classes, each with their own special attributes and methods. This helps all different kinds of programmers to build reusable code that makes their work more efficient. You can even build the Spaceship class mentioned previously. The example, here, demonstrates how to do this.

```python
class Spaceship:
   # Class attribute
   tractor_beam = 'off'

   # Instance attributes
   def __init__(self, name, kind):
       self.name = name
       self.kind = kind
       self.speed = None

  # Instance methods
   def warp(self, warp):
       self.speed = warp
       print(f'Warp {warp}, engage!')

   def tractor(self):
       if self.tractor_beam == 'off':
           self.tractor_beam = 'on'
           print('Tractor beam on.')
       else:
           self.tractor_beam = 'off'
           print('Tractor beam off')

# Create an instance of the Spaceship class (i.e. "instantiate")
ship = Spaceship('Mockingbird','rescue frigate')

# Check ship's name
print(ship.name)

# Check what kind of ship it is
print(ship.kind)

# Check tractor beam status
print(ship.tractor_beam)

# Set warp speed
ship.warp(7)

# Check speed
ship.speed

# Toggle tractor beam
ship.tractor()

# Check tractor beam status
print(ship.tractor_beam)
```

**A class is like a blueprint for all things that share characteristics and behaviors**. In this case, the class is Spaceship. There can be all different kinds of spaceships. They can have different names and different purposes.

Whenever you create an object of a given class, you’re creating an **instance** of that class. This is also known as **instantiating** the class. In the code above, every time you instantiate an object of the Spaceship class it will start with its tractor beam set to off. The tractor beam is a class attribute. All instances of the Spaceship class have one. There are also instance attributes. These are attributes that you can assign when you instantiate the object.

```python
# Create an instance of the Spaceship class (i.e. "instantiate")
ship = Spaceship('Mockingbird','rescue frigate')

# Check ship's name
print(ship.name)

# Check what kind of ship it is
print(ship.kind)

# Check tractor beam status
print(ship.tractor_beam)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683020960230/9f0a9417-95ec-4a07-bbfa-eaf84687895c.png align="center")

The next block of code uses the **warp()** method to set the warp speed to seven. Then it checks the current speed of the ship using the speed attribute.

```python
# Set warp speed
ship.warp(7)

# Check speed
ship.speed
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683021035391/76f1cf06-0103-4620-991f-346ec1ff6dce.png align="center")

This final block of code uses the **tractor()** method to toggle the tractor beam. Then it checks the current status of the tractor beam using the **tractor\_beam** attribute.

```python
# Toggle tractor beam
ship.tractor()

# Check tractor beam status
print(ship.tractor_beam)
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683032305843/26a9a871-2e07-448a-974d-36f95e5d2e06.png align="center")

# Conclusion

Python has become one of the most popular languages for data science and analysis. It offers a wide range of libraries and tools that can be used for tasks such as data manipulation, cleaning, analysis, visualization, and modeling.

Python's popularity in data science can be attributed to several factors, including its simplicity, readability, and ease of use, as well as its open-source nature and vibrant community. The availability of various libraries and frameworks such as Pandas, NumPy, Matplotlib, Scikit-learn, and TensorFlow, among others, makes it a versatile and powerful tool for data science.

Furthermore, Python is an interpreted language, which means that it is easy to write and run code quickly, making it an ideal choice for exploratory data analysis. Additionally, Python's support for functional programming, object-oriented programming, and procedural programming makes it a flexible language that can be used for various data science tasks.

In conclusion, Python is an excellent language for data science, with a rich ecosystem of tools and libraries that make it easier for data scientists to perform various tasks. Its versatility, ease of use, and strong community make it an ideal choice for data scientists and analysts.

*Thanks for Reading*

![Thanks Snake GIF - Thanks Snake Harry Potter - Discover & Share GIFs](https://media.tenor.com/m9AIU701D4QAAAAC/thanks-snake.gif align="left")