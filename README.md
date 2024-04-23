# Guessing-Game
Initial commit - set up basic project structure
import random

def get_word():
    words = ['apple', 'banana', 'cherry', 'date', 'elderberry']
    return random.choice(words)

def display(word, guessed_letters):
    display_letter = [letter if letter in guessed_letters else '_' for letter in word]
    return ' '.join(display_letter)

def play_game():
    word = get_word()
    guessed_letters = set()
    attempts = 10

if __name__ == '__main__':
    play_game()
    
