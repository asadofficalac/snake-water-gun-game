'''
snake = 1
water = -1
gun = -0

'''
import random

computer = random.choice([0, 1, -1])
you_str = input("Enter you choice: ")
you_dic = {"s":1, "w":-1, "g":0}
revers_dic = {1:"s", -1:"w", 0:"g"}

you = you_dic[you_str]

print(f"You choice {revers_dic[you]}\nComputer choice {revers_dic[computer]}")
if (you == computer):
    print("Draw")
else:
    if(you==1 and computer==-1):
        print("you win")
    elif(you==0 and computer==-1):
        print("you lose")
    elif(you==-1 and computer==1):
        print("you lose")    
    elif(you==0 and computer==1):
        print("you win")
    elif(you==-1 and computer==0):
        print("you win")
    elif(you==1 and computer==0):
        print("you lose")
