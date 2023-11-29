# codealpha_task_3
import nltk
from nltk.chat.util import Chat, reflections

# Define the chat pairs for the chatbot
pairs = [
    ["hi|hello|hey", ["Hello!", "Hi there!", "Hey!"]],
    ["how are you", ["I'm good, thanks. How about you?", "I'm a bot, so I don't have feelings, but I'm here to help!"]],
    ["what is your name", ["I'm a chatbot. You can call me ChatQ."]],
    ["your age", ["I don't have an age. I'm just a computer program."]],
    ["Your favorite song",["Sorry I am just a program so I don't have favorite song but I recommand for you"]],
    ["Recommand one song for me",["You may like Arijit Singh,Taylor Swift,Atif Aslam songs"]],
    ["bye|goodbye", ["Goodbye!", "See you later!", "Bye!"]],
    ["default", ["I'm not sure how to respond to that. Can you ask me something else?"]]
]
chatbot=Chat(pairs,reflections)
def start_chat():
    print("Hello!I am a chat bot.You can say goodbye to exit")
    while True:
        user_input=input("You:")
        if user_input.lower()=="goodbye":
            print("Bye have a great day")
            break
        response=chatbot.respond(user_input)
        print("ChatQ:",response)
start_chat()
