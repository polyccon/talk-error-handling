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

The first plus will convert the "1" string to a number and then when it sees the second "1" it will convert both to strings.
The answer is "112"

-------------------
slide 17

what about this ? Will this throw an error?
```console.log( "A" - "B" + "2" );```
So we are "minusing" 2 strings here, is that possible?

-------------------
slide 18

So since "minusing" isn't possible with strings, JavaScript converts the 2 stings into numbers and that gives us NaN which is then converted to a string because of "2" that follows.
The answer is "NaN2"

-------------------
slide 19

what about this?
```console.log( "A" - "B" + 2 );```

-------------------
slide 20

so like the previous example, we have NaN plus 2 what does that give us?
Answer is ```NaN```

-------------------
slide 21

Last example which you will also read about in the readme, what about this? will this throw an error?
```console.log( {number: 6} + 10 );```

-------------------
slide 22

As you cannot add an object and a number, JavaScript will convert both to strings:
```[object object]10```
The conclusion is, that JavaScript will not throw an error in any of those examples.

--------------------
slide 23

So, let's say in a real life web application senario, when would we have an unexpected data type conversion?

(user input, web APIs)
That is the situation in which we are interested in, data coming from somewhere that we dont have any control of, that we need to have an error handling strategy.

----------------------
slide 24 -34

1) The general princiles are:
2) Assume your code will fail
3) Handle your errors!
4) Identify where errors might occur
5) Throw your own errors: do so in the low levels of the application
6) Handle your errors!
7) Be consistent not ad hoc
8) Handle your errors!
9) Deal with the errors at the highest level of the application as possible
10) HANDLE YOUR ERRORS!

------------------------
slide 35

So. What approaches are there to error handling?

1) Throw and catch
2) Return an error to the caller
3) Error first callbacks

-------------------------
slide 36

and what are those? Great news I have this thing for you to read!
