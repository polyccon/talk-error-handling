slide 1

Welcome to the error-handling 1.0. This is a brief introduction to error Handling, introducing the concepts in the workshop that you will do following this presentation. The exercise has been recently revised but not thoroughly tested, so should you notice anything that might be off be sure to let us know.
---------------
slide 2

So I've been sent here from upstairs to deliver this message: You need to handle your errors!
But don't worry if you don't know what I'm talking about as after this workshop you will have an understanding of:

---------------
slide 3

what are errors

---------------
slide 4

and a vague idea of how to handle them

---------------
slide 5

So.. what kind of errors are there?
Broadly speaking, there are 2 main categories:

----------------
slide 6

1. Programmer errors: these are bugs, something you did wrong when you were writing your code (for example a syntax error) and with programmer errors your application won't run.

----------------
slide 7

2. Operational errors: these are usually runtime errors, which means that your code will run, but something else went wrong

----------------
slide 8

aaaand:
3. Custom errors: I took an initiative to add my own category here, because today we will learn how to throw our own errors!

-----------------
slide 9

These are some common sub-categories for errors that JavaScript provides but we will make our own ones

-----------------
slide 10

waiddasecond!

CUSTOM? Why on earth would you throw your OWN ERROR?

-----------------
slide 11

Doesn't that make your programme **less** likely to work?

-----------------
slide 12

The answer is because JavaScript!

------------------
slide 13

So hold that thought, and we will have a little JavaScript conversation now.
What do we expect as an output in the console when we type the following ?

```console.log( 1 + "2" + "2" );```

------------------
slide 14

So JavaScript will see the string "2" following number 1 and will concatenate them into strings.
The answer is "122"

------------------
slide 15

what about this one?

```console.log( +"1" + "1" + "2" );```
Start reading it from the left to right and think about what will happen, with only the first two and forget about the third element.

-------------------
slide 16

the first plus will convert the "1" string to a number and then when it sees the second "1" it will convert both to strings.
The answer is "112"

-------------------
