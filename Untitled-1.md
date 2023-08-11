11.What is the use of self in Python?
Self is used to represent the instance of the class. With this keyword, you can access the attributes and methods of the class in python. It binds the attributes with the given arguments. self is used in different places and often thought to be a keyword. But unlike in C++, self is not a keyword in Python.

12. What is init?

init is a contructor method in Python and is automatically called to allocate memory when a new object/instance is created. All classes have a init method associated with them. It helps in distinguishing methods and attributes of a class from local variables.

class definition
class Student: def init(self, fname, lname, age, section): self.firstname = fname self.lastname = lname self.age = age self.section = section

creating a new object
stu1 = Student("Sara", "Ansh", 22, "A2")

 13.What is break, continue and pass in Python?
 Break The break statement terminates the loop immediately and the control flows to the statement after the body of the loop. Continue The continue statement terminates the current iteration of the statement, skips the rest of the code in the current iteration and the control flows to the next iteration of the loop. Pass As explained above, the pass keyword in Python is generally used to fill up empty blocks and is similar to an empty statement represented by a semi-colon in languages such as Java, C++, Javascript, etc.
pat = [1, 3, 2, 1, 2, 3, 1, 0, 1, 3] for p in pat: pass if (p == 0): current = p break elif (p % 2 == 0): continue print(p) # output => 1 3 1 3 1 print(current) # output => 0

 14.What are unit tests in Python?

Unit test is a unit testing framework of Python. Unit testing means testing different components of software separately. Can you think about why unit testing is important? Imagine a scenario, you are building software that uses three components namely A, B, and C. Now, suppose your software breaks at a point time. How will you find which component was responsible for breaking the software? Maybe it was component A that failed, which in turn failed component B, and this actually failed the software. There can be many such combinations. This is why it is necessary to test each and every component properly so that we know which component might be highly responsible for the failure of the software.

 15.What is docstring in Python?

Documentation string or docstring is a multiline string used to document a specific code segment. The docstring should describe what the function or method does.

16.What is slicing in Python?

As the name suggests, ‘slicing’ is taking parts of. Syntax for slicing is [start : stop : step] start is the starting index from where to slice a list or tuple stop is the ending index or where to sop. step is the number of steps to jump. Default value for start is 0, stop is number of items, step is 1. Slicing can be done on strings, arrays, lists, and tuples.

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] print(numbers[1 : : 2]) #output : [2, 4, 6, 8, 10]

Explain how can you make a Python Script executable on Unix?



 17.What is the difference between Python Arrays and lists?

Arrays in python can only contain elements of same data types i.e., data type of array should be homogeneous. It is a thin wrapper around C language arrays and consumes far less memory than lists. Lists in python can contain elements of different data types i.e., data type of lists can be heterogeneous. It has the disadvantage of consuming large memory.

import array a = array.array('i', [1, 2, 3]) for i in a: print(i, end=' ') #OUTPUT: 1 2 3 a = array.array('i', [1, 2, 'string']) #OUTPUT: TypeError: an integer is required (got type str) a = [1, 2, 'string'] for i in a: print(i, end=' ') #OUTPUT: 1 2 string

Python Interview Questions for Experienced
 18.. How is memory managed in Python?

Memory management in Python is handled by the Python Memory Manager. The memory allocated by the manager is in form of a private heap space dedicated to Python. All Python objects are stored in this heap and being private, it is inaccessible to the programmer. Though, python does provide some core API functions to work upon the private heap space.
Additionally, Python has an in-built garbage collection to recycle the unused memory for the private heap space.

 19.What are Python namespaces? Why are they used?
A namespace in Python ensures that object names in a program are unique and can be used without any conflict. Python implements these namespaces as dictionaries with 'name as key' mapped to a corresponding 'object as value'. This allows for multiple namespaces to use the same name and map it to a separate object. A few examples of namespaces are as follows:

Local Namespace includes local names inside a function. the namespace is temporarily created for a function call and gets cleared when the function returns.
Global Namespace includes names from various imported packages/ modules that are being used in the current project. This namespace is created when the package is imported in the script and lasts until the execution of the script.
Built-in Namespace includes built-in functions of core Python and built-in names for various types of exceptions.
The lifecycle of a namespace depends upon the scope of objects they are mapped to. If the scope of an object ends, the lifecycle of that namespace comes to an end. Hence, it isn't possible to access inner namespace objects from an outer namespace. 

20.What is pass in Python?
The pass keyword represents a null operation in Python. It is generally used for the purpose of filling up empty blocks of code which may execute during runtime but has yet to be written. Without the pass statement in the following code, we may run into some errors during code execution.
