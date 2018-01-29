#First take at hangman before reading chapter
import time

print('Welcome to hangman!') # prints a simple welcome to the player
wannaPlay = True             # sets the while loop control variable to true

while wannaPlay = True:      # the entire game is housed within a while loop that only executes while the player still wants to play

    secretWord  = 'cat'      # this is just for testing; need to learn to generate random word and break it down into individual chars
    letterOne   = 'c'
    letterTwo   = 'a'
    letterThree = 't' 


    
    guessed = False          # this variable will be used in the 'has player won' while loop
    letterOneGuessed = False # the following three variables combined will make 'guessed' true if all true
    letterTwoGuessed = False
    letterThrGuessed = False
    bodyParts = 0            # the value in bodyParts and the status of guessed will control when the game ends
    missedLetters = ''       # this variable will carry a list of the player's previos incorrect guesses
    head = '      '          # this variable will add the head when the player makes their first wrong guess
    body = '       '         # this variable will add the body and arms as the player makes more wrong guesses
    legs = '       '         # this variable will add the legs as the player makes their last wrong guesses

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
