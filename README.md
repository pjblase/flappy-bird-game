# magic 8 ball
this the magic 8 ball game

# This is where the code is going to be.
# W.I.P
import random
import time

responses = [
    "It is certain.",
    "It is decidedly so.",
    "Without a doubt.",
    "Yes definitely.",
    "You may rely on it.",
    "As I see it, yes.",
    "Of course",
    "Yes.",
    "Signs point to yes.",
    "Reply hazy, try again.",
    "Ask again later.",
    "Better not tell you now.",
    "Cannot predict now.",
    "Concentrate and ask again.",
    "Do not count on it.",
    "My reply is no.",
    "My sources say no.",
    "Outlook not so good.",
    "Very doubtful."]


def play_game():
    inp = input('What do you want from the magnificent 8 ball?')
    print("You asked: '" + str(inp) + "'")
    time.sleep(1)
    print("Let me see... ")
    time.sleep(1.25) 
    print("...Sorry got distracted... ")
    time.sleep(1.5)
    print("...Aha, got it... ")
    time.sleep(1.25)
    print(responses[random.randint(0, len(responses) - 1)])
    play_again()  

def play_again():
    quest = input("What else you want home slice?")
    if quest == 'yes':
        print('')
        play_game()
    elif quest != 'yes':
        print('')
        time.sleep(1.5)
        print('...I have to see you later homie ...')
        quit()

play_game()
