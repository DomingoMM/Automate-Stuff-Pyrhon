# Automate-Stuff-Pyrhon
In this repository, I will be uploading my solutions to some of the programming tasks provided in the book Automate the boring stuff with Python.


## Coin programm

import random

def toss():
    flip = random.randint(0, 1)
    if flip == 0:
        return 'H'
    else:
        return 'T'

number_of_streaks = 0
results=[]
streak=0

for experimentNumber in range(10000):
    # Code that creates a list of 100 'heads' or 'tails' values.
    for i in range(100):
        results.append(toss())
    

    # Code that checks if there is a streak of 6 heads or tails in a row.
    for listItem in range(len(results)-1):
        if results[listItem]==results[listItem+1]:
            streak +=1
            if streak == 6:
                number_of_streaks+=1
                streak=0
        else:
            streak=0
    results=[]
    
print('Chance of streak: %s%%' % (number_of_streaks / 100))


##Print program

grid = [['.', '.', '.', '.', '.', '.'],
        ['.', 'O', 'O', '.', '.', '.'],
        ['O', 'O', 'O', 'O', '.', '.'],
        ['O', 'O', 'O', 'O', 'O', '.'],
        ['.', 'O', 'O', 'O', 'O', 'O'],
        ['O', 'O', 'O', 'O', 'O', '.'],
        ['O', 'O', 'O', 'O', '.', '.'],
        ['.', 'O', 'O', '.', '.', '.'],
        ['.', '.', '.', '.', '.', '.']]
        

for i in range(6):
    for j in range(len(grid)):
        print(grid[j][i], end='')
    print()
        

