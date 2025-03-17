# python_practice
A collection of my Python practice scripts
import random

def guess_number():
    number = random.randint(1, 10)
    attempts = 0
    print("Guess a number between 1 and 10.")

    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1
            if guess < number:
                print("Too low! Try again.")
            elif guess > number:
                print("Too high! Try again.") 
            else:
                print(f"🎉 Correct! You guessed it in {attempts} attempts.")
                break
        except ValueError:
            print("Please enter a valid number.")

guess_number()
