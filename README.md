# Python oop


### step 1

````
# create an animal class
# syntax is class name:

class Animal:

    # __init__ to declare class attribute

    def __init__(self): # self refers current class
        self.alive = True
        self.spine = True

    def sleep(self):
        return "8 hrs sleep is advised"

    def eat(self):
        return "eat if you like to stay alive.. eat healthy"

# create an object of the class before using it
cat= Animal()

print(cat.eat())   # call method from the class, abstracted how                     was eat created or what info is available

#print(cat.alive)

````


### Step 2- Inheritance

# Inherit everything from Animal class into reptile file
from animal import Animal

# create a reptile class

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

# create an object of reptile class

reptile_object = Reptile()

#print(reptile_object.eat())
#print(reptile_object.hunt())
````


## Step-3 

# Inherit reptile from Reptile class


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

