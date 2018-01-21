#First take at hangman before reading chapter
import time

print('Welcome to hangman!')
time.sleep(1)
print('Player 1: What is the secret word?')
word = input()
# code for referencing letter guesses will go here
# spaces = string length (input)

guessed = False
bodyParts = 0
missedLetters = ''
head = '      '
body = '       '
legs = '       '  

''' next code will take user input and compare it to secret word
    if part of secret word, gets added, else adds body part'''

# while guessed == false and bodyParts != 6:

''' the following while loop is only to validate body part/stand print alignment,
    it doesn't check correct/incorrect guesses yet '''
while bodyParts < 7:

    print('     +---+     ')
    print(head + '   |    ')
    print(body + '  |     ')
    print(legs + '  |     ')
    print('        ===    ')
    print('Missed letters:')
    print(  missedLetters  )
    print('Guess a letter.')
    userGuess = input()
    # check guess against letters in secret word
   
    if bodyParts == 0:
        head = '     O'
    elif bodyParts == 1:
        body = '     | '
    elif bodyParts == 2:
        body = '    /| '
    elif bodyParts == 3:
        body = '    /|\\'
    elif bodyParts == 4:
        legs = '      \\'
    elif bodyParts == 5:
        legs = '    / \\'
    else:
        print('Sorry, you lose.')

    bodyParts = bodyParts + 1
