import time
import random

def intro():
    print("\nWelcome to the Cavern of Challenges!")
    print("You are a brave adventurer seeking the legendary Crystal of Truth.")
    print("Let's begin your journey...\n")

def choose_path():
    print("You find yourself at a fork in the cavern.")
    print("Do you go left into the darkness or right toward a faint glow?")
    return input("Choose 'left' or 'right': ").lower()

def encounter_enemy():
    print("\nA wild cave troll appears!")
    choice = input("Do you want to 'fight' or 'run'? ").lower()
    if choice == "fight":
        if random.choice([True, False]):
            print("You defeated the troll with your sword!")
            return True
        else:
            print("The troll was too strong... You were defeated.")
            return False
    else:
        print("You managed to escape safely!")
        return True

def puzzle_room():
    print("\nYou reach a chamber with a stone door and a riddle carved on it:")
    print("“I speak without a mouth and hear without ears. I have nobody, but I come alive with the wind. What am I?”")
    answer = input("Your answer: ").strip().lower()
    if answer == "echo":
        print("The door rumbles open. Correct!")
        return True
    else:
        print("Wrong! The door remains sealed forever.")
        return False

def timed_decision(turns_left):
    print("\nYou are in a collapsing tunnel!")
    print("You must choose one of three levers to open the exit.")
    print(f"You have {turns_left} turns before the tunnel collapses.")
    for i in range(turns_left):
        lever = input("Choose a lever (1, 2, or 3): ")
        if lever == "2":
            print("The exit opens just in time! You escape!")
            return True
        else:
            print("Nothing happens...")
    print("The tunnel collapses. You're trapped forever.")
    return False

def adventure():
    inventory = []

    intro()

    # First Choice
    path = choose_path()
    if path == "left":
        if encounter_enemy():
            inventory.append("key")
        else:
            return
    else:
        print("You found a glowing orb. It might be useful.")
        inventory.append("orb")

    # Puzzle Room
    if not puzzle_room():
        return

    # Inventory Check
    print("\nA gate blocks your path. It needs a key.")
    if "key" in inventory:
        print("You use the key to open the gate.")
    else:
        print("You don't have the key. There's no way forward.")
        return

    # Timed Decision
    if timed_decision(3):
        print("\n🎉 Congratulations! You found the Crystal of Truth and completed the adventure!")
    else:
        print("\n💀 Your journey ends here.")

if __name__ == "__main__":
    adventure()
