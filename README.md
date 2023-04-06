# Markdown-Assignment
Notes on what we have learned in the OOP assignment 

OOP 1
Object: 
Collection of methods (objects’s code) and variables
An instance of a class

Object can have both attributes (characteristics) and methods (what can the object do?)

Class:

Contains attributes for object or for itself. Easily accessible if not encapsulated
Methods are the functions of the object that it can call on



Object Oriented Programming (OOP):
Designs programs which creates Objects
Focuses more on the interpretation of data rather than using logic for its functionality
Programs are reusable

Ex. 
Class Elephant:
	def __init__ (self, name, ears):
		#self parameter used to refer to this instance
		self.name = name
		self.ears = ears
		#our attributes

	def walk():
		print(self.name, ‘is walking’)
	#method, function that it can call on

elephant1 = Elephant(‘dumbo, ‘floppy ears’)
elephant1.walk()
Encapsulation:
Information Hiding: Restricting the access to the classes/object’s certain attributes and methods.
Two underscores in the front mean encapsulation (prefix) → cannot access them outside
Objects that are not encapsulated can be modified outside of the class definition 

What is self?:
Self represents the instance of class
It is a keyword used to access attributes and methods of the class in Python
Treat its own attributes as local (variables declared inside the function/block, not accessible outside of function)

OOP 2
__init__:

Initialization method is used as soon as an object is created
Used to create object’s attributes

__Encapsulation (two underscore prefixes):
Makes the classes/objects attributes and methods inaccessible
Used for data protection

Ex. 
class Elephant:
	def __init__ (self, name, ears):
		#self parameter used to refer to this instance
		self.name = name
		self.__ears = ears
		#our attribute, self.__ears is encapsulated

	def __setEars(self, earlobe):
		Self.__ears = earlobe

	#resetting variable
	def getEars(self):
		return self.__ears
	#gets encapsulated variable
	def walk():
		print(self.name, ‘is walking’)
	#method, function that it can call on


Common Practice:
Setter and getter (used with encapsulated values)
Setter and getter used to update values
Without this, you can’t access the information

Polymorphism
Overloading: Two methods in one class that have the same method name, but different arguments (not possible in Python)
Both have different behaviours, but same method type

Overriding: Two methods with the same method name and parameters
However, they are in different areas
One method being in the parent class
The other being in the child class (but it acts differently in the child class)
Benefits:
Can complete mathematical operations on Objects
Can compare equality between Objects

Polymorphism: A method that can be used across different classes and object that is dependent on the parameters. Same named method, but different kinds of outputs. 
I.e. index()
Same named method, but in two different classes

Ex. 

class Dog:

	def sound(self):
		print(‘woof!’)
class cat

	def sound(self):
		print(‘meow’)

Double under-score as both prefix and suffix is a base override. Controlling that something that already exists in Python 
__repr__ allows us to present a printable version of our object
__str__ allows us to convert our object to a string

What is % for string formatting?:


(format string) % (values)
Ex. print(“Hello, my name is %s.” % “Graham”)
Hello, my name is Graham
 
Only attributes should be made during initialization

On the test, unless specified, you don’t have to encapsulate
On an assignment, do encapsulation to prove skills

OOP 3

Inheritance: when an object or class is based on another class; where its features are passed down from a parent class
Various types of inheritance
Single (inheritance from a single superclass), multiple (inheriting features from multiple parents), multilevel inheritance (grandparents)
Can also have a tree (like a family tree)
Child will receive all attributes and methods from the parent class
They can override the attributes/methods to their own liking
IMPORTANT NOTES: the child does not need another __init__() method unless it needs new attributes 
You also don’t need to restate the parent’s methods unless you decide to override them
super() is a method to refer to the parent class

How to do:

class Parent:
	pass
class Child(Parent):
	def __init__(self, param, param2):
parent.__init__(self, param) #can use super() here instead
self.param2 = param2
#inheritance

OOP 4

Iterable Objects:

The portion of the iterable object must be a sequence
Not necessarily indexable


__iter__() allows our object to be iterable
__next__() allows us to get the next value when iterating 
Common practice:
Setting an index attribute to -1
Add 1 to the index attribute by 1 until self.__index is equal to the length of the sequence
Once it reaches this point, we say raise StopIteration

def __iter__(self):
	return self

def __next__(self):
	self.__index += 1
	if self.__index == len(self.__cards):
		Self.__index = -1 #index rest
		raise StopIteration
	else:
		return self.__cards[self.__index]






