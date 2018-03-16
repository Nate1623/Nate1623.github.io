---
title: PythonIII Project
layout: post
---

## Overview:

This is my PythonIII project which uses the turtle function to create a drawing.

## Code:
```python
#imports the turtle function.
import turtle

#creates a turtle to draw.
t = turtle.Turtle()


#function to create a star.
def star(n):
  while (n < 7):
    t.forward(100)
    t.right(135)
    n = n+1

#creates a visual composition using the inputs starColor, squareColor, squareColor2, squareSize, and squareSize2.
#starColor changes the star color.
#squareColor changes the square color that surrounds the starColor.
#squareColor2 changes the color of the biggest square choose either purple or yellow.
#squareSize changes the pen size width for the square surrounding the star.
#squareSize2 changes the pen size of the biggest square.
def create_visual_composition(starColor, squareColor, squareColor2, squareSize, squareSize2):
    t.color(starColor)
    star(-1)
    t.color(squareColor)
    t.pensize(squareSize)
    t.penup()
    t.left(90)
    t.forward(30)
    t.right(90)
    t.pendown()
    t.forward(100)
    t.right(90)
    t.forward(100)
    t.right(90)
    t.forward(100)
    t.right(90)
    t.forward(100)
    t.right(90)
    t.left(45)
    t.color(squareColor2)
    t.pensize(squareSize2)
    t.forward(70)
    t.right(90)
    t.forward(70)
    t.forward(70)
    t.right(90)
    t.forward(140)
    t.right(90)
    t.forward(140)
    t.right(90)
    t.forward(70)
#If squareColor2 is purple then make the next square yellow.
    if squareColor2 == "purple":
      t.left(90)
      t.penup()
      t.color("yellow")
      t.forward(25)
      t.right(135)
      t.pendown()
      t.pensize(5)
      t.forward(140)
      t.right(90)
      t.forward(140)
      t.right(90)
      t.forward(140)
      t.right(90)
      t.forward(140)
#If squareColor2 is yellow then make the next square purple.
    elif squareColor2 == "yellow":
      t.left(90)
      t.penup()
      t.color("purple")
      t.forward(25)
      t.right(135)
      t.pendown()
      t.pensize(5)
      t.forward(140)
      t.right(90)
      t.forward(140)
      t.right(90)
      t.forward(140)
      t.right(90)
      t.forward(140)
    

create_visual_composition("red", "black", "yellow", 7, 10)
```
