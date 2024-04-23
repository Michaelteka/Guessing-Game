Word Guessing Game
Project Overview
Hey there!
#Welcome to the Word Guessing Game repo! This project is a fun little game built in Python where you guess letters to figure out a secret word. You can play by yourself or with friends, and there are a few different rules and mechanics to keep things interesting. How It Works Secret Word: The game kicks off by picking a random word from a list we've created. It could be anything from a fruit to an animal, or something else entirely. Scoring: The fewer guesses you need to find the secret word, the better your score. It's all about being efficient with your guesses.

#Explaining the code 
def get_word():
    words = ['shirts', 'pants', 'shoes', 'jackets', 'sweaters']
    return random.choice(words)

#The get_word function returns a random word from a list of potential words (words). This list can be expanded or modified to change the game's vocabulary. The use of random.choice(words) ensures that each game starts with a different secret word, keeping the game fresh.

def display(word, guessed_letters):
    display_letter = [letter if letter in guessed_letters else '_' for letter in word]
    return ' '.join(display_letter)
#The display function is responsible for showing the current state of the word to the player. It takes two arguments: the secret word (word) and the set of guessed letters (guessed_letters). It constructs a list of characters (display_letter), where each letter is revealed if it's been guessed, or replaced with an underscore (_) if it hasn't. The return ' '.join(display_letter) line converts this list into a string with spaces between the letters, making it easy to display to the player.

def play_game():
    word = get_word()
    guessed_letters = set()
    attempts = 10
#The play_game function contains the main logic for running the game. Here's what each part does:
Getting the Secret Word: The word = get_word() line sets the secret word by calling the get_word function.
Tracking Guessed Letters: guessed_letters = set() initializes an empty set to keep track of the letters the player has guessed. Using a set ensures that each guessed letter is unique, preventing duplicates.
#Setting the Number of Attempts: attempts = 10 defines the maximum number of attempts the player has to guess the word.
Game Welcome Message: The print statements provide a brief introduction to the game and inform the player of their 10 attempts.

while attempts > 0:
    print(display(word, guessed_letters))
    guess = input("Enter a letter: ").lower()
#Display the Current State of the Word: print(display(word, guessed_letters)) shows the current state of the word to the player, with guessed letters revealed and others hidden.
Get Player's Guess: guess = input("Enter a letter: ").lower() prompts the player to enter a letter. The lower() method converts the input to lowercase, ensuring consistent case handling.
