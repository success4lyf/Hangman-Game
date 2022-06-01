# Hangman-Game
Hangman is a classic game in which a player thinks of a word and the other player tries to guess that word within a certain amount of attempts.

## Explanation

This is an implementation of the Hangman game, where the computer thinks of a word and the user tries to guess it.
This Game starts with a default number of lives and a random word from the word_list as parameters. the user will be asked for a letter and checks if it is in the word. I have used the python object oriented programing to code this game. The parameters, attributes and methods used are as follows:

#### Parameters:

   -  word_list (list):
        List of words to be used in the game
    
   - num_lives (int):
        Number of lives the player has
    
#### Attributes:

   - word (str):
        The word to be guessed picked randomly from the word_list
        
   - word_guessed (list):
        A list of the letters of the word, with '_' for each letter not yet guessed
        For example, if the word is 'apple', the word_guessed list would be ['_', '_', '_', '_', '_']
        If the player guesses 'a', the list would be ['a', '_', '_', '_', '_']
        
   - num_letters (int):
        The number of UNIQUE letters in the word that have not been guessed yet
        
   - num_lives (int):
        The number of lives the player has
        
   - list_letters (list):
        A list of the letters that have already been tried

 #### Methods:

   - check_letter(letter):    
        Checks if the letter is in the word.
        
   - ask_letter():
        Asks the user for a letter.

## Milestone 1
Declaring the class and defining the initializer, and creating the instance variables as shown below:
```python
class Hangman:

    def __init__(self, word_list, num_lives=5):
        self.word_list = word_list
        self.word = random.choice(self.word_list)
        self.num_letters = len(set(list(self.word)))
        self.num_lives = num_lives
        self.list_letters = []
        self.word_guessed = []
        for letter in range(len(self.word)):
            self.word_guessed.append('_')
        self.hangman_pics = [
```
## Milestone 2

This is were the methods are defined. 

- The ask_letter method is defined, asking the player to input a single letter. If the player enters more thane one letter, it will ask the player to enter a single letter, by printing - "Please, enter just one character" to the console. it also checks that the letter hasn't been tried already. If the letter has been tried already, it will ask the user to enter a new letter, and it prints "{letter} was already tried, try again" to the console. 
- The ask_letter method calls the check_letter method to check if the letter is in the word. If it is, it replaces the '_' in the word_guessed list with the letter. If it is not, it reduces the number of lives by 1. 
- while the play_game method Iteratively ask the user for a letter until the user guesses the word or runs out of lives.

## Milestone 3
Game output.

<img width="717" alt="Screenshot 2022-05-30 at 23 49 53" src="https://user-images.githubusercontent.com/78314396/171066701-0e3464f3-0b94-4c01-90c8-26da81ba1f06.png">
