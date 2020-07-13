ARRAYS  
Numbers and strings are kind of boring. There’s not a lot that you can do with a string on its own. JavaScript lets you create and group together
data in more interesting ways with arrays. An array is just a list of other JavaScript data values. 

For example, if your friend asked you what your favorite dinosaurs were, you could create an array with the names of
those dinosaurs, in order:
var myDinosaurs = ["T-Rex", "Velociraptor", "Stegosaurus", "Triceratops", "Brachiosaurus", "Pteranodon", "Apatosaurus", "Diplodocus","Compsogna];
So instead of giving your friend three separate strings, you
can just use the single array myDinosaurs.

To create an array, you just use square brackets, []. 
In fact, an empty array is simply a pair of square brackets, like this:
[];
[]

To create an array with values in it, enter the values, separated by commas, between the square brackets. We can call the
individual values in an array items or elements. In this example,
our elements will be strings (the names of our favorite dinosaurs),
so we’ll write them with quote marks. We’ll store the array in a
variable called dinosaurs:
var dinosaurs = ["T-Rex", "Velociraptor", "Stegosaurus", "Triceratops", "Brachiosaurus", "Pteranodon", "Apatosaurus", "Diplodocus", "Compsognathus"];


ACCESSING AN ARRAYS ELEMENT
When it’s time to access elements in an array, you use square
brackets with the index of the element you want, as you can see
in the following example:
dinosaurs[0];
"T-Rex"
dinosaurs[3];
"Triceratops"

An index is the number that corresponds to (or matches) the
spot in the array where a value is stored. Just as with strings, the
first element in an array is at index 0, the second is at index 1,
the third at index 2, and so on. That’s when you ask for index 0
from the dinosaurs array returns "T-Rex" (which is first in the list),
and index 3 returns "Triceratops" (which is fourth in the list). 
Arrays 43

It’s useful to be able to access individual elements from an
array. For example, if you just wanted to show someone your absolute favorite dinosaur, you wouldn’t need the whole dinosaurs array.
Instead you would just want the first element:
dinosaurs[0];
"T-Rex"
Setting or Changing Element


FINDING THE LENGTH OF AN ARRAY
Sometimes it’s useful to know how many elements there are in
an array. For example, if you kept adding dinosaurs to your dinosaurs
array, you might forget how many dinosaurs you have.
The length property of an array tells you how many elements
there are in the array. To find the length of an array, just add
.length to the end of its name. Let’s try it out. First we’ll make a
new array with three elements:
var maniacs = ["Yakko", "Wakko", "Dot"];
maniacs[0];
"Yakko"
maniacs[1];
"Wakko"
maniacs[2];
"Dot"
To find the length of the array, add .length to maniacs:
maniacs.length;
3
JavaScript tells us that there are 3 elements in the array, and
we already know they have the index positions 0, 1, and 2. This
gives us a useful piece of information: the last index in an array is
always the same number as the length of the array minus 1. This
means that there is an easy way to access the last element in an
array, however long that array is:
maniacs[maniacs.length - 1];
"Dot"

ADDING ELEMENTS TO ARRAY
To add an element to the end of an array, you can use the push
method. Add .push to the array name, followed by the element you
want to add inside parentheses, like this:
var animals = [];
animals.push("Cat");
1
animals.push("Dog");
2
animals.push("Llama");
3
animals;
["Cat", "Dog", "Llama"]
animals.length;
3 -->
.pop() simply add a new element to the end of the array and returns the new length of the array

REMOVING AN ELEMENT IN AN ARRAY
To remove and element from an array, you use the .pop()
method. The .pop()
 would usually remove the last element in an array and return that particular array

CLASS EXERCISE

Creating a Random Insult Generator
We can extend the decision maker example to create a program
that generates a random insult every time you run it!
var randomBodyParts = ["Face", "Nose", "Hair"];
var randomAdjectives = ["Smelly", "Boring", "Stupid"];
var randomWords = ["Fly", "Marmot", "Stick", "Monkey", "Rat"];
// Pick a random body part from the randomBodyParts array:
u var randomBodyPart = randomBodyParts[Math.floor(Math.random() * 3)];
// Pick a random adjective from the randomAdjectives array:
v var randomAdjective = randomAdjectives[Math.floor(Math.random() * 3)];
// Pick a random word from the randomWords array:
w var randomWord = randomWords[Math.floor(Math.random() * 5)];
// Join all the random strings into a sentence:
var randomInsult = "Your " + randomBodyPart + " is like a " + 
randomAdjective + " " + randomWord + "!!!";
randomInsult;
"Your Nose is like a Stupid Marmot!!!" 


OBJECTS
Objects in JavaScript are very similar to arrays, but
objects use strings instead of numbers to access the
different elements. The strings are called keys or
properties, and the elements they point to are called
values. Together these pieces of information are called
key-value pairs. While arrays are mostly used to
represent lists of multiple things, objects are often

In the previous session  we made several arrays
that listed different animal names. But what if we wanted to
store different pieces of information about one animal?

Creating Objects
We could store lots of information about a single animal by creating a JavaScript object. Here’s an object that stores information
about a three-legged cat named mickey.
var cat = {
 legs: 4,
 name: "mickey",
 color: "grey"
};
Here we create a variable called cat
and assign an object to it with three keyvalue pairs. To create an object, we use
curly brackets, {}, instead of the straight
brackets we used to make arrays. In
between the curly brackets, we enter
key-value pairs. The curly brackets and
everything in between them are called
an object literal. An object literal is a
way of creating an object by writing out
the entire object at once.

Note We’ve also seen array literals (for example, ["a", "b", "c"]), number
literals (for example, 37), string literals (for example, "moose"), and
Boolean literals (true and false). Literal just means that the whole
value is written out at once, not built up in multiple steps.

For example, if you wanted to make an array with the numbers
1 through 3 in it, you could use the array literal [1, 2, 3]. Or you
could create an empty array and then use the push method to add 1,
2, and 3 to the array. You don’t always know at first what’s going to
be in your array or object, which is why you can’t always use literals
to build arrays and objects.

When you create an object, the
key goes before the colon (:), and
the value goes after. The colon acts
a bit like an equal sign—the values
on the right get assigned to the
names on the left, just like when
you create variables. In between
each key-value pair, you have to
put a comma but you don’t need a comma after the last keyvalue pair (color: "grey"). Because it’s the last key-value
pair, the closing curly bracket comes next, instead of a comma.
Keys Without Quotes

Notice that we didnt put quotes around the keys. JavaScript knows that the keys will always be strings, which
is why you can leave out the quotes. If you don’t put quotes around
the keys, the unquoted keys have to follow the same rules as variable names: spaces aren’t allowed in an unquoted key, for example.
If you put the key in quotes, then spaces are allowed:
var cat = {
 legs: 3,
 "full name": "Harmony Philomena Snuggly-Pants Morgan",
 color: "Tortoiseshell"
}; 

ACCESSING AN OBJECT 
You can access values in objects using square brackets, just like
with arrays. The only difference is that instead of the index (a
number), you use the key (a string).
cat["name"];
"Harmony"
Just as the quotes around keys are optional when you create
an object literal, the quotes are also optional when you are accessing keys in objects. If you’re not going to use quotes, however, the
code looks a bit different:
cat.name;
"Harmony"
This style is called dot notation. Instead of typing the key
name in quotes inside square brackets after the object name, we
just use a period, followed by the key, without any quotes. As with
unquoted keys in object literals, this will work only if the key
doesn’t contain any special characters, such as spaces.
Objects 67
Instead of looking up a value by typing its key, say you wanted
to get a list of all the keys in an object. JavaScript gives you an
easy way to do that, using Object.keys():
var dog = { name: "Pancake", age: 6, color: "white", bark: "Yip yap 
yip!" };
var cat = { name: "Harmony", age: 8, color: "tortoiseshell" };
Object.keys(dog);
["name", "age", "color", "bark"]
Object.keys(cat);
["name", "age", "color"]



CLASS EXERCISE 
Keeping Track of Owed Money
Let’s say you’ve decided to start a bank. You lend your friends
money, and you want to have a way to keep track of how much
money each of them owes you.

You can use an object as a way of linking a string and a value
together. In this case, the string would be your friend’s name, and
the value would be the amount of money he or she owes you. Let’s
have a look.
var owedMoney = {};
owedMoney["Jimmy"] = 5;
owedMoney["Anna"] = 7;
owedMoney["Jimmy"];
5
y owedMoney["Jinen"];
undefined
At u, we create a new empty
object called owedMoney. At v, we
assign the value 5 to the key "Jimmy".
We do the same thing at w, assigning the value 7 to the key "Anna".
At x, we ask for the value associated with the key "Jimmy", which
is 5. Then at y, we ask for the value
associated with the key "Jinen",
which is undefined because we didn’t
set it.
Now let’s imagine that Jimmy
borrows some more money (say, $3).
We can update our object and add 3
to the amount Jimmy owes with the
plus-equals operator (+=) that you
saw in Chapter 2.
owedMoney["Jimmy"] += 3;
owedMoney["Jimmy"];
8
This is like saying owedMoney["Jimmy"] = owedMoney["Jimmy"] + 3.
We can also look at the entire object to see how much money each
friend owes us:
owedMoney;
{ Jimmy: 8, Anna: 7 }
