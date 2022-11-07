import turtle

turtle.screensize(canvwidth=450, canvheight=450)

FILENAME = "turtle-draw.txt"

inputFILENAME = input("Enter file name: turtle-draw.txt/n")
print(FILENAME)

Textfile = open(inputFILENAME, 'r')

line = FILENAME.readline()
turtledraw = turtle.Turtle()
turtledraw.speed(15)
turtledraw.penup()

while line:
    splits = line.split('')

    if(len(splits)) == 3:
        color = splits[0]
        x = int(splits[1])
        y = int(splits[2])

        turtledraw.color(color)
        turtledraw.goto(x,y)
        turtledraw.pendown()

        while turtledraw == turtledraw.pendown():
            turtledraw = turtle.distance(x,y)
            Totaldistance = turtle.distance(x,y) + turtle.distance(x,y)

    if splits[0] != color:
        turtledraw.penup()
        turtledraw != turtle.distance(x,y)

Line = FILENAME.readline

totaldistance = turtle.distance(x,y) + turtle.distance(x,y)
print(totaldistance)

turtle.done
