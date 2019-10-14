# Follow-Along Activity - Turtle Graphics
![](https://i.imgur.com/zVWdA5m.png) <- (not this kind of turtle)

In this activity, write a **Python** application and play around with some two-dimensional graphics. It will provide a glimpse into the power of programming and show how fun it can be to write code!

## Python
<a href="https://en.wikipedia.org/wiki/Python_(programming_language)">Python</a> is a popular programming language used by developers all over the world. It is a _general-purpose_ language, which means that developers can use it to write **scripts** that do almost anything: create websites, analyze large data sets, control robots, design video games... the list goes on and on!

### trinket
trinket is a website that allows a developer to write and run code in a web browser. It works in any browser, on any device! This makes it easy to practice coding and show off any programs that are created. During this activity, trinket will be used to build some cool Python programs.

### First Python Program - Hello World
The first program a developer normally writes when learning a new programming language is a "Hello World" program. The goal of these programs is to display a message of "Hello World" to the user. In Python, that program is fairly simple. Follow the steps below to create a Python "Hello World" program:

1. Navigate to https://trinket.io/python/93409853b0 to start building the program
1. Open the hamburger menu in the upper left, and select "Fullscreen" so it is easier to use
1. In the `main.py` file, type the Python command to print a message to the screen:   
    ```python
    print("Hello World")
    ```
1. Click the "Run" button to _run_ the program!

When a developer "runs" their program, they are telling the computer to execute all the code they wrote, and perform the commands they specified. **Commands** are like instructions in a recipe; they tell the computer what to do. Running the "Hello World" program in Python will print the message on the console screen.

#### Challenge: Change the Message
Update the simple "Hello World" program so that instead of saying "Hello World" it says something else!

## Python Library - Turtle Graphics Introduction
Python has a multitude of **libraries** that allow developers to use pre-existing code to build their own applications. One such library is for [turtle graphics](https://en.wikipedia.org/wiki/Turtle_graphics), which are vector graphics that use a cursor (or "turtle") to create images on a Cartesian plane.

### First Turtle Program
Remove any code from the `main.py` file so it is totally blank. Then, on the first line of the file, add the following command:  
```python
from turtle import *
```

This command tells the computer to bring in all the code from the `turtle` library so it is usable in the program! The next step is to create the turtle. First, add a blank line underneath the first line. Then, on the third and fourth lines of the file, add the following commands:
```python
koopa = Turtle()
koopa.shape("arrow")
```

These lines create a turtle and set its shape. In this case, the turtle is `koopa`, but the turtle could have any name. Click the "Run" button to see the "turtle" appear on the page!

#### Challenge: Change the Shape to "turtle"
Update the code so that instead of setting the shape to `"arrow"`, it sets the shape to `"turtle"`. Run the program again to see the shape shift!

### Add Color
Black and white is boring, so we can add some color to the program! On the next line of the `main.py` file, add the following command:  
```python
koopa.color("green")
```

This command will turn the turtle green! Next, we can change the background color. Add a blank line, and then add the following commands:
```python
paper = koopa.getscreen()
paper.bgcolor("azure")
```

These commands get the screen and set its background color to azure. Run the program again to see the new colors on the page!

#### Challenge: Change the Colors
Update the code so that instead of green and azure, the turtle and the background have different colors. For example, the turtle could be blue, and the background could be pink!

## Turtle Graphics - Basic Abilities
Turtles can do a lot! Developers use the turtle abilities to create interesting designs and experiences.

### Talking
Turtles can talk by displaying messages on the screen. Make a new line, and add the following command:
```python
koopa.write("My name is Koopa")
```

Unfortunately, sometimes turtles cover their own messages! To move the message over, add some spaces at the beginning of the text.

### Turning and Moving
Turtles can change the direction they face by turning. They can turn either **left** or **right**. Use the following command on a new line to turn the turtle `90` degrees to the right so it faces down:
```python
koopa.right(90)
```

Turtles can also move across the canvas. If they move **forward**, they will travel in the direction they currently face. Use the following command on a new line to move the turtle down `75` pixels on the screen:
```python
koopa.forward(75)
```

## Turtle Graphics - Drawing and Storytelling
Using these three simple abilities (_talking_, _turning_, and _moving_) it is possible to tell stories and create images that illustrate those stories. Use Koopa to draw a picture of a musical quarter note while describing the drawing!

### Planning
Before writing code, developers usually spend time planning what they want to do from a broad perspective. This technique helps avoid problems, and provides a vision of the bigger picture.

Start by drawing a musical note on paper, or on a whiteboard. Koopa has already begun this drawing, so continue from there. A quarter note should look something like this:
```
         _
        | |
        | |
        | |
        | |
 _______| |
|         |
|         |
|_________|
```

Try to figure out which commands will be necessary to complete the drawing. While drawing on paper or on a whiteboard, notice the path of the writing utensil. Keep in mind how far the cursor travels across the Cartesian plane, the different positions, and the angles between each line. Each of these will relate to the code!

### Drawing the Base
First, have Koopa display a message and then continue down `75` for the base of the note:
```python
koopa.write(" I like to draw on my computer")
koopa.forward(75)
```

This will complete the right side of the base. Next, draw the bottom line. This will require Koopa to turn to the **right**  `90` degrees and move forward:
```python
koopa.right(90)
koopa.forward(100)
```

Next, start draw the left side of the base. The turtle should turn **right** `90` degrees to face upward, and then move forward `50` pixels.
```python
koopa.right(90)
koopa.forward(50)
```

At this point, Koopa should display a message to the user to continue the story:
```python
koopa.write(" I can draw anything!")
```

Finally, to complete the base, Koopa should continue up the left side and then turn to draw the top:
```python
koopa.forward(50)
koopa.right(90)
koopa.forward(85)
```

### Drawing the Stem
Complete the quarter note by drawing the stem. Koopa should turn **left** `90` degrees to face upward, then travel `150` pixels forward:
```python
koopa.left(90)
koopa.forward(150)
```

Next, to draw the top of the stem, Koopa should turn **right** `90` degrees and move `15` pixels to the right:
```python
koopa.right(90)
koopa.forward(15)
```

Koopa still has a couple of things to say! Use the **write** command to display a message saying "I like music" next to the turtle: 
```python
koopa.write(" I like music")
```

Now, all that's left is the right side of the quarter note. Turn Koopa to face downward, and move part of the way down:
```python
koopa.right(90)
koopa.forward(50)
```

Finally, Koopa should display a message saying "I can draw a quarter note!" and complete the drawing!
```python
koopa.write(" I can draw a quarter note!")
koopa.forward(90)
```

### Filling in the Drawing
It is also possible to fill in drawings, sort of like using a paint bucket tool. To do this, make Koopa use the `begin_fill` command before drawing, and the `end_fill` command when the drawing is complete. Make sure to place these commands in the proper place!

**Quarter Note Fill**
```python
koopa.begin_fill()

koopa.write(" My name is Koopa")
# ... code ...
koopa.write(" I can draw a quarter note!")
koopa.forward(90)

koopa.end_fill()
```

## Turtle Graphics - Multiple Turtles
So far, the program has used one sole turtle to carry out all of the commands. However, it is also possible to create more than one turtle, and each turtle can do different things! We can create a new turtle, and have it draw a **triangle**!

### Creating the turtle
Creating the _new_ turtle will be very similar to creating the original turtle. The only difference will be the name of the turtle (turtles are not allowed to have the same name in Python). Copy the commands used to create the `koopa` turtle, and update them to create a turtle named `shelly`. Add the following commands at the bottom of the `main.py` file:
```python
shelly = Turtle()
shelly.shape("turtle")
shelly.color("navy")
```

Run the program to see the new navy turtle appear at the end!

### Drawing the triangle
Shelly should draw three lines of equal length `100`, turning `120` degrees between each line. Add the following commands at the bottom of the `main.py` file:
```python
shelly.forward(100)
shelly.right(120)
shelly.forward(100)
shelly.right(120)
shelly.forward(100)
shelly.right(120)
```

Run the program to see Shelly draw the triangle!

### Changing the starting point
When running the current program, Shelly draws all over Koopa's good work! Fix this by moving Shelly before the triangle drawing begins. Two commands make this possible: `penup` and `goto`.

First, lift Shelly's pen before changing the position. This command should happen right after Shelly is created, before the triangle is drawn. This will prevent errant pen marks from messing up the canvas:
```python
shelly.penup()
```

Next, Shelly should move to a proper starting point on the screen. The top left corner will work well. Plotting this position on the Cartesian plane, the coordinates are `(-150, 150)`:
```python
shelly.goto(-150, 150)
```

Now, Shelly moves in a triangle at the right place, but there is still more to do! After moving, Shelly wants to provide a little introduction. Write a message to the screen saying " My name is Shelly... I like triangles" next to Shelly:
```python
shelly.write(" My name is Shelly... I like triangles")
```

Now, Shelly has to move out of the way of the message on the screen. Use `goto` to move the turtle down `10` pixels:
```python
shelly.goto(-150, 140)
```

Finally, Shelly has to put the pen back down in order to draw! Use `pendown` to accomplish this:
```python
shelly.pendown()
```

Now Shelly can properly draw a triangle without interfering with any of Koopa's artwork! Next, see how Shelly can draw the triangle more efficiently using Loops.

## Loops
Loops are a very powerful programming tool. They allow developers to repeat blocks of code automatically, without having to write the commands over and over again. One of the major benefits is that if the developer needs to change something, they only have to change it in one place!

In the turtle code, there is a block of commands that could be improved with loops. Where do those repetitive commands occur?

### Drawing the triangle
```python
shelly.forward(100)
shelly.right(120)
shelly.forward(100)
shelly.right(120)
shelly.forward(100)
shelly.right(120)
```

The two lines, `shelly.forward` and `shelly.right`, are repeated three times here. It takes up extra space in the file, and in order to update the program, each individual line would require update. For example, to make the triangle bigger, each `100` would have to change. Imagine if, instead of three times, the developer had to change three _hundred_ lines! Or, if the program needed to dynamically update the number of times to repeat the code, that would be impossible without loops.

### Looping the triangle
Use a `for` loop to automatically repeat the `forward` and `right` lines. Replace the triangle-drawing code with the following set of commands:
```python
for x in range(3):
    shelly.forward(100)
    shelly.right(120)
```

This will make the two lines repeat `3` times!

Note that the two lines are _indented_; this is how the loop knows which commands should repeat. The `for x in range()` part is the same for any number of repetitions; the `3` specifies that the loop should repeat four times.

With the use of loops, the file is shorter, and easier to maintain. Loops are one of the most important parts of programming!

## Final Code
```python
from turtle import *

koopa = Turtle()
koopa.shape("turtle")
koopa.color("green")

paper = koopa.getscreen()
paper.bgcolor("azure")

koopa.begin_fill()

koopa.write(" My name is Koopa")
koopa.right(90)
koopa.forward(75)

koopa.write(" I like to draw on my computer")
koopa.forward(75)

koopa.right(90)
koopa.forward(100)

koopa.right(90)
koopa.forward(50)

koopa.write(" I can draw anything!")
koopa.forward(50)

koopa.right(90)
koopa.forward(85)

koopa.left(90)
koopa.forward(150)

koopa.right(90)
koopa.forward(15)

koopa.write(" I like music")
koopa.right(90)
koopa.forward(50)

koopa.write(" I can draw a quarter note!")
koopa.forward(90)

koopa.end_fill()

shelly = Turtle()
shelly.shape("turtle")
shelly.color("navy")

shelly.penup()
shelly.goto(-150, 150)
shelly.write(" My name is Shelly... I like triangles")
shelly.goto(-150, 140)
shelly.pendown()

for x in range(3):
  shelly.forward(100)
  shelly.right(120)
```

## Turtle Challenges
After completing the follow-along activity, try some of the [challenges](TurtleChallenges.md)!