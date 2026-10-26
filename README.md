# Number-Guessing
A simple Python Number Guessing Game where players guess a random number between 1 and 100. It provides hints, counts attempts, and allows multiple rounds using loops and functions.

import random

# Function to play the game
def play_game():
    number = random.randint(1, 100)
    attempts = 0

    print("\nWelcome to Number Guessing Game!")
    print("Guess a number between 1 and 100")

    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1

            if guess < number:
                print("Too low! Try again.")

            elif guess > number:
                print("Too high! Try again.")

            else:
                print("Correct Guess!")
                print("Total attempts:", attempts)
                break

        except ValueError:
            print("Please enter a valid number!")

# Main program
while True:
    play_game()

    choice = input("Play again? (yes/no): ").lower()

    if choice != "yes":
        print("Thank you for playing!")
        break
23
