# First take at hangman before reading chapter
# Next step after chapter is making this word for varying lengths of secret words
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
    missedLetters = 'Missed letters:'       # this variable will carry a list of the player's previos incorrect guesses
    head = '      '          # this variable will add the head when the player makes their first wrong guess
    body = '       '         # this variable will add the body and arms as the player makes more wrong guesses
    legs = '       '         # this variable will add the legs as the player makes their last wrong guesses
    spaceOne   = '___ '      # the following three variables creat blanks that correctly guessed letters will be displayed on
    spaceTwo   = '___ '
    spaceThree = '___ '
    # need variable to check if player has guessed this letter before. How?
    
    while guessed = False and bodyParts != 6:
        print('     +---+     ')  # the following print statements print the hangman character as incorrect guesses are made
        print(head + '   |    ')
        print(body + '  |     ')
        print(legs + '  |     ')
        print('        ===    ')
        print(  missedLetters  )  # this contains a list of missed 
        print( spaceOne + spaceTwo + spaceThree) # prints blank spaces

        print('Guess a letter.')
        userGuess = input()  # this takes the user's input as a guessed char (maybe add char(userGuess) if that's a thing

'''
        while userGuess == wayToTellIfTheyAlreadyGuessedThisLetter:
            print('Sorry, you've already guessed that letter.\nPlease guess again.')
            userGuess =input
'''
        if userGuess = letterOne:
            print ('That\'s correct! \'' + userGuess + '\' is the first letter of the secret word.')
            letterOneGuessed = True
            spaceOne = '_' + userGuess + '_ '
        elif userGuess = letterTwo:

        elif userGuess = letterThree:

        else:


        if letterOneGuessed == True and letterTwoGuessed == True and letterThrGuessed == True:
            guessed = True
        else
            guessed = False
