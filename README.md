# ROCK-PAPER-SCISSORS-GAME
import random, sys 

print("ROCK, PAPER, SCISSORS")

wins = 0 
losses = 0
ties = 0


while True: #the main game loop
    
    while True:
        print(f"Wins:{wins},Losses:{losses},Ties:{ties}")      #print("Wins:",wins,"Losses:", losses) additional way to write code 
        print("Enter your move: (r)ock, (p)aper, (s)cissors or (q)uit")
        playermove = input()
        if playermove == 'q':
            sys.exit()
        if playermove == 'r' or playermove == 'p' or playermove == 's' :
            break
        print ("Type one of r, p, s or q")   
        
    #Recording player move 
    if playermove == 'r':
        print("ROCK V/S ...")
    elif playermove == 'p':
        print("PAPER V/S ...")
    elif playermove == 's':
        print("SCISSORS V/S ...") 
              
    # Computer move
    
    randomNumber = random.randint(1,3)
    if randomNumber == 1:
        computermove = 'r'
        print("ROCK")
    if randomNumber == 2:
        computermove = 'P'
        print("PAPER")   
    if randomNumber == 2:
        computermove = 's'
        print("SCISSORS")    
        
    #displaying wins/losses/ties
    if playermove == computermove :
        print("It's a tie!")
        ties = ties + 1 
        
    #winning moves 
    
    elif playermove == 'r' and computermove == 's':
        print ("You win !")
        wins += 1
    elif playermove == 'p'and computermove == 'r':
        print ("You win !")
        wins += 1
    elif playermove == 's'and computermove == 'p':
        print ("You win !")
        wins += 1
        
    #losing moves  
    
    elif playermove == 's' and computermove == 'r':
        print ("You lose !")
        losses += 1
    elif playermove == 'r' and computermove == 'p':
        print ("You lose !")
        losses += 1
    elif playermove == 'p' and computermove == 's':
        print ("You lose !")
        losses += 1
    
