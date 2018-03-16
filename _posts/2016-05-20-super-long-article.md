---
layout: post
title: "PythonII Project"
categories: misc
---

## Overview:

This PythonII Project is a code that uses the application python to run a simple fortune teller. Using a function certain inputs create a custom function. The user gets to repond to things such as if they woke up before 8 A.M. simply responding "Y" (for yes) or "N" (for no). Then from there, there is a specific output for that input.

## The code:

```python
#Fortune Teller

#Function Library
import random
import sys
import time


  
#Ask the user for their first name and if they want their fortune.
print('What is your first name?')
userName = input()
print('Would you like to know your fortune, ' + userName +'? (Y = yes/N = no)')
userYN = str(input())

#if user says yes ask for their birth month if no quit the program.
if userYN == 'Y':
    print('What is your birth month, '+ userName + '?')
    print('(ex. 1 = January)')
else:
    sys.exit("Well I didn't want to give you a fortune "+ userName +'!')

#Store the users birth month and ask for the day of the month.
userBirthMonth = int(input())
print('What is the day you were born on ' + userName + '?')
print('(ex. 1 = First day of the month)')
userBirthDay = int(input())

#Ask the user for a significant person in their life and what their birth month is.
print('What is the birth month of someone significant in your life?') 
print('(ex. 1 = January)')
sigBirthMonth = int(input())

#Find out the significant person's birth day.
print('What day were they born on?')
print('(ex. 1 = First day of the month)')
sigBirthDay = int(input())

#Find out the significant person's name.
print('What is their name?')
sigName = input()

#Ask the user for their height.
print('What is your height in inches?')
userHeight = int(input())

#Ask the user to choose a color from either red, blue, or green.
print('Pick from these two colors: Red and Blue')
print('(R = Red and B = Blue)')
userColor = str(input())

#Declare R and B.
R = ('determination')
B = ('intelligence')

#Use an if statement to output either R or B.
if userColor == 'R':
  userColor = R
elif userColor == 'B':
  userColor = B

#Ask the user if they woke up before 8 AM.
print('Did you wake up before 8 A.M. this morning? (Y = yes/N = no)')
userWakeUp  = str(input())

#Declare Y and N.
Y = ('you that you\'re an early bird')
N = ('that you like to sleep a lot')

#Use an if statement to output the Y or N.
if userWakeUp == 'Y':
  userWakeUp = Y
elif userWakeUp == 'N':
  userWakeUp = N

#Separate the questions from the lucky number and delay the separations by 0.5 seconds.
time.sleep(0.5)
print('\n*****************************************************************')
print('*****************************************************************\n')

#From the results, determine a lucky number for the user and display it plus delay the result by 0.5 seconds.
luckyNumber = str((userHeight * sigBirthDay)//(userBirthDay + userBirthMonth))
time.sleep(0.5)
print('Your lucky number is: ' + luckyNumber + '\n')

#Separate the lucky number from the fortune and delay it by 0.5 seconds.
time.sleep(0.5)
print('*****************************************************************\n')

#Determining the birthflower using an if-else if statement.
if userBirthMonth == 1:
  birthFlower = ('carnation')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find love in the near future.')
elif userBirthMonth == 2:
  birthFlower = ('primrose')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find virtue in the near future.')
elif userBirthMonth == 3:
  birthFlower = ('daffodil')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will be reborn in the near future.')
elif userBirthMonth == 4:
  birthFlower = ('sweet pea')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find blissful pleasure in the near future.')
elif userBirthMonth == 5:
  birthFlower = ('hawthorn')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find happiness in the near future.')
elif userBirthMonth == 6:
  birthFlower = ('rose')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find appreciation in the near future.')
elif userBirthMonth == 7:
  birthFlower = ('water lily')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find fickleness in the near future.')
elif userBirthMonth == 8:
  birthFlower = ('poppy')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find moral integrity in the near future.')
elif userBirthMonth == 9:
  birthFlower = ('morning glory')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find daintiness food in the near future.')
elif userBirthMonth == 10:
  birthFlower = ('calendula')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find protection in the near future.')
elif userBirthMonth == 11:
  birthFlower = ('chrysanthemum')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and you will find a friendship in the near future.')
elif userBirthMonth == 12:
  birthFlower = ('holly')
  birthFlower = ('. Your birth flower is the ' + birthFlower + ' and your self-esteem will rise in the near future.')

#Declare variables for userHeight above 60 inches, and equal to or below 60 inches.
if userHeight <= 60:
  userHeight = ('You may be only ' + str(userHeight) + ' inches tall, but don\'t let that put you down because it will help you in the upcoming days')
elif userHeight > 60:
  userHeight = ('You are ' + str(userHeight) + ' inches tall, your height will help you succeed in the upcoming days')

#Create a function that uses the variables/inputs userWakeUp, userColor, userHeight, and birthFlower.
def userFortune(userWakeUp, userColor, userHeight, birthFlower):
  if userBirthMonth >= 1:
    print('The people in your life will tell ' + str(userWakeUp) + '. You will have the ' + str(userColor) + ' in your future to achieve your goals. ' + str(userHeight) + birthFlower + '\n\n P.S. ' + sigName + ', will have the answers to your questions if you look close enough.')
    

#Tell the user their custom fortune by calling the function userFortune
userFortune(userWakeUp, userColor, userHeight, birthFlower)

#Separate the function call from thanking the user and delay the separations by 0.5 seconds.
time.sleep(0.5)
print('\n*****************************************************************\n')

#Thank user and use their name to say goodbye.
print('Thank you, ' + userName + ', for using the fortune teller! Goodbye.')

#Close off thanking the user and delay the separations by 0.5 seconds.
time.sleep(0.5)
print('\n*****************************************************************')
print('*****************************************************************')
```
