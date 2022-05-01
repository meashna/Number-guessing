# Number-guessing
import random

flag = True 
while flag:
    num = input("Type a number greater than 1: ")

    if num.isdigit():
        print("Lets play!!!")
        num = int(num)
        flag = False
    else:
        print("Try again")

secret = random.randint(1 , num)
        
guess  = None
count = 0

while guess != secret:
    guess = input("please type a number between 1 and " + str(num) + ":") 
    if guess.isdigit():
        guess = int(guess)


    if guess == secret:
        count +=1
        print("You guessed the number in", count, "attempts" "\nCongrats😍")

    else:
        count += 1
        print(" Oops ! Trry again . It took you", count, "guesses.2")
