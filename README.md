# Treasure-Island---Python-Text-Adventure-Game

# 🏝️ Treasure Island - Python Text Adventure Game

Welcome to **Treasure Island**, a beginner-friendly Python text-based adventure game. Your mission is to survive dangerous choices and find the hidden treasure!

---

## 🎯 Objective

The player is presented with a series of choices. Each choice leads to a new scenario, and ultimately, only the correct sequence of decisions leads to treasure. Wrong choices end the game with various humorous or deadly fates.

---

## 🚀 How to Play

- Run the script using Python 3.
- Follow the prompts and type your decisions (case-insensitive).
- Your fate depends on your choices!

---

## 🛠️ Code Cleanup & Refactoring

This project started with a working version of the game but was refactored for **readability** and **better structure**. Here are the key improvements made:

### ✅ Simplified Control Flow
- The original version used `sys.exit(print(...))` for game termination, which mixed concerns and returned `None`.
- The new version uses a clear nested `if` structure with printed messages only.

### ✅ Removed Redundant Imports
- Removed the unnecessary import of `sys` and `random.choice` which were not used in the final version.

### ✅ Cleaned User Prompts
- Prompts were adjusted for clarity and consistent formatting using `\n` for line breaks.

### ✅ Lowercased Inputs
- All inputs are normalized using `.lower()` to handle case-insensitive responses without repetition.

### ✅ ASCII Art Intro
- Added a detailed ASCII treasure map banner for a fun and thematic introduction to the game.

---

## 🧪 Example Run

```python
import sys
from random import choice

print(r'''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\ ` . "-._ /_______________|_______
|                   | |o ;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
# print("Welcome to Treasure Island.")
# print("Your mission is to find the treasure.")
#
# direction = input("Which way would you like to go? Type Right or Left. ")
# if direction.lower() == "right":
#     sys.exit(print("You fell into a hole GAME OVER!!!"))
#
# lake = input("Looks like you made it to a lake. Would you like to wait or swim? "
#              "Type \"Wait\" to wait for a boat or \"Swim\" to swim across the lake. ")
# if lake.lower() == "swim":
#     sys.exit(print("An alligator ate you GAME OVER!!!"))
#
# house_door = input("A boat picks you up and you made it to a house with 3 doors. "
#                    "Which door would you like to enter Red or Blue or Yellow? ")
# if house_door.lower() == "blue":
#     sys.exit(print("Beast are in here! You are eaten, GAME OVER!!"))
# elif house_door.lower() == "red":
#     sys.exit(print("Everything is on Fire GAME OVER!!"))
# else:
#     print("YOU WIN, YOU FOUND THE TREASURE!!!")

print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.")

choice_1 = input("Which way would you like to go? Type Right or Left.\n").lower()
if choice_1 == "left":
    choice_2 = input("Looks like you made it to a lake. Would you like to wait or swim? "
                     "Type \"Wait\" to wait for a boat or \"Swim\" to swim across the lake.\n").lower()
    if choice_2 == "wait":
        choice_3 = input("A boat picks you up and you made it to a house with 3 doors. "
                         "Which door would you like to enter Red or Blue or Yellow?\n").lower()
        if choice_3 == "blue":
            print("Beast are in here! You are eaten, GAME OVER!!")
        elif choice_3 == "red":
            print("Everything is on fire GAME OVER!!")
        else:
            print("YOU WIN, YOU FOUND THE TREASURE!!!")
    else:
        print("An alligator ate you GAME OVER!!!")
else:
    print("You fell into a hole GAME OVER!!!")








