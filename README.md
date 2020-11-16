# mattG
import time

# Game answers
answer_A = ["A", "a"]
answer_B = ["B", "b"]
answer_C = ["C", "c"]
game_name = " ~ The Pickle Quest ~ "
game_end = "\n" + ": " + game_name + "\n game created by: Matt G."
# grabbing objects
stick = 0
morning_star = 0

required = "\nUse only A, B, or C\n"


# Game function!

# intro to the story!
def intro():
    time.sleep(0)
    print("\nThis quest begins on a day just like any other,\n"
          "you and Pickle (your puppy) are on a walk through the 'dark forest'."
          "\nYou have never been here before and both of you are quite concerned that\n"
          "it will start getting dark soon!\n\n"
          ".......\n")
    time.sleep(0)
    print("Suddenly you hear a noise behind you! At which point 'Pickle' from nowhere says....\n\n"
          "" + player_name.upper() + " we are is great danger! we need to run towards the mountains!\n"
                                     "PLEASE TRUST ME !!")
    time.sleep(0)
    print("\n\n")
    print("You need to thing quickly!!\n"
          "A.) Do you follow 'Pickle' towards the mountains?\n"
          "B.) Do you try and run to the car?\n"
          "C.) Do you throw a rock in the direction of the noise?\n")
    choice_1 = input("Please Chose: ")
    time.sleep(0)
    if choice_1 in answer_A:
        mountain_option()

        game_middle()

    elif choice_1 in answer_B:
        car_option()

        game_middle()

    elif choice_1 in answer_C:
        rock_option()
    else:
        print(required)
        intro()


def car_option():
    print("You start running!! SUDDENLY you feel your leg "
          "being grabbed by something wet and sharp!!\n\n"
          "You can feel that this 'something' is just about to pull you away!\n"
          "....... With the corner of your eye you can see 'Pickle' bite and"
          " get the 'something' of your leg!!...\n"
          "~ 'Pickle' ~ goes on to say, come on lets run to the mountains!!!\n\n")


def mountain_option():
    print("'Pickle' repeats again, " + player_name + "RUN!!\n"
                                                     "you start running....\n\n")


def rock_option():
    print("You throw a rock... you see a shadowy silhouette appear.\n"
          "...'BANG'... you see blood appearing on your top...\n"
          "you go down to the ground. With your last breath you shout!\n"
          "'Pickle RUN!!! ")
    print("\n\n You lose " + game_name + "!\n")
    print(game_end)


def game_middle():
    print("You have been running for some time now! Your legs are getting really tired and finding"
          " it more difficult "
          "to catch a breath!!\n"
          "Pickle can see this and is getting concerned that you will not reach the mountains in time!")
    print("\nWhiles running 'Pickle' shouts cave! I know this way, lets go to the cave!\n"
          "She goes on to explain that this cave will be safer and it will take you "
          "to where you need to be!\n"
          "you decide to go in.")
    print("You approach the cave entrance, there is a big door blocking it!"
          "\nOn the door you can see a question, and some "
          "writing saying only ones that can pass this test can pass!\n\n"
          "I have cities, but no houses. I have mountains, but no trees. "
          "I have water, but no fish. What am I?\n"
          "A.) You answer - A painting!\n"
          "B.) You answer - A map!\n"
          "C.) You answer - A game!\n")

    choice_2 = ""
    while choice_2 not in answer_B:
        choice_2 = input("Please chose: ")
        if choice_2 in answer_B:
            print("\nThe door opens...\nYou and Pickle run inside!")
        else:
            print("The door remains shut...")


def cave_part_one():
    print("hello")


# main game intro (player info)

game_name = " ~ The Pickle Quest ~ "
print("\nWelcome to: " + game_name)

print("\nIn this game every decision you make will alter the outcome of the Quest....\n"
      "'Please Chose Wisely! ...'\n")

game_start = input("Are you ready to START(YES/NO)?: ").upper()
if game_start == "YES":
    print("Welcome to  " + game_name)
    player_name = input("Before you start your Adventure...\n"                 "What is your name?: ")
    player_age = int(input("What is your age?: "))
    if player_age > 18:
        print("Master " + player_name + " with age comes experience,"
                                        " you can continue on this Quest! ")
        intro()

    else:
        print("Brave Adventurer "
              + player_name + " you are to young to "
                              "participate in " + game_name)
        print(" ~ Your adventure ended before it even began! ~ \n"
              " ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ \n"
              "~~~   Turn back now   ~~~\n\n" + ": " + game_name + "\n game created by: Matt G.")
else:
    print(" ~ Your adventure ended before it even began! ~ \n"
          " ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ ")
    game_end = "\n" + ": " + game_name + "\n game created by: Matt G."
    print(game_end)
