## `CONDITIONALS`
There are two forms of conditional statements in JavaScript: if
statements and if...else statements. An if statement is used to
execute a piece of code if something is true. For example, if you’ve
been good, you get a treat. An if...else statement executes one
piece of code if something is true and another if not. For example,
if you’ve been good, you get a treat; else, you get grounded.

## `IF STATEMENT`
The if statement is the simplest of JavaScript’s control structures.
It’s used to run code only if a condition is true. Return to your 
92 Chapter 6
HTML file and replace the two lines inside the script element
with this:
u var name = "Nicholas";
v console.log("Hello " + name);
w if (name.length > 7) {
x console.log("Wow, you have a REALLY long name!");
}

## `IF...ELSE STATEMENT`
As I said before, an if statement will execute its body only if the
condition is true. If you want something else to happen when
the condition is false, you need to use an if...else statement.
Let’s extend the example from earlier:
var name = "Nicholas";
console.log("Hello " + name);
if (name.length > 7) {
 console.log("Wow, you have a REALLY long name!");
} else {
 console.log("Your name isn't very long.");relative
}               

## `CHAINING OF IF...ELSE STATEMENT`
Often we need to check a sequence of conditions and do something
when one of them is true. For example, say you’re ordering Chinese
food and you’re choosing what to eat. Your favorite Chinese dish
is lemon chicken, so you’ll have that if it’s on the menu. If it’s
not, you’ll have beef with black bean sauce. If that’s not on the
menu, you’ll have sweet and sour pork. In the rare case that none
of those options is available, you’ll have egg fried rice, because you
know all the Chinese restaurants you go to will have that.
var lemonChicken = false;
var beefWithBlackBean = true;
var sweetAndSourPork = true;
if (lemonChicken) {
 console.log("Great! I'm having lemon chicken!");
} else if (beefWithBlackBean) {
 console.log("I'm having the beef.");
} else if (sweetAndSourPork) {
 console.log("OK, I'll have the pork.");
} else {
 console.log("Well, I guess I'll have rice then.");
}
To create a chain of if...else statements, start with a normal if statement and, after the closing brace of its body, enter the
keywords else if, followed by another condition and another body.
You can keep doing this until you run out of conditions; there’s no 
Conditionals and Loops 95
limit to the number of conditions. The final else section will run if
none of the conditions is true. Figure 6-3 shows a generic chain of
if...else statements.
if (condition1) {
console.log("Do this if condition 1 is true");
} else if (condition2) {
console.log("Do this if condition 2 is true");
} else if (condition3) {
console.log("Do this if condition 3 is true");
} else {
console.log("Do this otherwise");
}
Each condition has code to run
if the condition is true.
Some code to run
if all the conditions are fal


## `LOOPS`
As we’ve seen, conditionals allow you to run a piece of code
once if a condition is true. Loops, on the other hand, allow you to
run a piece of code multiple times, depending on whether a condition remains true. For example,
while there’s food on your plate,
you should keep eating; or,
while you still have dirt on your
face, you should keep washing.

## WHILE LOOPS
The simplest kind of loop is a while loop. A while loop repeatedly
executes its body until a particular condition stops being true. By
writing a while loop, you are saying, “Keep doing this while this
condition is true. Stop when the condition becomes false.”
As Figure 6-4 shows, while loops start with the while keyword, followed by a condition in parentheses and then a body
in braces.
while (condition) {
console.log("Do something");
 i++;
} Some code to run and repeat
as long as the condition is true
(something in here should change things
so the condition is eventually false)
This condition is checked
each time the loop repeats.
Figure 6-4: The general structure of a while loop
Like an if statement, the body of a while loop is executed if the
condition is true. Unlike an if statement, after the body is executed,
the condition is checked again, and if it’s still true, the body runs
again. This cycle goes on until the condition is false.
Counting Sheep with a while Loop
Say you’re having trouble sleeping and you want to count sheep.
But you’re a programmer, so why not write a program to count
sheep for you?
var sheepCounted = 0;
u while (sheepCounted < 10) {
v console.log("I have counted " + sheepCounted + " sheep!");
 sheepCounted++;
}
console.log("Zzzzzzzzzzz");
98 Chapter 6
We create a variable called sheepCounted and set its value
to 0. When we reach the while loop u, we check to see whether
sheepCounted is less than 10. Because 0 is less than 10, the code
inside the braces (the body of the loop) v runs, and "I have
counted " + sheepCounted + " sheep!" is logged as “I have counted
0 sheep!” Next, sheepCounted++ adds 1 to the value of sheepCounted,
and we go back to the start of the loop, over and over:
I have counted 0 sheep!
I have counted 1 sheep!
I have counted 2 sheep!
I have counted 3 sheep!
I have counted 4 sheep!
I have counted 5 sheep!
I have counted 6 sheep!
I have counted 7 sheep!
I have counted 8 sheep!
I have counted 9 sheep!
Zzzzzzzzzzz
This repeats until sheepCounted becomes 10, at which point the
condition becomes false (10 is not less than 10), and the program
moves on to whatever comes after the loop. In this case, it prints
Zzzzzzzzzzz.


## `FOR LOOPS`
for loops make it easier to write loops that create a variable, loop
until a condition is true, and update the variable at the end of
each turn around the loop. When setting up a for loop, you create
a variable, specify the condition, and say how the variable should
change after each cycle—all before you reach the body of the loop.
For example, here’s how we could use a for loop to count sheep:
for (var sheepCounted = 0; sheepCounted < 10; sheepCounted++) {
 console.log("I have counted " + sheepCounted + " sheep!");
}
console.log("Zzzzzzzzzzz");
As Figure 6-5 shows, there are three parts to this for loop,
separated by semicolons: the setup, condition, and increment.
for (setup; condition; increment) {
console.log("Do something");
}
Some code to run
as long as the
condition is true
Something that is
either true or false
This code runs
before the loop starts.
Something to run
after each repetition
of the loop body
Figure 6-5: The general structure of a for loop
The setup (var sheepCounted = 0) is run before the loop starts.
It’s generally used to create a variable to track the number of times
the loop has run. Here we create the variable sheepCounted with an
initial value of 0.
The condition (sheepCounted < 10) is checked before each run
of the loop body. If the condition is true, the body is executed;
if it’s false, the loop stops. In this case, the loop will stop once
sheepCounted is no longer less than 10.
The increment (sheepCounted++) is run after every execution of
the loop body. It’s generally used to update the looping variable.
Here, we use it to add 1 to sheepCounted each time the loop runs.
100 Chapter 6
for loops are often used to do something a set number of times.
For example, this program will say Hello! three times.
var timesToSayHello = 3;
for (var i = 0; i < timesToSayHello; i++) {
 console.log("Hello!");
}
Here is the output:
Hello!
Hello!
Hello!
If we were the JavaScript interpreter running this code, we
would first create a variable called timesToSayHello and set it to
3. When we reach the for loop, we run the setup, which creates a
variable i and sets it to 0. Next, we check the condition. Because
i is equal to 0 and timesToSayHello is 3, the condition is true, so we
enter the loop body, which simply outputs the string "Hello!". We
then run the increment, which increases i to 1.
Now we check the condition again. It’s still true, so we run
the body and increment again. This happens repeatedly until i is
equal to 3. At this point, the condition is false (3 is not less than 3),
so we exit the loop. 

## ASSIGNMENT
Read up about switch 

## `EXERCISE`

Building a  grading system Using conditionals
Building a multiplication table using a loops
