OVERVIEW
<ul>
<li> Data types <li>
<li> Dynamic typing </li>
<li>Strings </li>
<li>Numbers</li>
<li>Booleans</li>
<li>
BigInt</li>
<li>
Undefined</li>
<li>
Symbols</li>
<li>
Objects</li>
<li>Null</li>

</ul>








<h4> DATA TYPES </h4>
We come across different kinds of data – numbers, alphabets, symbols. Data types supported by a language are quite simply the kind of data the language can work with under some predefined rules. Here’s how Wikipedia defines it :

In computer science and computer programming, a data type or simply type is an attribute of data which tells the compiler or interpreter how the programmer intends to use the data. Most programming languages support basic data types of integer numbers (of varying sizes), floating-point numbers (which approximate real numbers), characters and Booleans. A data type constrains the values that an expression, such as a variable or a function, might take. This data type defines the operations that can be done on the data, the meaning of the data, and the way values of that type can be stored. A data type provides a set of values from which an expression (i.e. variable, function, etc.) may take its values.

Data Types – Wikipedia
The data types that are supported by JavaScript are : Strings , Numbers , Arrays, Objects , Booleans, Empty, Null, Undefined . To know the data type of any particular variable, we can use the ‘ typeOf ‘ operator.

typeof variableName
typeof 'myString'
typeof 50 


<h4>DYNAMIC TYPING </h4>
Some programming languages check the data types used at compilation stage. These programming languages are called as ‘Static Typed’ programming languages. Some programming languages check for data types at the run time and are called as ‘Dynamically Typed’ programming languages.

In Dynamically Typed languages, variables are defined before they are used. A variable is said to be defined when it has a certain value to it. JavaScript is dynamically typed.

var a ;  //a is undefined 
a = 20; //a is defined as a number 


<h4>STRINGS</h4>
Strings are a collection of different characters and are enclosed in single(‘ ‘) / double(” “) quotes or backticks(“).

The single quotes and double quotes are essentially same just remember to use the same quote at both ends of the string. The backticks (“) , however, act a bit different and enable what is called ‘Template Literals’ (. But in brief, backticks help embed expressions using ${ } :

function product(a,b){
    return a*b;
}
console.log(`Product of 23 and 56 is ${product(23,56)}`); 
// Product of 23 and 56 is 1288
Backticks also allow you to span multiple lines of code.

let places = `Bangalore,
Mumbai,
New Delhi`;
console.log(places);
//
Bangalore,
Mumbai, 
New Delhi


<h4>NUMBERS </h4>
Unlike languages like Python and C / C++ , JavaScript uses single data type for integers and decimal numbers. This data type is called ‘Numbers’. Scientific notations are also allowed.

var a = 13; 
var b = 12.36;
var c= 15e-2;
//all definitions are valid. 
<br>
<br>
<h4>BOOLEANs</h4>
Booleans are extensively used with conditional statements. A boolean can have only two values – True and False. It is like the ‘yes’ and ‘no’ of the coding realm.

if (a == b){
  console.log(" a==b returned a true");
}
else console.log("a==b returned a false");
<br>
<br>

<h4>BIGINT</h4>
BigInt is a numeric data type that can represent integers in an arbitrary precision format. These are used to store and manipulate large integer numbers which may be beyond the limits of Number data type. (Larger than 253 – 1 which is represented by MAX_SAFE_INTEGER constant ).

BigInt accepts single integer literal as string that needs to be represented and returns a value as BigInt type. It can be initialized either by appending ‘n’ to the number or calling the BigInt constructor.

varbigNum = BigInt("646546542156421354351534421354215");
console.log(bigNum); 
// returns 646546542156421354351534421354215n
MDN further explains :

You can use the operators +, *, -, **, and % with BigInts—just like with Numbers. A BigInt is not strictly equal to a Number, but it is loosely so.
A BigInt behaves like a Number in cases where it is converted to Boolean: if, ||, &&, Boolean, !.
BigInts cannot be operated on interchangeably with Numbers. Instead a TypeError will be thrown.

<h4>UNDEFINED </h4>
Undefined is a value that is automatically assigned to a variable that has been declared but not defined. It is also assigned to formal arguments for which there are no actual arguments provided.

Let value; 
//type is Undefined as value is declared but not defined. 
<h4>SYMBOL</h4>
Symbol value is created by using the function symbol(). This created an anonymous and distinct value. Symbols may have an optional description. However, regardless of using same description,

let sym1 = Symbol("sym");
let sym2 =Symbol("sym");
//regardless of same description, sym1 != sym2. 
Symbols are immutable and also don’t support auto-conversion to string.

<h4>OBJECTS</h4>
MDN defines JavaScript objects as

In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup, for example. A cup is an object, with properties. A cup has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

MDN Docs
JavaScript objects have a key-value pairs ( also called Object Literals ) and are enclosed in curly braces { }. Here is a simple example :

var obj = { name : "doWhileBlog", topic : "javascript" };
let object2 = {} ; //empty object
If you are coming from a Python background, I think you can see the similarity with Python dictionaries here.

Objects are essentially a value in memory that can be referred by an identifier. The ‘key’ of objects can be a string or a symbol value. The value assigned can be of any data type including Objects themselves.

But Objects do not simply end here, there is a lot more to them than just being key-value pair. For example, in JavaScript, even functions, null and arrays are of type object.

<h4>NULL </h4>
We just discussed that Nulls are essentially objects. If an object is not inherited, it returns a null value. A null value represents a reference that points to a non-existent or invalid object .

<h4>REFERENCE </h4>
A lot of reading goes into making a simple post, even on the most basic of topics. I have tried to mention all the significant sources that I have used. These should be used for further reading, if needed. MDN docs are however, an exception and must be read by anyone learning JavaScript.

Strings (javascript.info)

Template literals (Template strings) – JavaScript | MDN (mozilla.org)

JavaScript Data Types (w3schools.com)

JavaScript data types and data structures – JavaScript | MDN (mozilla.org)

BigInt in JavaScript – GeeksforGeeks

BigInt (javascript.info)
