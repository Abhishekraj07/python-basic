# python-basic
# magical calculator

import re

print("our magical calculator")
print("type quit to exit")

previous = 0
run = True

def perform_maths():

    global run
    global previous

    equation=""
    if previous==0:
        equation = input("enter the equation")
    else:
        equation=input(str(previous))

    if equation=="quit":
        run=False
        print("thank you")
    else:

        equation=re.sub("[a-zA-Z,." "()]","",equation)
        if previous==0:
            previous=eval(equation)
       # print("you typed the equation", previous)

        else:
            previous=eval(str(previous)+ equation)

        print("you typed the equation", previous)






while run:
        perform_maths()
