# Almost final take at hangman before reading chapter, just need to add comments to clarify
# Next step after chapter is making this word for varying lengths of secret words
import time

print('Welcome to hangman!') # prints a simple welcome to the player
wannaPlay = True             # sets the while loop control variable to true

while wannaPlay == True:     # the entire game is housed within a while loop that only executes while the player wants to play

    secretWord  = 'cat'      # this is just for testing; need to learn to generate random word/break word down into chars
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
    
    while guessed == False and bodyParts != 6:
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
        if userGuess == letterOne:
            print ('That\'s correct! \'' + userGuess + '\' is the first letter of the secret word.')
            letterOneGuessed = True
            spaceOne = '_' + userGuess + '_ '
        elif userGuess == letterTwo:
            print ('That\'s correct! \'' + userGuess + '\' is the second letter of the secret word.')
            letterTwoGuessed = True
            spaceTwo = '_' + userGuess + '_ '
        elif userGuess == letterThree:
            print ('That\'s correct! \'' + userGuess + '\' is the last letter of the secret word.')
            letterThrGuessed = True
            spaceThree = '_' + userGuess + '_ '
        else:
            print('Sorry, that letter isn\'t in the secret word.')
            missedLetters = missedLetters + userGuess + ', ' # need to add if statement for cleaner , population
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
            else:
                legs = '    / \\'
                print('     +---+     ') 
                print(head + '   |    ')
                print(body + '  |     ')
                print(legs + '  |     ')
                print('        ===    ')
                print('Sorry, you\'ve run out of guesses.')

            bodyParts = bodyParts + 1
            

        if letterOneGuessed == True and letterTwoGuessed == True and letterThrGuessed == True:
            guessed = True
        else:
            guessed = False

    print('Wanna play again? (y or n)')
    yesNo = input()
    if yesNo == 'y':
        wannaPlay = True
    else:
        wannaPlay = False    
