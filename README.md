#First take at hangman before reading chapter
import time

print('Welcome to hangman!')
time.sleep(1)
print('Player 1: What is the secret word?')
word = input()
# spaces = string length (input)

guessed = False
bodyParts = 0
missingLetters = ''
head = '      '
body = '      '
legs = '      '  

# while guessed == false and bodyParts < 6:
print('     +---+     ')
print(head + '   |    ')
print(body + '   |    ')
print(legs + '   |    ')
print('        ===    ')
print('Missed letters:')
print(  missingLetters )
print('Guess a letter.')
userGuess = input()
# check guess against letters in secret word
'''
if userGuess ==

else
    head = '     O'
'''
head = '     O'

print('     +---+     ')
print(head + '   |    ')
print(body + '   |    ')
print(legs + '   |    ')
print('        ===    ')
print('Missed letters:')
print(  missingLetters )
print('Guess a letter.')
userGuess = input()
