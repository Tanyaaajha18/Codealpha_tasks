# Codealpha_tasks


import random

# Sample responses for a simple chatbot
responses = {
    "hi": ["Hello!", "Hi there!", "Hey!"],
    "how are you": ["I'm good, thank you!", "Doing well, how about you?", "I'm just a bot, but I'm doing great!"],
    "bye": ["Goodbye!", "See you later!", "Bye! Have a nice day!"],
    "default": ["I'm not sure how to respond to that.", "Could you rephrase?", "Interesting... tell me more!"]
}

def get_response(user_input):
    user_input = user_input.lower().strip()
    return random.choice(responses.get(user_input, responses["default"]))

def chat():
    print("Chatbot: Hi! Type 'bye' to exit.")
    while True:
        user_input = input("You: ")
        if user_input.lower().strip() == "bye":
            print("Chatbot:", random.choice(responses["bye"]))
            break
        response = get_response(user_input)
        print("Chatbot:", response)

if _name_ == "_main_":
    chat()
