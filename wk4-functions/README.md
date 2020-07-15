## `FUNCTIONS`
A function is a way to bundle code so that it can be
reused. Functions allow us to run the same piece of
code from multiple places in a program without having to copy and paste the code repeatedly. Also, by
hiding long bits of code in a function and giving it
an easy-to-understand name, you’ll be better able to
plan out your code because you can focus on organizing your functions rather than all of the little code 

## `CREATING A SIMPLE FUNCTION`
Let’s create a simple function that prints Hello world!. Enter the
following code in the browser console. 

var ourFirstFunction = function () {
 console.log("Hello world!");
};

To run the function we just created (code inside a function "the
function body' ), we need to call the function. To call a function, you enter its
name followed by a pair of opening and
closing parentheses.

ourFirstFunction();
Hello world!

Calling ourFirstFunction executes the body of the function,
which is console.log("Hello world!");, and the text we asked to be
printed is displayed on the next line: Hello world!.


But if you call this function in your browser, you’ll notice that
there’s a third line, with a little left-facing arrow, as shown in
This is the return value of the function.

## `EXERCISE`
Build a random word generator