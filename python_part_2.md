# Python presentation part 2

## Abstract
  Python is a modern, easy-to-learn, object-oriented programming language. It has a powerful set of built-in data
types and easy-to-use control constructs. let us discuss about some of them in this session


## Topics 
* Modules
  * Definition
  * Standard Modules
  * The dir() Function
  * Packages
*  Errors and Exceptions
   * Definition
   * Syntax errors
   * Logical errors (Exceptions)
   * Error Handling
* Classes in Python
  * Definition
  * Defining a class
  * Class Objects
  * Declaring Objects 
  * The self
  * __init__ method
  * Class and Instance Variables


## Module 

1. ### Definition

    Module is a file consisting of Python code. A module can define functions, classes and variables. A module can also include runnable code.  
    
    in shorter way module is a file which containing the Python code and it can be impoeted to another module so that we can use it for many other pursposes like getting data from it and adding featurse ,deliting features etc.


2. ### standard modules 

    Python comes with a library of standard modules.Some modules are built into the interpreter; these provide access to operations that are not part of the core of the language but are nevertheless built in, either for efficiency or to provide access to operating system primitives such as system calls.

    some of the standard modules are 
    * math
    * sys
    * datetime
    * itertools etc

<br />

3. ### The dir() Function  

   The built-in function dir() is used to find out which names a module defines. It returns a sorted list of strings: 
        

        import math
        builtinList=dir(math)
        print(builtinList)    
        #it will return the builtin functions in this module in sorted way


4. ### packages

    A Python module may contain several classes, functions, variables, etc. whereas a Python package can contains several module. In simpler terms a package is folder that contains various modules as files.

    Packages are a way of structuring Python's module namespace by using "dotted module names". A.B stands for a submodule named B in a package named A. Two different packages like P1 and P2 can both have modules with the same name, let's say A, for example.  
<br />
    ![ Packages]()]( https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTiKrjLpnzh13Qh2yGVv7FwP94bSoQ3FBDE2Sbc6QNSuQ&s)
<br />
<br />

## Errors and Exceptions
1. ### Defination
     Errors are the problems in a program due to which the program will stop the execution. On the other hand, exceptions are raised when some internal events occur which changes the normal flow of the program. Two types of Error occurs in python. 
        

    * Syntax errors
    * Logical errors (Exceptions) 
  
<br />

2. ### Syntax errors
      When the proper syntax of the language is not followed then a syntax error is thrown.

        a=100
        print(a


3. ### Logical errors (Exceptions)
    When in the runtime an error that occurs after passing the syntax test is called exception or logical type

    for example as shown below

            a=100/0
            print(a)
            # it gives an error Zero division error

    Some of the common built-in exceptions are other than above mention exceptions are:
     * IndexError - When the wrong index of a list is retrieved.
     * AssertionError - It occurs when the assert statement fails
     * AttributeError - It occurs when an attribute assignment is failed.
     * ImportError - It occurs when an imported module is not found.
     * KeyError - It occurs when the key of the dictionary is not found.
     * NameError - It occurs when the variable is not defined.
     * MemoryError - It occurs when a program runs out of memory.
     * TypeError - It occurs when a function and operation are applied in an incorrect type.
  
<br />

4. ### Error Handling
   When an error and an exception are raised then we handle that with the help of the Handling method.
    * Handling Exceptions with Try/Except/Finally. We can handle errors by the Try/Except/Finally method. we write unsafe code in the try, fall back code in except and final code in finally block.

                try:
                    a=10/0
                    print(a)  
                #if error occur the it goes in except block
                except:
                    print("an error occurs")
                
                #final code in finally block
                finally:
                    print("ok")
                    
    * Raising exceptions for a predefined condition 
        - When we want to code for the limitation of certain conditions then we can raise an exception

                try:
                    score = 50
                    if amount < 35:   
                        # raise the ValueError
                        raise ValueError("You are not eligible")
                    else:
                        print("You are eligible")            
                # if false then raise the value error
                except ValueError as e:
                        print(e)
                        
     <br />                
## Classes 


1. Defination

   Python is an object oriented programming language.Almost everything in Python is an object, with its properties and methods.A Class is like an object constructor, or a "blueprint" for creating objects.
   
   in shorter way a class is a blue print of the project


    Some points on Python class:  

    * Classes are created by keyword class.
    * Attributes are the variables that belong to a class.
    * Attributes are always public and can be accessed using the dot (.) operator.                  
   Eg.: Myclass.Myattribute


<br />

2. Defining a class

   he class keyword indicates that you are creating a class followed by the name of the class (Dog in this case).

        class Dog:
            pass

    <br />
 3. Class Objects
   
    An Object is an instance of a Class. A class is like a blueprint while an instance is a copy of the class with actual values.it consist of 

       * State: It is represented by the attributes of an object. It also reflects the properties of an object.
       * Behavior: It is represented by the methods of an object. It also reflects the response of an object to other objects.
       * Identity: It gives a unique name to an object and enables one object to interact with other objects.

<br />

4. Declaring Objects  

    When an object of a class is created, the class is said to be instantiated. All the instances share the attributes and the behavior of the class. But the values of those attributes, i.e. the state are unique for each object. A single class may have any number of instances.

    [![ Declaring objects]()]( https://media.geeksforgeeks.org/wp-content/uploads/Blank-Diagram-Page-1-3.png)

        class Dog:
            
            # A simple class attribute
            attr1 = "mammal"
            attr2 = "dog"
        
            # A sample method 
            def fun(self):
                print("I'm a", self.attr1)
                print("I'm a", self.attr2)

        # Object instantiation
        Rodger = Dog()
        
        # Accessing class attributes and calling method through objects
        print(Rodger.attr1)
        Rodger.fun()

    In the above example, an object is created which is basically a dog named Rodger. This class only has two class attributes that tell us that Rodger is a dog and a mammal

5. The self 

    - Class methods must have an extra first parameter in the method definition. We do not give a value for this parameter when we call the method, Python provides it.
    - If we have a method that takes no arguments, then we still have to have one argument.
    - This is similar to this pointer in C++ and this reference in Java.

<br />

6.  `__init__` method

    The `__init__` method is similar to constructors in C++ and Java. Constructors are used to initializing the object’s state. Like methods, a constructor also contains a collection of statements(i.e. instructions) that are executed at the time of Object creation. It runs as soon as an object of a class is instantiated. The method is useful to do any initialization you want to do with your object.

6. Class and Instance Variables

    Instance variables are for data, unique to each instance and class variables are for attributes and methods shared by all instances of the class. foe example 

        class Dog:
    
        # Class Variable
        animal = 'dog'            
    
        # The init method or constructor
        def __init__(self, breed, color):
        
            # Instance Variable    
            self.breed = breed
            self.color = color       
            
        # Objects of Dog class
        Rodger = Dog("Pug", "brown")
        Buzo = Dog("Bulldog", "black")

        # print(Rodger.breed)
        # print(Dog.animal)  



<br />

#  Thank You
