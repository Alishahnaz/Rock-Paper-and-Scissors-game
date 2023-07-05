# Rock-Paper-and-Scissors-game
This game has 9 different possibilities.There are 2 friends playing. Lets explore
import random

def determine_winner(player_choice, computer_choice):
    if player_choice == computer_choice:
        return "It's a tie!"
    elif (
        (player_choice == "rock" and computer_choice == "scissors") or
        (player_choice == "scissors" and computer_choice == "paper") or
        (player_choice == "paper" and computer_choice == "rock")
    ):
        return "Player wins!"
    else:
        return "Computer wins!"

def play_game():
    choices = ["rock", "scissors", "paper"]
    player_choice = input("Enter your choice (rock/scissors/paper): ").lower()
    while player_choice not in choices:
        print("Invalid choice! Please try again.")
        player_choice = input("Enter your choice (rock/scissors/paper): ").lower()

    computer_choice = random.choice(choices)
    print(f"Computer chooses: {computer_choice}")

    result = determine_winner(player_choice, computer_choice)
    print(result)

play_game()

