# Guess My Number
#
# The computer picks a random number between 1 and 100
# The player tries to guess it and the computer lets
# the player know if the guess is too high, too low
# or right on the money

import random
print("\tWelcome to 'Guess my Number Game'!")
print ("\nI'm thinking of a number between 1 and 100.")
print ("Try to guess it in as few attempts as possible.\n")

# set the initial values
the_number = random.randrange(1, 100) + 1
guess = int(input ("Guess the number"))
tries = 1
#Guessing loop
while(guess!= the_number):
    if (guess > the_number):
        print ("Try to Guess Lower...")
    else:
        print ("Try to Guess higher..")

    tries +=1
    if tries > 7:
        break
    guess = int(input ("Guess the number again:"))
    if guess == the_number:
        print ("\n\tYou guessed right! The number was", the_number,".")
        print ("\n\tAnd it only took you ",tries, "trials!\n")
    elif tries == 7:
        print ("\n\tOOPS!!!!Game over\n\tThe number was", the_number)
    else:
        print ("")
input("\nPress enter key to exit.")
