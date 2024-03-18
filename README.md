name = input("Enter the name of the user: ")
gender = input("Enter the gender of the user: ")
age = int(input("Enter the age of the user: "))
height = int(input("Enter the height of the user (in cm): "))
weight = int(input("Enter the weight of the user (in kg): "))

print("Name of user:", name)
print("Gender of user:", gender)
print("Age of user:", age)
print("Height of user:", height, "cm")
print("Weight of user:", weight, "kg")

print("Which exercise do you want to take on:")
print("1. Running")
print("2. Push-ups")

choice = int(input("Enter your choice: "))

if choice == 1:
    print("Your goal is to run 1.6 km daily.")
    remaining_distance = 0
    for day in range(1,31):
        distance = input(f"Did you complete your {day}th day challenge? (yes/no): ")
        if distance == "no":
            d = float(input(f"enter your remaining km of {day}th day?: "))
            remaining_distance += d
            print(f"remainimg {d} km.")
        elif distance == "yes":
            print("OK")
        else:
            print("Invalid input. Please enter 'yes' or 'no'.")
    if remaining_distance > 0:
        print(
            f"Your challenge is not complete. You still need to run {remaining_distance:.2f} km."
        )
    else:
        print("Congratulations🥳💫! You have completed your running challenge.")
elif choice == 2:
    print("Your goal is to do 100 push-ups daily.")
    remaining_pushups = 0
    for day in range(1, 30):
        completed = input(f"Did you complete your {day}th day challenge? (yes/no): ")
        if completed == "no":
            sets = int(input(f"enter your remaining push up of {day}th day?: "))
            remaining_pushups += sets
            print(f"You did {sets} push-ups.")
        elif completed == "yes":
            print("OK")
        else:
            print("Invalid input. Please enter 'yes' or 'no'.")
    if remaining_pushups > 0:
        print(f"Your challenge is not complete. You still need to do {remaining_pushups} push-ups.")
    else:
        print("Congratulations🥳💫! You have completed your push-up challenge.")
else:
    print("Invalid choice. Please choose either 1 or 2 for exercise.")
