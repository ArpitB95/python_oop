## What is oop (Object orient programing) ?
- Object-oriented programming (OOP) is a computer programming model that organizes software design around data, or objects, rather than functions and logic. An    object can be defined as a data field that has unique attributes and behavior.

- OOP focuses on the objects that developers want to manipulate rather than the logic required to manipulate them. This approach to programming is well-suited for programs that are large, complex and actively updated or maintained. This includes programs for manufacturing and design, as well as mobile applications; for example, OOP can be used for manufacturing system simulation software

## There are four pillars of python oop:
Encapsulation.
Inheritance.
Polymorphism.
Abstraction.

1) Abstraction:
2) Inheritance
3) Encapsulation 
4) Polymorphism






# Python oop - task

<img width="422" alt="Animal_example" src="https://user-images.githubusercontent.com/110182832/182913131-c81d46ef-2b80-4755-a119-9a9dea6010ee.png">


## Steps to follow:
- Create a new project on pycharm
- Create new github repo called python_oop
- Create a README.md in pycharm
- Create a file called animal.py (if this works do abstraction)
- Create a file called reptile.py and inherit Animal (key words used - super class, init)
- Create a file called snake.py and inherit reptile ( do encapsulation)
- Create a file called python.py and inherit snake (do polymorphism)


### step 1

````
### create an animal class
### syntax is class name:

class Animal:

    # __init__ to declare class attribute

    def __init__(self): # self refers current class
        self.alive = True
        self.spine = True

    def sleep(self):
        return "8 hrs sleep is advised"

    def eat(self):
        return "eat if you like to stay alive.. eat healthy"

### create an object of the class before using it
cat= Animal()

print(cat.eat())   ### call method from the class, abstracted how    was eat created or what info is available

print(cat.alive)

````


### Step 2- Inheritance

### Inherit everything from Animal class into reptile file
from animal import Animal

### create a reptile class

````
class Reptile(Animal):  # write the name of the class in (parent-class) to inherit

    # parent class- base class, super class

    def __init__(self):
        # to let it know to inherit everything from parent class (Animal)

        super().__init__() # super is used to inherit everything from base class
        self.cold_blooded = True
        self.heart_chambers = [3,4]

    def seek_heat(self):
        return "looking for the sunshine"

    def hunt(self):
        return "working hard to catch a next meal"

### create an object of reptile class

reptile_object = Reptile()

print(reptile_object.eat())
print(reptile_object.hunt())
````


## Step-3 

### Inherit reptile from Reptile class


````
from reptile import Reptile

class Snake(Reptile):

    def __init__(self):
        super().__init__()

        self.forked_tongue = True

    def use_tongue_to_smell(self):
        return "I can use tongue to smell food"
        # pass # if you don't need to print statement or you don't have to pass message


snake_object = Snake()

print(snake_object.eat()) # this function is inherited from animal
print(snake_object.seek_heat()) # this function is inherited from Reptile class
print(snake_object.use_tongue_to_smell()) # this function is inherited from Snake class
````

## Step-3- Capsulation

### Inherit reptile from Reptile class

````
from reptile import Reptile

class Snake(Reptile):

    def __init__(self):
        super().__init__()

        self.forked_tongue = True
        self.danger = True
        self._canfly = False
        self.__speedy = True



    def use_tongue_to_smell(self):
        return "It can use tongue to smell food"

    def _hiss(self):
        return "hissss"

    def __speaks(self):
        return "no"


        ### pass- if you don't need to print statement or you don't have to pass message


snake_object = Snake()



# print(snake_object.eat()) # this function is inherited from animal
# print(snake_object.seek_heat()) # this function is inherited from Reptile class
# print(snake_object.use_tongue_to_smell()) # this function is inherited from Snake class
print(snake_object.danger)
print(snake_object._canfly)
print(snake_object._hiss())

````
