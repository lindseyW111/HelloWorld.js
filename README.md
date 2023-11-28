# JavaScript CS-330
## History
  Invented in 1995 by Brendan Eich, it took Eich 10 days to write the program. The programming language was designed to aid Netscape's communication’s flagship web browser, as a scripting language. In 1997 it was handed to ECMA.  It is important to note that java and javascript are in no way related. After the release other companies started using the program. Sadly in its infancy the program had security and performance issues. But Javascript took a turn in 2008 when Chrome V8, Google's open source, was able to use Javascript as a high performance engine. 
## Getting Started on Mac
1. Download [VSCode](https://code.visualstudio.com/download) for Mac
2. On VSCode download the extension JavaScript (ES6) Code Snippet.
3. Next you have to download [Node.js](https://nodejs.org/en) for Mac.
4. This will then allow you to run JavaScropt on VSCode.

## Hello World Program
This is the code to run Hello World in JavaScript

Input:

    console.log('Hello World!')
   

Output:

     // Two forward slashes is how you comment
    //  The code above outputs this into the terminal 
   
    Hello World!

## Naming

JavaScript is a dynamically typed language, and weakly typed.  Variable names must start with a letter underscore _ or the dollar sign $ and they cannot include spaces. It is also standard practice to name variables with camelCase, and have spaces around operators and commas. Also to use code indentions (2 spaces) when writing code blocks (everything except the first line of the block is indentented). While simple samples end in semicolons. 

#### Mutable vs immutable 
There are only two mutable variables in JavaScript Arrays and Objects.
#### Limitations
1. Does not do multi threading
2. Can not do big numbers
3. Lack of reading and writing capabilities on the client side.
4. Limitations of networking.

## Keywords
There are 63 keywords in JavaScript.

abstract	| arguments |	boolean |	break |	byte |	case |	catch | char |	const
--- | --- | --- | --- |--- |--- |--- |--- |--- 
continue |	class* |	debugger |	default |	delete |	do |	double |	else |	eval
enum* |	export* |	extends* |	false |	final |	finally |	float |	for |	function
goto | if |	implements | in |	instanceof |	int |	interface |	import* |	let
long |	native | new |	null |	package |	private |	protected |	public |	return
short|	static | switch |	synchronized |	super* |	this |	throw |	throws | transient
true | try | typeof | var| void | Volatile | while | with | Yield

### Arthmetic Operators

Addition | +
  --- | --- 
Subtraction | -
Multiplication | *
Exponentiation | **
Division | /
Modulus | %
Increment |++
Decrement | --

### Assignent Operators
Assign value to variables
= | += | -= | *= | /= | %= | **= 
  --- | --- |---|---|---|---|---

### Comparison Operators

Equal to | ==
  --- | --- 
Equal value and equal type | ===
Not equal | !=
Not equal value or not equal type | !==
Greater than | >
Less than | <
Greater than or equal to | >=
Less than or equal to | <=
Ternary operator | ?

### Logical Operators

 Logical and | &&
  --- | --- 
Logical or| two vertical bars
Logical not | !


### Type Operators


  typeof| Returns typle of variable
  --- | --- 
instanceof | Returns true if an object is an instance of a type

### Bitwise Operators

 
AND | &
---|--- 
OR | vertical bar
NOT | ~
XOR | ^
left shift | <<
right shift | >>
Unsigned right shift | >>>

## Data Type Code

### int and float

Input:

    const num1=3.7; 
    const num2 = 2;
    const sum = num1 + num2;
    console.log(sum)
    
Output:

      5.7

### string

Input:

    const a =("Hello User");
    console.log(a);

Output:

    Hello User


### boolean
returns either true or false

Input:

    console.log(5==6);

Output:

    false

### array

Input:

    const catNames= ["Henry","Sam","Lucy"]
    console.log(catNames);

Output:

    (3) ["Henry","Sam","Lucy"]


### dictionary 

Input:

      var dict = [{
    pet:"cat",
    age : 2,
    name:"Sam"
    },
    {
    pet:"dog",
    age : 1,
    name:"Fred"

    }
    ];
    console.log(dict[0]);

Output:

    {pet: 'cat', age: 2, name: 'Sam'}
    
## Functions

To make a function you use the function keyword followed by the function name and then parameters inside parenthesis. Functions can only run when they are in scope. Javascript does support recursive functions. Functions can accept multiple variables within parameters, in the parentheses separated by commas. They also can be different data types. You can also return multiple values in the return statement by separating them with commas.  Javascript functions are  passed by value ( functions know values, not the location of the value).  Javascript has global variables (declared outside the function) and local variables (declared inside the function). When Variables are declared their lifetime starts. When it is a global variable they only die when the web browser is closed. When it is a local variable they die when the function is completed. Local variables are also stored on the stack until the function has run. 


#### Where are the arguments, parameters and local variables stored during execution?
Stack | Heap
---|--- 
number |function
string | array
boolean | 
null | 
undefined | 

  
#### Function that takes in two numbers, multiplies them, and returns the output. Also saves the results of the function calls in variables. Also this shows a pass by value function.


Input:

    function add(x,y){
      a= x*y
    return a
    }

    let result = add(2,5)  //let assigns variable to a simple value
    console.log(result)

Output:

    10


#### Function that takes in a string (or your language's equivalent) and splits it into two strings, then returns both strings

Input:

    function func() {
      let str = 'Hello world'
      let array = str.split(" ");
      console.log(array);
    }
    func();

  Output:
      
      (2) ['Hello', 'world']
####  Recursive function

Input:

    function countDown(x) {
      console.log(x)
  
      let y = x - 1
  
      if (y > 0) {
          countDown(y)
      }
    }
    countDown(3)
Output:

    3
    2
    1



## Conditional Statements

if |
---|
if else |
else |
switch | 

The delimit code blocks for condition in selection control statements are {“curly brackets”}.

### One-condition if/else statement

Input:

    x=1;
    if(x==0){
      console.log("x is 0!")
    }
    else{
      console.log("x is not 0!")
    }

  Output:

    x is not 0!

### Multi-condition if/else if/else statement

Input:

    x=11;
    if(x>1 && x<10){
      console.log("This number is between 1 and 10")
    }
    else if(x>10){
      console.log("This number is greater than 10")
    }
    else{
      console.log("This number is less than 0.")
    }

Output:

    This number is greater than 10

### Short-circuit evaluation 

In javascript short-circuit evaluation happens in to instances with the or and and operations, javascript will read left to right.

### Or operator will return the first true value or the last false value. 

Input:

    console.log(true || false)

Output:

      true
### And operator will return false when it hits the first false value, or will return the last true value, if all values are true. 

Input:

    console.log(true && false)

Output:

      false

### Switch

Input:

      switch (6) {
    case 1:
        console.log("Sunday");
        break;
    case 2:
         console.log("Monday");
         break;
    case 3:
        console.log("Tuesday");
        break;
    case 4:
        console.log("Wednesday");
        break;
    case 5:
        console.log("Thursday");
        break;
    case 6:
        console.log("Friday");
        break;
    case 7:
        console.log("Saturday");
        break;
    default:
        console.log("Not a day");
       break;}

Output:

    Friday


### Dangling else problem
  Dangling else problem usually happens in javascript when not using curly brackets. The simplest way to fix this problem is to use curly brackets.


## Classes and Inhertance
#### Objects are variables that can have many values 


Input:

    
    const person ={name:"Jane", age:21, hairColor:"brown"} // creat person object
    // code to print out 
    document.getElementById("demo").innerHTML =
    person.name + " is " + person.age + " years old.";

Output:

    Jane is 21 year old.
#### this
this is a keyword used to refrence objects

Code example:

    function myFunction() {
      return this;}
### Standard Methods
Javascript has standard methods that are built in for Java scrpit [Click here for list](https://dev.to/elpepebenitez/built-in-methods-in-javascript-4bll).



## Sources
https://www.w3schools.com/js/js_history.asp#:~:text=JavaScript%20was%20invented%20by%20Brendan,JavaScript%20for%20the%20Firefox%20browser

https://launchschool.com/books/javascript/read/introduction

https://www.programiz.com/java-programming/hello-world

https://www.programiz.com/javascript/recursion#:~:text=Recursion%20is%20a%20process%20of,function%20is%20a%20recursive%20function.

https://dmitripavlutin.com/6-ways-to-declare-javascript-functions/#:~:text=way%20is%20better%3F-,1.,that%20delimits%20the%20body%20code.&text=Open%20the%20demo.

https://flexiple.com/javascript/javascript-pass-by-reference-or-value#:~:text=It%20is%20important%20to%20note,arguments%20inside%20of%20the%20function.

https://fjolt.com/article/javascript-by-reference-by-value

https://www.w3schools.com/js/js_scope.asp#:~:text=The%20Lifetime%20of%20JavaScript%20Variables,browser%20window%20(or%20tab).

https://www.geeksforgeeks.org/javascript-string-split-method/

https://www.javascripttutorial.net/javascript-recursive-function/\

https://www.educative.io/answers/what-are-javascript-short-circuiting-operators#:~:text=In%20JavaScript%2C%20short%2Dcircuiting%20is,return%20that%20result%20(value).

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/block#:~:text=The%20block%20is%20delimited%20by,or%20more%20statements%20and%20declarations.

https://www.w3schools.com/js/js_switch.asp

https://www.javatpoint.com/dangling-else-problem-in-java


