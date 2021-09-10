# Bizim-Marian
#Connect 4 (My first project)
#Create the field
def drawField(field):
    for row in range(11):
        if row %2 == 0:
            practicalRow = int(row / 2)
            for column in range(11):
                if column % 2 == 0:
                    practicalColumn = int(column/2)
                    if column != 10:
                        print(field[practicalColumn][practicalRow],end="")
                    else:
                        print(field[practicalColumn][practicalRow])
                else:
                    print("|",end = "")
        else:
            print("------------")
Player = 1
currentField = [[" ", " ", " ", " ", " ", " ", " "],[" ", " ", " ", " ", " ", " ", " "],[" ", " ", " ", " ", " ", " ", " "],[" ", " ", " ", " ", " ", " ", " "],[" ", " ", " ", " ", " ", " ", " "],[" ", " ", " ", " ", " ", " ", " "],[" ", " ", " ", " ", " ", " ", " "]]
drawField(currentField)
while (True):
    print("Players turn: ", Player)
    MoveColum = int(input("Please enter the column: \n"))

    #If the space is empty place an X
    if Player == 1:
        if currentField[MoveColum][5] == " ":
            currentField[MoveColum][5] = u"\u2716"
            Player = 2
        elif currentField[MoveColum][4] == " ":
            currentField[MoveColum][4] = u"\u2716"
            Player = 2
        elif currentField[MoveColum][3] == " ":
            currentField[MoveColum][3] = u"\u2716"
            Player = 2
        elif currentField[MoveColum][2] == " ":
            currentField[MoveColum][2] = u"\u2716"
            Player = 2
        elif currentField[MoveColum][1] == " ":
            currentField[MoveColum][1] = u"\u2716"
            Player = 2
        elif currentField[MoveColum][0] == " ":
            currentField[MoveColum][0] = u"\u2716"
            Player = 2

    # If the space is empty place an 0
    else:
        if currentField[MoveColum][5] == " ":
            currentField[MoveColum][5] = u"\u25CB"
            Player = 1
        elif currentField[MoveColum][4] == " ":
            currentField[MoveColum][4] = u"\u25CB"
            Player = 1
        elif currentField[MoveColum][3] == " ":
            currentField[MoveColum][3] = u"\u25CB"
            Player = 1
        elif currentField[MoveColum][2] == " ":
            currentField[MoveColum][2] = u"\u25CB"
            Player = 1
        elif currentField[MoveColum][1] == " ":
            currentField[MoveColum][1] = u"\u25CB"
            Player = 1
        elif currentField[MoveColum][0] == " ":
            currentField[MoveColum][0] = u"\u25CB"
            Player = 1

    drawField(currentField)
    #Declare who's winning Vertical
    if currentField[MoveColum][5] == u"\u2716" and currentField[MoveColum][4] == u"\u2716" and currentField[MoveColum][3] == u"\u2716" and currentField[MoveColum][2] == u"\u2716":
        print("X Wins Vertically")
        break
    elif currentField[MoveColum][5] == u"\u25CB" and currentField[MoveColum][4] == u"\u25CB" and currentField[MoveColum][3] == u"\u25CB" and currentField[MoveColum][2] == u"\u25CB":
        print("O Wins Vertically")
        break
    elif currentField[MoveColum][4] and currentField[MoveColum][3] == u"\u2716"and currentField[MoveColum][2] == u"\u2716" and currentField[MoveColum][1] == u"\u2716":
        print("X Wins Vertically")
        break
    elif currentField[MoveColum][4] == u"\u25CB" and currentField[MoveColum][3] == u"\u25CB" and currentField[MoveColum][2] == u"\u25CB" and currentField[MoveColum][1] == u"\u25CB":
        print("O Wins Vertically")
        break
    elif currentField[MoveColum][3] and currentField[MoveColum][2] == u"\u2716" and currentField[MoveColum][1] == u"\u2716" and currentField[MoveColum][0] == u"\u2716":
        print("X Wins Vertically")
        break
    elif currentField[MoveColum][3] == u"\u25CB" and currentField[MoveColum][2] == u"\u25CB" and currentField[MoveColum][1] == u"\u25CB" and currentField[MoveColum][0] == u"\u25CB":
        print("O Wins Vertically")
        break


    # Declare who's winning Horizontal(row 5)
    elif currentField[0][5] == u"\u2716" and currentField[1][5] == u"\u2716" and currentField[2][5] == u"\u2716" and currentField[3][5] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[0][5] == u"\u25CB" and currentField[1][5] == u"\u25CB" and currentField[2][5] == u"\u25CB" and currentField[3][5] == u"\u25CB":
        print("0 Wins Horizontally")
        break
    elif currentField[1][5] == u"\u2716" and currentField[2][5] == u"\u2716" and currentField[3][5] == u"\u2716" and currentField[4][5] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[1][5] == u"\u25CB" and currentField[2][5] == u"\u25CB" and currentField[3][5] == u"\u25CB" and currentField[4][5] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[2][5] == u"\u2716" and currentField[3][5] == u"\u2716" and currentField[4][5] == u"\u2716" and currentField[5][5] == u"\u2716":
        print("X WinsHorizontally")
        break
    elif currentField[2][5] == u"\u25CB" and currentField[3][5] == u"\u25CB" and currentField[4][5] == u"\u25CB" and currentField[5][5] == u"\u25CB":
        print("O Wins Horizontally")
        break
    # Declare who's winning Horizontal(row 4)
    elif currentField[0][4] == u"\u2716" and currentField[1][4] == u"\u2716" and currentField[2][4] == u"\u2716" and currentField[3][4] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[0][4] == u"\u25CB" and currentField[1][4] == u"\u25CB" and currentField[2][4] == u"\u25CB" and currentField[3][4] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[1][4] == u"\u2716" and currentField[2][4] == u"\u2716" and currentField[3][4] == u"\u2716"and currentField[4][4] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[1][4] == u"\u25CB" and currentField[2][4] == u"\u25CB" and currentField[3][4] == u"\u25CB" and currentField[4][4] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[2][4] == u"\u2716"and currentField[3][4] == u"\u2716" and currentField[4][4] == u"\u2716" and currentField[5][4] == u"\u2716":
        print("X Wins VHorizontally")
        break
    elif currentField[2][4] == u"\u25CB" and currentField[3][4] == u"\u25CB" and currentField[4][4] == u"\u25CB" and currentField[5][4] == u"\u25CB":
        print("O Wins Horizontally")
        break
    # Declare who's winning Horizontal(row 3)
    elif currentField[0][3] == u"\u2716" and currentField[1][3] == u"\u2716"and currentField[2][3] == u"\u2716" and currentField[3][3] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[0][3] == u"\u25CB" and currentField[1][3] == u"\u25CB" and currentField[2][3] == u"\u25CB" and currentField[3][3] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[1][3] == u"\u2716" and currentField[2][3] == u"\u2716" and currentField[3][3] == u"\u2716"and currentField[4][3] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[1][3] == u"\u25CB" and currentField[2][3] == u"\u25CB" and currentField[3][3] == u"\u25CB" and currentField[4][3] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[2][3] == u"\u2716" and currentField[3][3] == u"\u2716" and currentField[4][3] == u"\u2716" and currentField[5][3] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[2][3] == u"\u25CB" and currentField[3][3] == u"\u25CB" and currentField[4][3] == u"\u25CB" and currentField[5][3] == u"\u25CB":
        print("O Wins Horizontally")
        break
    # Declare who's winning Horizontal(row 2)
    elif currentField[0][2] == u"\u2716" and currentField[1][2] == u"\u2716" and currentField[2][2] == u"\u2716" and currentField[3][2] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[0][2] == u"\u25CB" and currentField[1][2] == u"\u25CB" and currentField[2][2] == u"\u25CB" and currentField[3][2] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[1][2] == u"\u2716" and currentField[2][2] == u"\u2716" and currentField[3][2] == u"\u2716" and currentField[4][2] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[1][2] == u"\u25CB" and currentField[2][2] == u"\u25CB" and currentField[3][2] == u"\u25CB" and currentField[4][2] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[2][2] == u"\u2716" and currentField[3][2] == u"\u2716" and currentField[4][2] == u"\u2716" and currentField[5][2] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[2][2] == u"\u25CB" and currentField[3][2] == u"\u25CB" and currentField[4][2] == u"\u25CB" and currentField[5][2] == u"\u25CB":
        print("O Wins Horizontally")
        break
    # Declare who's winning Horizontal(row 1)
    elif currentField[0][1] == u"\u2716" and currentField[1][1] == u"\u2716" and currentField[2][1] == u"\u2716" and currentField[3][1] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[0][1] == u"\u25CB" and currentField[1][1] == u"\u25CB" and currentField[2][1] == u"\u25CB"and currentField[3][1] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[1][1] == u"\u2716" and currentField[2][1] == u"\u2716" and currentField[3][1] == u"\u2716" and currentField[4][1] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[1][1] == u"\u25CB" and currentField[2][1] == u"\u25CB" and currentField[3][1] == u"\u25CB" and currentField[4][1] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[2][1] == u"\u2716" and currentField[3][1] == u"\u2716" and currentField[4][1] == u"\u2716" and currentField[5][1] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[2][1] == u"\u25CB" and currentField[3][1] == u"\u25CB" and currentField[4][1] == u"\u25CB" and currentField[5][1] == u"\u25CB":
        print("O Wins Horizontally")
        break
    # Declare who's winning Horizontal(row 0)
    elif currentField[0][0] == u"\u2716" and currentField[1][0] == u"\u2716" and currentField[2][0] == u"\u2716" and currentField[3][0] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[0][0] == u"\u25CB" and currentField[1][0] == u"\u25CB" and currentField[2][0] == u"\u25CB" and currentField[3][0] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[1][0] == u"\u2716"and currentField[2][0] == u"\u2716" and currentField[3][0] == u"\u2716" and currentField[4][0] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[1][0] == u"\u25CB" and currentField[2][0] == u"\u25CB" and currentField[3][0] == u"\u25CB" and currentField[4][0] == u"\u25CB":
        print("O Wins Horizontally")
        break
    elif currentField[2][0] == u"\u2716" and currentField[3][0] == u"\u2716" and currentField[4][0] == u"\u2716" and currentField[5][0] == u"\u2716":
        print("X Wins Horizontally")
        break
    elif currentField[2][0] == u"\u25CB" and currentField[3][0] == u"\u25CB" and currentField[4][0] == u"\u25CB" and currentField[5][0] == u"\u25CB":
        print("O Wins Horizontally")
        break



    # Declare who's winning Diagonal(To the right)

    elif currentField[0][5] == u"\u2716" and currentField[1][4] == u"\u2716" and currentField[2][3] == u"\u2716" and currentField[3][2] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[0][5] == u"\u25CB" and currentField[1][4] == u"\u25CB" and currentField[2][3] == u"\u25CB" and currentField[3][2] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[1][4] == u"\u2716" and currentField[2][3] == u"\u2716" and currentField[3][2] == u"\u2716" and currentField[4][1] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[1][4] == u"\u25CB"and currentField[2][3] == u"\u25CB" and currentField[3][2] == u"\u25CB" and currentField[4][1] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[2][3] == u"\u2716" and currentField[3][2] == u"\u2716" and currentField[4][1] == u"\u2716" and currentField[5][0] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[2][3] == u"\u25CB" and currentField[3][2] == u"\u25CB" and currentField[4][1] == u"\u25CB" and currentField[5][0] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[1][5] == u"\u2716" and currentField[2][4] == u"\u2716" and currentField[3][3] == u"\u2716" and currentField[4][2] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[1][5] == u"\u25CB" and currentField[2][4] == u"\u25CB" and currentField[3][3] == u"\u25CB" and currentField[4][2] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[2][4] == u"\u2716" and currentField[3][3] == u"\u2716"and currentField[4][2] == u"\u2716" and currentField[5][1] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[2][4] == u"\u25CB" and currentField[3][3] == u"\u25CB" and currentField[4][2] == u"\u25CB" and currentField[5][1] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[2][5] == u"\u2716" and currentField[3][4] == u"\u2716" and currentField[4][3] == u"\u2716" and currentField[5][2] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[2][5] == u"\u25CB" and currentField[3][4] == u"\u25CB" and currentField[4][3] == u"\u25CB" and currentField[5][2] == u"\u25CB":
        print("O Wins Diagonally")
        break

        # Declare who's winning Diagonal(To the left)


    elif currentField[5][5] == u"\u2716" and currentField[4][4] == u"\u2716" and currentField[3][3] == u"\u2716" and currentField[2][2] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[5][5] == u"\u25CB" and currentField[4][4] == u"\u25CB" and currentField[3][3] == u"\u25CB" and currentField[2][2] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[4][4] == u"\u2716" and currentField[3][3] == u"\u2716" and currentField[2][2] == u"\u2716" and currentField[1][1] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[4][4] == u"\u25CB" and currentField[3][3] == u"\u25CB" and currentField[2][2] == u"\u25CB" and currentField[1][1] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[3][3] == u"\u2716" and currentField[2][2] == u"\u2716" and currentField[1][1] == u"\u2716" and currentField[0][0] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[3][3] == u"\u25CB" and currentField[2][2] == u"\u25CB" and currentField[1][1] == u"\u25CB" and currentField[0][0] == u"\u25CB":
        print("O Wins Diagonally")
        break


    elif currentField[4][5] == u"\u2716" and currentField[3][4] == u"\u2716" and currentField[2][3] == u"\u2716" and currentField[1][2] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[4][5] == u"\u25CB" and currentField[3][4] == u"\u25CB" and currentField[2][3] == u"\u25CB" and currentField[1][2] == u"\u25CB":
        print("O Wins Diagonally")
        break
    elif currentField[3][4] == u"\u2716" and currentField[2][3] == u"\u2716" and currentField[1][2] == u"\u2716" and currentField[0][1] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[3][4] == u"\u25CB" and currentField[2][3] == u"\u25CB" and currentField[1][2] == u"\u25CB" and currentField[0][1] == u"\u25CB":
        print("O Wins Diagonally")
        break

    elif currentField[3][5] == u"\u2716" and currentField[2][4] == u"\u2716" and currentField[1][3] == u"\u2716" and currentField[0][2] == u"\u2716":
        print("X Wins Diagonally")
        break
    elif currentField[3][5] == u"\u25CB" and currentField[2][4] == u"\u25CB" and currentField[1][3] == u"\u25CB" and currentField[0][2] == u"\u25CB":
        print("O Wins Diagonally")
        break





    else:
        continue
