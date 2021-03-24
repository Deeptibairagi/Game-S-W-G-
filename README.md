# Game-S-W-G-
Snake, Water, Gun

import random
game_list=["S", "W", "G"]
you_point= 0
computer_point = 0
num_time=1
while num_time<=10:
    Computer = random.choice(game_list)
    You = input("Choise your word:\nS snake,W water,G gun\n")
    if You=="G" and Computer=="S":
        print(f"Your guess {You} & computer {Computer}\n","You win 1 point")
        you_point=you_point+1
    elif You=="G" and Computer=="W":
        print(f"Your guess {You} & computer {Computer}\n","Computer win 1 point")
        computer_point=computer_point+1
    elif You=="G" and Computer=="G":
        print(f"Your guess {You} & computer {Computer}\n","Tie both 0 point")
    elif You=="W" and Computer=="G":
        print(f"Your guess {You} & computer {Computer}\n","You win 1 point")
        you_point=you_point+1
    elif You == "W" and Computer == "S":
        print(f"Your guess {You} & computer {Computer}\n","Computer win 1 point")
        computer_point=computer_point+1
    elif You == "W" and Computer == "W":
        print(f"Your guess {You} & computer {Computer}\n","Tie both 0 point")
    elif You=="S" and Computer=="W":
        print(f"Your guess {You} & computer {Computer}\n","You win 1 point")
        you_point=you_point+1
    elif You == "S" and Computer == "G":
        print(f"Your guess {You} & computer {Computer}\n","Computer win 1 point")
        computer_point=computer_point+1
    elif You == "S" and Computer == "S":
        print(f"Your guess {You} & computer {Computer}\n","Tie both 0 point")
    else:
        print("Invalid value")
    num_time=num_time+1
print("Game over")
if you_point>computer_point:
    print(f"You are a Winner\nyour point {you_point} & computer point {computer_point}")
elif you_point<computer_point:
    print(f"You lose the game\n your point {you_point} & computer point {computer_point}")
elif you_point==computer_point:
    print(f"Tie Game\n your point {you_point} & computer point {computer_point}")
