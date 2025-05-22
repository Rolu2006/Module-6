# EX-21-Polymorphism
## AIM:
To Create two classes Cat and Dog with functions mood() and sound() which are same for both the classes yet they produce distinct outputs. iterate over the objects of the two classes “Cat” and “Dog” without worrying about the class types

## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
Step 1: Define class Cat with two methods: mood() printing "Grumpy" and sound() printing "Meow".

Step 2: Define class Dog with two methods: mood() printing "Happy" and sound() printing "Woof".

Step 3: Create an object hello_kitty of class Cat and hello_puppy of class Dog.

Step 4: Store both objects in a tuple.

Step 5: Loop through each object, calling the mood() and sound() methods to demonstrate behavior based on object type.


## PROGRAM:
```
class Cat:
    def mood(self):
        print("Grumpy")
    def sound(self):
        print("Meow")
 
class Dog:
    def mood(self):
        print("Happy")
    def sound(self):
        print("Woof")
 
hello_kitty = Cat()
hello_puppy = Dog()
 
for pet in (hello_kitty, hello_puppy):
    pet.mood()
    pet.sound()
```
## OUTPUT:




![Screenshot 2025-05-23 000217](https://github.com/user-attachments/assets/346f2c9d-8b9e-4fb1-93f5-357314e4ed6e)


## RESULT:
Thus the program to Create two classes Cat and Dog with functions mood() and sound() which are same for both the classes yet they produce distinct outputs. iterate over the objects of the two classes “Cat” and “Dog” without worrying about the class types has been executed successfully.

# EX-22-Operator Overloading
## AIM:
To write a python program to overload less than operator 

class name should be A

ob1 = A(20)

ob2 = A(3)

## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
Step 1: Define class A with an __init__ method to initialize a value a for each object.

Step 2: Define method less() in class A to return the object's stored value a.

Step 3: Create two instances: ob1 with value 20, and ob2 with value 3.

Step 4: Use the less() method to get values from both objects into variables a and b.

Step 5: Compare a and b, then print which object has the smaller value.


## PROGRAM:
```
class A:
    def __init__(self,a):
        self.a=a
    def less(self):
        return self.a
ob1 = A(20)
ob2 = A(3)
a=ob1.less()
b=ob2.less()
if a>b:
    print("ob2 is less than ob1")
else:
    print("ob1 is less than ob2")
```
## OUTPUT:




![Screenshot 2025-05-23 000440](https://github.com/user-attachments/assets/25e77901-1c42-4db2-8e6c-15b46d90cb8d)


## RESULT:
Thus the program write a python program to overload less than operator 

class name should be A

ob1 = A(20)

ob2 = A(3)

has been successfully executed.
# EX-23-Abstraction
## AIM:
To Create an abstract class Invoice, and abstract method invoice () under def statement also has two child class derived from Invoice and does the functionality. Then, using an Object ‘aa’, the methods are invoked.
## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
Step 1: Import ABC and abstractmethod from abc and define an abstract class Invoice with a concrete method final_bill() and an abstract method Invoice().

Step 2: Create subclass paycheque that implements the abstract Invoice() method to print a cheque payment message.

Step 3: Create subclass CardPayment that implements the abstract Invoice() method to print a card payment message.

Step 4: Instantiate objects aa of paycheque and CardPayment, call their Invoice() and final_bill() methods with payment amounts.

Step 5: Use isinstance() to verify that the objects are instances of the abstract base class Invoice.


## PROGRAM:
```
from abc import ABC, abstractmethod
class Invoice(ABC):
    def final_bill(self, pay):
        print('Purchase of the product- ', pay)
    @abstractmethod
    def Invoice(self,pay):
        pass
class paycheque(Invoice):
    #Define a invoice function
    def Invoice(self,pay):
        print("paycheque of- ",pay)
class CardPayment(Invoice):
    #Define a invoice function
    def Invoice(self,pay):
        print("pay through card of- ",pay)
aa = paycheque()
aa.Invoice(6500)
aa.final_bill(6500)
print(isinstance(aa,Invoice))
aa = CardPayment()
aa.Invoice(2600)
aa.final_bill(2600)
print(isinstance(aa,Invoice))
```
## OUTPUT:





![Screenshot 2025-05-23 000801](https://github.com/user-attachments/assets/c3b948d2-56a4-45ec-b71d-5d6d2d0a2aa4)


## RESULT
Thus the program to Create an abstract class Invoice, and abstract method invoice () under def statement also has two child class derived from Invoice and does the functionality. Then, using an Object ‘aa’, the methods are invoked has been successfully executed.
 # EX-24-Encapsulation
 # (A)
 ## AIM:
 To Create a Class  Student with the private members name and age ,Add getter and setter to initialize the age variable.
 ## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
Step 1: Define a class Student with private attributes __name and __age initialized via the constructor.

Step 2: Create getter methods get_name() and get_age() to access private variables.

Step 3: Create a setter method set_age() to modify the private attribute __age.

Step 4: Instantiate a Student object with name and age.

Step 5: Use getter methods to print the name and age, then update age with setter, and print updated values again.
## PROGRAM:
```
class Student:
    def __init__(self, name, age):
        # private member
        self.name = name
        self.__age = age

    # getter method
    def get_name(self):
        return self.__name
    def get_age(self):
        return self.__age
    # setter method
    def set_age(self,age):
        self.__age=age

stud = Student('Jessa', 14)

# retrieving age using getter
print('Name:', stud.name, stud.get_age())

# changing age using setter
stud.set_age(16)
# retrieving age using getter
print('Name:', stud.name, stud.get_age())
```
## OUTPUT:




![Screenshot 2025-05-23 001048](https://github.com/user-attachments/assets/03939aaa-f5d8-415c-af22-07b9b78347cf)


## RESULT:
 Thus the program to Create a Class  Student with the private members name and age ,Add getter and setter to initialize the age variable has been executed successfully.

 # (B)
 ## AIM:
 To Create a class Car with the private variables max_speed,name change the value of a private variable, Use a setter method  setMaxSpeed(). create an object of the class to invoke the methods
 ## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
Step 1: Define a class Car with private class attributes __maxspeed and __name.

Step 2: Initialize instance variables __maxspeed to 200 and __name to "Supercar" in the constructor __init__().

Step 3: Define a method drive() that prints the current __maxspeed.

Step 4: Define a method setMaxSpeed(spd) to update the private __maxspeed attribute.

Step 5: Create a Car object redcar, call drive(), then update max speed to 320 with setMaxSpeed(), and call drive() again.
## PROGRAM:
```
class Car:

    __maxspeed = 0
    __name = ""
    
    def __init__(self):
        self.__maxspeed = 200
        self.__name = "Supercar"
    
    def drive(self):
        print('driving. maxspeed ' + str(self.__maxspeed))

    def setMaxSpeed(self,spd):
        self.__maxspeed=spd
redcar = Car()
redcar.drive()
redcar.setMaxSpeed(320)#change the maxspeed as 320
redcar.drive()
```
## OUTPUT:





![Screenshot 2025-05-23 001253](https://github.com/user-attachments/assets/62ecfb35-78e8-4add-8895-c4472c6dc97d)


## RESULT:
 
 Thus the program to Create a class Car with the private variables max_speed,name change the value of a private variable, Use a setter method  setMaxSpeed(). create an object of the class to invoke the methods has been executed successfully.
