# game
Snake water gun game (Python)
import random 
computer = random.choice([-1, 0, 1])
youstr = input("Enter your choice (s for snake, w for water, g for gun):")
youDict = {"s": 1, "w": -1, "g": 0}
reverseDict = {1: "snake", -1: "water", 0: "gun"}
you = youDict[youstr]
print(f"You chose {reverseDict[you]}\nComputer chose {reverseDict[computer]}")
if computer == you:
    print("It's a draw")
else:
    if (computer == -1 and you == 1):  # snake drinks water
        print("You Won!")
    elif (computer == 0 and you == -1):  # water destroys gun
        print("You Won!")
    elif (computer == 1 and you == 0):  # gun kills snake
        print("You Won!")
    else:
        print("You Lose!")
