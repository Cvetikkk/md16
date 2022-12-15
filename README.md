# md16
#1 фаил

import scipy


class Rectangle:
    def __init__(self,a,b):
        self.a = a
        self.b = b
    def get_area(self):
        return self.a * self.b
class Square:
    def __init__(self,a):
        self.a = a
    def get_area_square(self):
        return self.a ** 2
class Circle:
    def __init__(self,a):
        self.a = a
    def get_area_circle(self):
        return (scipy.pi * (self.a ** 2))
       
 #2 фаил
 
from main2 import Rectangle, Square, Circle

rect1 = Rectangle(7,44)
# print(rect1.get_area())

squar = Square(11)
print(squar.get_area_square(),
        rect1.get_area())

cir = Circle(2)
print(cir.get_area_circle())

figures = [rect1,squar, cir]
for figure in figures:
        if isinstance(figure,Square):
                print(figure.get_area_square())
        elif isinstance(figure, Rectangle):
                print(figure.get_area())
        else:
                print(figure.get_area_circle())
