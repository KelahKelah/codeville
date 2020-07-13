## `NAMING VARIABLES`
Be careful with your variable names, because it’s easy to misspell
them. Even if you just get the capitalization wrong, the JavaScript
interpreter won’t know what you mean! For example, if you accidentally used a lowercase c in numberOfCandies, you’d get an error:
numberOfcandies / numberOfSiblings;
ReferenceError: numberOfcandies is not defined
Unfortunately, JavaScript will only do exactly what you ask it
to do.

## `JavaScript lets you perform basic mathematical operations like`
addition, subtraction, multiplication, and division. To make these
calculations, we use the symbols 
+,
 -, 
 *, 
  /, which are called
operators.
You can use the JavaScript console just like a calculator. 

Check some calculations on the console 

REASSIGNING VARIABLES 
avaScript lets you reassign variables 
var lastName = "Kelechi";
console.log(firstName)

lastName = "okonkwo"; 


## `INCREMENTING AND DECREMENTING`
In JavaScript you’ll often need to increase or decrease the
value of a variable containing a number by 1. For example, you
might have a variable that counts the number of high-fives you
received today. Each time someone high-fives you, you’d want to
increase that variable by 1.
Increasing by 1 is called incrementing, and decreasing by 1 is
called decrementing. You increment and decrement using the operators ++ and --.
var highFives = 0;
++highFives;
1
++highFives;
2
--highFives;
1
When we use the ++ operator, the value of highFives goes up by 1,
and when we use the -- operator, it goes down by 1.


+= (plus-equals) and
–= (minus-equals)
To increase the value of a variable by a certain amount, you could
use this code:
var x = 10;
x = x + 5;
x;
15
Here, we start out with a variable called x, set to 10. Then, we
assign x + 5 to x. Because x was 10, x + 5 will be 15. What we’re
doing here is using the old value of x to work out a new value for x.
Therefore, x = x + 5 really means “add 5 to x.” Same princeple applies to - -->
<!-- 
DATA TYPE AND VARIABLES
Strings, Booleans and number

## STRINGS
Stringns and sequence of characters surrounded by quotes. It could contain number or symbols
var aString = 'i am a string number 1!'
 CHECKING LENGHT OF STRING 
 var stringLenght = aString.lenght
 ASSESSING A STRING 
 var getChar = aString[4]

 Todays game with strings 

 Todays exercise will be getting a clue which will be our secret word to access a hunted house
 
 var word1 = 'What is Trust';
 var word2 = 'We coulds ee';
 var word3 = 'Lenght';
 var word4 = '!?';

 var secretWorld = word1[9] + word2[5] + word3[2] + word4[0]
console.log(secretWorld) 

## NUMBERS 

## BOOLEANS
Now for Booleans. A Boolean value is simply a value that’s either
true or false. For example, here’s a simple Boolean expression.
var javascriptIsCool = true;
javascriptIsCool;
true 




## `UNDEFINED AND NULL`
Finally, we have two values that don’t fit any particular mold.
They’re called undefined and null. They’re both used to mean
“nothing,” but in slightly different ways.
undefined is the value JavaScript uses when it doesn’t have a
value for something. For example, when you create a new variable,
if you don’t set its value to anything using the = operator, its value
will be set to undefined:
var myVariable;
myVariable;
undefined


The null value is usually used when you want to deliberately
say “This is empty.”
var myNullVariable = null;
myNullVariable;
null
At this point, you won’t be using undefined or null very often.
You’ll see undefined if you create a variable and don’t set its value,
because undefined is what JavaScript will always give you when
it doesn’t have a value. It’s not very common to set something to
undefined; if you feel the need to set a variable to “nothing,” you
should use null instead.
null is used only when you actually want to say something’s
not there, which is very occasionally helpful. For example, say
you’re using a variable to track what your favorite vegetable is.
If you hate all vegetables and don’t have a favorite, you might set
the favorite vegetable variable to null.
Setting the variable to null would make it obvious to anyone
reading the code that you don’t have a favorite vegetable. If it were
undefined, however, someone might just think you hadn’t gotten
around to setting a value yet 