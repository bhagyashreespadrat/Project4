# Project4
#Simple guessing number game in python
# Label program
# author:Bhagyashree
# Location:Pune
# Date:17/11/2020
#Simple guessing number game in python
#completed sucessfully

import random
randNumber=random.randint(1,10)
userguess=None
guesses=0
while(userguess!=randNumber):
    userguess=int(input("Enter your guess:"))
    guesses+=1
    if(userguess==randNumber):
        print("you guessed it right!")
    else:
        if(userguess>randNumber):
            print("you guessed it wrong! enter smaller number")
        else:
            print("you guessed it wrong ! enter larger number")
print(f"you guessed the number in:{guesses} times")
with open("hiscore.txt","r")as f:
    hiscore=int(f.read())
if(guesses<hiscore):
    print("you have just broken the high score!")
    with open("hiscore.txt","w")as f:
        f.write(str(guesses))
'''#OUTPUT:
Enter your guess:8
you guessed it wrong! enter smaller number
Enter your guess:7
you guessed it wrong! enter smaller number
Enter your guess:6
you guessed it wrong! enter smaller number
Enter your guess:5
you guessed it wrong! enter smaller number
Enter your guess:4
you guessed it wrong! enter smaller number
Enter your guess:3
you guessed it wrong! enter smaller number
Enter your guess:2
you guessed it wrong! enter smaller number
Enter your guess:1
you guessed it right!
you guessed the number in:8 times'''
