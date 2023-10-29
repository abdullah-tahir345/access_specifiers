# access_specifiers

In Python, access specifiers are used to control the visibility and accessibility of class attributes and methods. Python uses a naming convention rather than explicit access specifiers like some other programming languages (e.g., public, private, protected). Here are the common access specifiers used in Python:

1. Public (No Prefix):
   In Python, all class attributes and methods are public by default, which means they can be accessed from outside the class.
   Public variables access anywhere in the program. Like

       print(object_class.public_variable) #This will not show any error but show th value of this variable
       object_class.public_variable == 'set_value' #This will not throw any error but override the value

3. Private (Double Underscore Prefix: "__"):
   By prefixing an attribute or method name with a double underscore, you indicate that it's private. However, it's worth noting that Python performs name mangling to make it difficult, but not impossible, to access these attributes from outside the class.
   Accessing the private variables outside the class will throw the error. Like

       print(object_class.__private_variable) #This will throw an error because private variable are not accessible outside the class and this is the binding of data. So, it's called encapsulation.
       object_class.__private_variable == 'set_value' #This will also throw an error because private variables are not override

4. Protected (Single Underscore Prefix: "_"):
   Attributes and methods prefixed with a single underscore are considered "protected" by convention. It's a signal to other programmers not to access them directly, but Python doesn't enforce this restriction.
   Protected variables access anywhere in the code but it's only useable in the derived class. Like

       print(object_class._protected_variable) #This will not show any error but show th value of this variable
       object_class._protected_variable == 'set_value' #This will not throw any error but override the value
