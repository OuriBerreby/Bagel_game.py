# Bagel_game.py

import random

guess_number = random.randint(100,1000)
guess_number =  str(guess_number)
print(guess_number)

tour = 1
play = 1

while(play == 1):
    print("I have thought up a number.\nYou have 10 guesses to get it.")
    while tour < 11:
       
        my_guess = str(input("Guess: {}\n> ".format(tour)))
        if my_guess == guess_number:
            print("You got it!")
            break
   
        isInclude = 0
        for index in range(len(my_guess)):
            for index2 in range(len(guess_number)):
                if my_guess[index] == guess_number[index]:
                    isInclude = 1
                    print("Fermi")
                    break
                if my_guess[index] == guess_number[index2]:
                    print("Pico")
                    isInclude = 1
                    break
    
        if isInclude == 0:
            print("Bagels")

        tour += 1
    
    
    if tour > 10:
        print("You use all your chance!")

    print("Want to play again ?\t1- Yes\t2-No")
    user_choice = input() 
    if user_choice == 1:
        play = 1
        tour = 1
    if user_choice == 2:
        play = 0

exit
