# Context Free

##  Who is this programming language for?
This program is for programmers who want to explore visualizations of 
context-free grammars and/or artists who want to create drawings composed 
of specific patterns.

## What is easy to do in this language? Why is it easy?
Drawing objects that can be seen as a pattern of smaller, equivalent 
objects is easy to do in this language. 

Context free grammar describes how symbols can be substituted for a 
collection of other symbols ordered in a specific way. This Context Free language 
works in the same way, substituting “symbols” for several basic “objects” 
in the previous sentence. A concrete example would be that a hexagon can be thought
of as a collection of 6 equilateral triangles ordered in a honeycomb fashion.

An additional note on the language's ease to draw in general: Unliked its host
language - mostly C++ - compiling and generating an image in Context Free takes one
click of the render button. Doing the same in C++ requires a lot more command line knowledge.

## What is hard to do in this language? Why is it hard?
Any sort of “free hand” drawing involving few repeated parts is difficult because 
manipulations like translation or rotation are relative to some other shape 
with nuances to which manipulations get applied first. This means that programmers 
cannot easily leverage primitive shapes offered by the language, and will need to 
draw lines (ex. path declarations) knowing specific 
coordinates/magnitudes and connecting these lines to create a free-hand shape.

Since manipulations can be done in different orderings, programmers would also need to be 
careful about manipulations between complex shapes (shapes made of many other shapes)
when running a program if there is a specific intended spacing.

## How did you learn how to program in this language?
I followed instructions on the 
[“How do I get started” page](https://github.com/MtnViewJohn/context-free/wiki/About#how-do-i-get-started)
, and then looked through the [GitHub wiki documentation](https://github.com/MtnViewJohn/context-free/wiki)
for more info about specific parts of Context Free programs. 
I then attempted to do some free-hand primitive shapes with different transforms 
before tackling recursion/weighing options/colors. I also explored the 
[forums](https://www.contextfreeart.org/phpbb/viewforum.php?f=2) for inspiration.

## What is the underlying _computational model_ for this programming language? 
The ContextFree program starts with the name of a shape indicated by the word after “startshape”. 
For each rule that is read, the program will draw the rule if it is a primitive shape 
(square, circle, triangle). Otherwise, save the instructions on manipulating the shape, 
and find the list of shape rules that makes up the shape, until a primitive shape is found. 
The sequence of saved instructions will then be drawn with reference to the primitive shape. 
The program finish when all shape instructions saved are drawn or when drawing 
additional shapes is too small to be seen.

## What do you think is interesting about the ContextFree program you wrote?
Since the documentation was a bit vague on what it meant by “too small to see”, I wanted to 
create a program that could “break” - a program that runs for a relatively long time with 
little visual difference as it runs. 

For my program, I had 2 complex shapes - version 1 is a curve made of circles, and version 2 
a curve made of alternating triangles and squares. Drawings made with weight of version 1 
greater than weight of version 2 tends to be less random. Additionally, as the weight of 
version 1 become significantly higher than version 2, the longer the program runs even though it 
quickly converged on a shape that doesn’t seem to change.
