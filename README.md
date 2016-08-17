# Introduction to JavaScript

### Learning Objectives
***Students will be able to...***

* Declare a variable in JavaScript
* Iterate through JS data structures
* Store JS data types in Objects
* Use Control Flow in JS

---

### What You Need For This Workshop

* Just your brain and something to take notes on. 
* You will have access to this lesson plan after you leave. 

---

### Lesson

##### Part 1 - A brief history. Why is JavaScript so important?

***The Beginning***

* ***`DO NOT`*** confuse this with **Java**
* JavaScript was created in 10 days in 1995 by Brendan Eich who was working at Netscape at the time.
* It was standardized by ECMA (European Computer Manufacturers Association) in 1996. 
* JavaScript is the only language that can interact with your browser. Sometimes it gets a bad reputation because the browser is difficult to control.
* JavaScript is one of the three main languages used for Front End Programming. The other two being HTML and CSS 
	* `Front End Programming` - How to build the User Interface of a website. 
		* What are the colors of the website
		* How is the website laid out
		* How does the user interact with the website
		* What will happen if a user clicks something
		* How do we render data to the browser

***2009 And Beyond***

* It was not until recently JavaScript could be used as a backend language
	* `Back End Programming` - 	How to build a server and store data
		* Build the different urls a person can visit on your website
		* Organize a users information for storage
		* Serve that information to the browser for the user to render
* This occured with the emergence of `Node.js`. A runtime environment that allows programmers to build server-side applications in JavaScript
* JavaScript has gained a lot of popularity in recent years as it is convenient to build a full web application, the front and back, in the same language
* No matter what language you are going to build your server in, whether it's `PHP`, `Ruby`, `Python`, or even `Node.js`, you will always need JavaScript to render things in your browser

---

#### Part 2 - Variables / Assignment / Comparison

* `Variables` are a core concept of programming. We use them to store data for repeated use. 
* A `variable` is our way of naming a value. You can think of it as a storage container. All we're doing is sticking a label on this storage container. What goes inside this storage container is a value.
* A `value` can be any form of data. We will `assign` this value to a variable using ONE equal sign. 
* Below is an example of `declaring` a `variable` and `assigning` a `value` to that variable

```
var actor = "Tom Cruise";

var favoriteNumber = 1000;
```
* Declaring a variable
	* Begin with the keyword `var`
	* Follow `var` with the name of your variable. Try to keep this as accurate as possible to the value it will be tied to
	* If the name has two or more words we write it in camelCase(favoriteNumber). 
	* One equal sign for `assignment`
	* Followed by the value you are assigning to the variable. 
	* Complete with a semi-colon. This tells JavaScript you're finished with that line
* We can also use three equal signs to compare things and see if they are equal or not. Using three equal signs will return to us either `true` or `false`
* The below example will return to us false

```
actor === favoriteNumber
```

---

#### Part 3 - DataTypes / DataStructures

* Now that we know how to `assign` `data/values` to `variables` lets take a look at the different types of data

***Booleans***

* This is a data type that only has two options. `true` or `false`

```
var areYouAlive = true;

var dayTime = false;
```

***Numbers***

* Numbers are just that, numbers 
* They could be whole numbers or with decimals
* You can also perform math operations on numbers

```
var firstNum = 10
var secondNum = 20

var sum = firstNum + secondNum
```
* sum is now equal to 30
* Any math operations follows PEMDAS
	* Parenthesis
	* Exponent
	* Multiplication
	* Division
	* Addition
	* Subtraction

***Strings***

* Strings are any characters surrounded by quotes

```
var a = "Hello";
var b = "World";
```
* If a number is wrapped in quotes it is not considered a number but a string

```
var favoriteNumber = "1000"
```
* We can also combine two or more strings to make a brand new one. This is called String Concatenation
* We can `concatenate` strings using the `+` or a `comma`

```
var a = "Hello";
var b = "World";

console.log(a + " " + b)

console.log(a,b)
```
* `console.log` is a function in JS that allows us to show things in our terminal. We'll talk more about functions later.

***Arrays***

* `Arrays` are a DataType and also a DataStructure
* They are a type of data that can be `assigned` to a variable
* They are also a `data structure` than can hold multiple values

```
var movies = ["Top Gun", "RoadHouse", "Pitch Perfect"];
```
* They can also hold various types of data

```
var randomThings = [88, true, "my string"];
```
* Arrays are written with square brackets
* The values inside an array can be targeted with `indexes`
* All the values in an array have an `index`, they start at 0 and increase by one
* Lets try to grab some values from the previous examples

```
var movies = ["Top Gun", "RoadHouse", "Pitch Perfect"];

var randomThings = [88, true, "my string"];

console.log(movies[0]); === "Top Gun"
console.log(randomThings[0]); === 88
console.log(movies[2]); === "Pitch Perfect"
```

---

#### Part 4 - Control Flow / Loops

***Control Flow***

* JavaScript also offers us the use of the `if/else` statement. 
* The syntax is as follows

```
if (if this condition is true){
	do this
} else if (if this condition is true){
	do this
} else {
	do this
};
```
* Here's an example below:

```
var deadpool = "Wade Wilson";

if (deadpool === "James Howlett"){
	console.log("Hey you're Wolverine");
} else if (deadpool === "Wade Wilson"){
	console.log("Here are your chimichangas");
} else {
	console.log("You're not a super hero!")
};
```
* We declared a variable
* Assigned that variable a value of "Wade Wilson"
* Began an `if` statement
* It used three equal signs to evaluate a condition
* It returned false to us
* Jump to the next `else if` statement
* That condition is true
* Run the console.log "Here are you chimichangas"
* Finished

***Loops***

* Loops are used to continuously repeat a block of code while something is true
* The for loop in JS is written with the below syntax

```
for (declare a counter; declare a condition; increment your counter){
	run this code
}
```
* Here's an example below:

```
var animals = ["dog", "cat", "bird", "turtle", "fish", "hamster", "lizard"];

for (var i = 0; i < animals.length-1; i++){
    console.log(animals[i])
};

"dog"
"cat"
"bird"
"turtle"
"fish"
"hamster"
"lizard"
```
* `var i = 0` is creating a variable called i that will start at zero
* `i < animals.length-1` - as long as this returns `true` the code in between the curly brackets will run
* `i++` this will increment i after every loop iteration

---

#### Part 4 - JS Syntax Control Flow / Iteration

***Function Syntax***

* Functions are reusable blocks of code. 
* There are three ways to declare functions in JavaScript. 

```
function helloWorld(){
	console.log("Hello");
};

var helloWorld = function helloWorld(){
	console.log("Hello");
};

var helloWorld = function(){
	console.log("Hello");
};
```
* For this course we will be sticking with the last example of function declaration. This is because we want to be safe from `hoisting` bugs. You can google this on your free time if you'd like
* Remember all your JS syntax will end with a semi colon
* Function code blocks are put in between curly brackets `{}`
* Functions can also take in values which allows them to be more dynamic
* Take the below example:

```
var add = function(x,y){
	console.log(x + y)
}

add(5,2) === 7

add(9,12) === 21

add(4,8) === 12
```
* The `x,y` inside of the function parenthesis are called `parameters`
* `Parameters` are like nicknames we give for the values we expect somebody to enter when they `invoke` or `call` our function
* The last three `add` calls are our way of saying `now run the code in that function`. This is `invoking`
* The numbers that are entered with invoking that function are called `arguments` 






