import random

# Computer randomly chooses between s (1), w (-1), g (0)
computer = random.choice([1, -1, 0])

# User input
you_str = input("Enter your choice (s for snake, w for water, g for gun): ").lower()
you_dic = {"s": 1, "w": -1, "g": 0}
revers_dic = {1: "s", -1: "w", 0: "g"}

# Validate user input
if you_str not in you_dic:
    print("Invalid choice! Please enter 's', 'w', or 'g'.")
else:
    you = you_dic[you_str]

    print(f"You chose {revers_dic[you]}\nComputer chose {revers_dic[computer]}")

    # Determine the winner
    if you == computer:
        print("It's a Draw!")
    elif (you == 1 and computer == -1) or (you == 0 and computer == 1) or (you == -1 and computer == 0):
        print("You Win!")
    else:
        print("You Lose!")
