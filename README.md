# tic-tac-toe
#just for fun
line1=[1,2,3]
line2=[4,5,6]
line3=[7,8,9]
player="X"

game=bool(True)
while game==True:


    print(str(line1[0])+ " "+str(line1[1])+" "+str(line1[2]))
    print(str(line2[0])+ " "+str(line2[1])+" "+str(line2[2]))
    print(str(line3[0])+ " "+str(line3[1])+" "+str(line3[2]))


    edit=int(input("please chose a no. to mark with "+player+" "))

    if 0<edit<4:
        if edit in line1:        
            line1[line1.index(edit)]=player
        else:
            print("wrong input")
    elif 3<edit<7:
        if edit in line2:
            line2[line2.index(edit)]=player
        else:
            print("wrong input")
    elif 6<edit<10:
        if edit in line3:
            line3[line3.index(edit)]=player
        else:
            print("wrong input")
    elif edit==123:
        break
    else:
        print("wrong input")
    
    if player=="X":
        player="O"
    elif player=="O":
        player="X"

    if line1[1]==line1[2]==line1[0]:
        break
    if line2[1]==line2[2]==line2[0]:
        break
    if line3[1]==line3[2]==line3[0]:
        break

    if line1[0]==line2[0]==line3[0]:
        break
    if line1[1]==line2[1]==line3[1]:
        break
    if line1[2]==line2[2]==line3[2]:
        break

    if line1[0]==line2[1]==line3[2]:
        break
    if line1[2]==line2[1]==line3[0]:
        break

if player=="X":
        print("O wins")
elif player=="O":
        print("X wins")
