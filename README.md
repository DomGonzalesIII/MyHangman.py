#Third take at hangman before reading chapter
import time

print('Welcome to hangman!')
time.sleep(1)
print('Let\'s play!')

# generate secret word (a random. function perhaps?)
# the following code is for secret words of static length 3
# once I know more about arrays, I can make the secret word varying lengths
secretWord = "   "

# need to know secret word for testing purposes, will remove
print(secretWord)

letterOne = ' ' # need some sort of reading function to read the letters of secret word
letterTwo = ' '
letterThree = ' '

# initializing variables to be used in while loop
letterOneGuessed   = False
letterTwoGuessed   = False
letterThreeGuessed = False
bodyParts = 0
missedLetters = ''
head = '      '
    body = '       '
legs = '       '  

''' next code will take user input and compare it to secret word
    if part of secret word, gets added, else adds body part'''



''' While loop parameters will have to change if secretWOrd has more than 3 letters
    while letterOneGuessed == False and letterTwoGuessed == False and letterThreeGuessed == False and bodyParts != 6:
        print('     +---+     ')
        print(head + '   |    ')
        print(body + '  |     ')
        print(legs + '  |     ')
        print('        ===    ')
        print('Missed letters:')
        print(  missedLetters  )
        print('Guess a letter.')
        userGuess = input() # maybe userGuess = char(input())?
        
        # check guess against letters in secret word
        if userGuess == letterOne or userGuess == letterTwo or userGuess == letterThree:
            print('That\'s right!') # maybe add userGuess is the blank number letter in the secret word

            if userGuess == letterOne:
                letterOneGuessed = True
            elif userGuess == letterTwo:
                letterTwoGuessed = True
            else userGuess == letterThree
                letterThreeGuessed = True
            
        else:
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
'''

''' the following while loop is only to validate body part/stand print alignment,
    it doesn't check correct/incorrect guesses yet '''
while bodyParts != 7:

    print('     +---+     ')
    print(head + '   |    ')
    print(body + '  |     ')
    print(legs + '  |     ')
    print('        ===    ')
    print('Missed letters:')
    print(  missedLetters  )

    # check guess against letters in secret word
    # add somewhere to check if that letter has been guessed
    # add letters that don't match to missed letters string
    # body part assignment will need to come after guess has
    # been verified as good no good, current test set up assumes guess is wrong




    # need to review end output, current end of game print seems odd




    if bodyParts == 0:
        head = '     O'
        print('Guess a letter.')
        userGuess = input()
    elif bodyParts == 1:
        body = '     | '
        print('Guess a letter.')
        userGuess = input()
    elif bodyParts == 2:
        body = '    /| '
        print('Guess a letter.')
        userGuess = input()
    elif bodyParts == 3:
        body = '    /|\\'
        print('Guess a letter.')
        userGuess = input()
    elif bodyParts == 4:
        legs = '      \\'
        print('Guess a letter.')
        userGuess = input()
    elif bodyParts == 5:
        legs = '    / \\'
        print('Guess a letter.')
        userGuess = input()
    else:
        print ('Sorry, you lose.')

    bodyParts = bodyParts + 1
