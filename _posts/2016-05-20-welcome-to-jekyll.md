---
title: PythonI Project 
layout: post
---

## Overview:

This is just a guessing game that I created for the PythonI project.

## Code:
```python
#Guess a number between 1-10 game

#Function Library
import random
import sys
import time

#Tell the user to choose a number between 1-10
print("Try to guess a number between 1-10!")
userInput = int(input())

#if the user chooses a number outside of the range quit the program
if userInput >= 11 or userInput <= 0:
  sys.exit("That isn't inbetween 1-10!")

#print what the user typed in
print("You chose the number, ", userInput)
time.sleep(0.5)
print(".")
time.sleep(0.5)
print(".")
time.sleep(0.5)

#declare a variable for the computer for a number between 1-10
computerNum = random.randint(0,10)

#Tell the user if they chose the right number
if userInput == computerNum:
    print("You guessed the right number!")
else:
    print("You guessed the wrong number..")
```
