
<!--Node Js learnings
To make any project to be npm, go to root directory of that folder and run 'npm init' and answer some basic questions it will enable npm on that project
then go to package.json and add start script to say ex: node app.js so when you run npm start on command line, it will run node app.js internally
To test if node is installed, just create a plain .js file and run that file using cmd or bash with command node "path to the file", it will show the output of .js file meaning if u have console statement
it will print the console output 
1)Require function can be used to load .js file meaning when we use require('express') it internally just loads index.js in express node module
. we can create two .js files in plain simple application (not node enabled) and can export on .js file and import that using require statement in another .js file because import feature is from ES2015 (meaning javascript feature) and not from any specific framework
Ex: See the first 5 minutes of below video https://www.youtube.com/watch?v=RLtyhwFtXQA
2)Node.js provides capabilities to create your own web server which will handle HTTP requests asynchronously. You can use IIS or Apache to run Node.js web application but it is recommended to use Node.js web server
3) Read about node folder structure meaning Node_modules and node_modules/.bin  ,local vs global installation
https://docs.npmjs.com/files/folders.html
-->

 Javascript Reference

<!-- Javascript learnings
Top Eight Javascfript Objecfs and Array Functions 
https://www.youtube.com/watch?v=Xal65C7pxVM
2) Value vs reference type:
  5 primitive type  : boolean, string, integer, null , undefined
  Above are value type meaning when we make a copy of them then change old value, new variable will not be changed as new memory heap will be created for new ones
  Non-Primitive Types-Reference Types : Array, Functions and Objects --Techinically all are called as Objects
  when we assign or copy them to new variable then any change in old variable data will change new variable data also

3) Learn Es6 Concepts--Must to learn new features
4)Closure - Lexical scoping ??
  javascript is a compiled language, but what does this mean? Shortly, just before execution, the source code is sent by the engine trough a compiler, in which, during an early phase called lexing (or tokenizing), scope get defined. This doesn’t just tell us what’s in a name, but also remember us that lexical scope is based on where variables and blocks of scope have been authored in the source code. In other words, lexical scope is defined by you during author time and frozen by the lexer during compilation
  5) Use Strict --look all the way at bottom
.filter()
.map()
5) Difference between function and methods in javascript
  a method is a function defined as property in object. (Methods are functions stored as object properties.)
  Reference : https://www.w3schools.com/js/js_object_methods.asp
  var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
 fullname is property in person Object and can be accessed as method/function by person.fullname(), where as function is defined at global level.
6) Tilde symbol (~) in javascript ,does boolean check on a string, Example below
On its own, indexOf() returns the index number of a String object passed in.

var foo = "bar";

foo.indexOf("r"); // 2
foo.indexOf("b"); // 0
foo.indexOf("a"); // 1
Combined with ~, it can do a boolean check if an item exists in a string value:

var foo = "hello world";

if (~foo.indexOf("w")) {
  // item in list
} else {
  // item not in list
}
This works because if a value does not exist the return is -1 for historical reasons. 

7) Prototype:
 All JavaScript objects inherit properties and methods from a prototype.
 The JavaScript prototype property allows you to add new properties to object constructors:
 function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}

Person.prototype.nationality = "English";
 Documentation: https://www.w3schools.com/js/js_object_prototypes.asp
Good knowledge on interview questions--https://www.toptal.com/javascript/interview-questions
-->





<!-- Learnings from this app:
 1) Make Sure Script Tag is declared, only then Data function will work
 2)If want to set the value in Parent Component or in any other component value of HTML(rather than in same component)
    then use PROP field Ex: <span>Componentproperty</span> in below example or entire InterpolationComponent.vue refers as example
 3) if you dont want in another component to change the value of field then use Data() function as shown below 
    for <span>{{databind}}</span> 
 4) if want to use V-modal in parent component or class then use @input method as shown below and can also bind the value of that control to
    another control using interpolation
  5) use props to set the default value but can be overridden in parent component
    Example <<name1>> property in InterpolationComponent.vue 
  6) Slot example below <slot> coming from slot.vue   and example to set the value of slot field in parent <<slotparentsetvalue>> 
  7) Pass button click event from component to parent  and set the fields in parents class using that event
  8) pass button click event from component to parent with some static data and use that data to set fields values in parent class 
  9) pass button click event from component to parent with some dynamic field data from component and use that data to set fields values in parent class  
  10) pass Dropdown select event change
  11) Look at tour of heroes app for Dynamic Component Loading , navigating b/w multiple components and sharing information between them.
-->





<!--
1) "Use Strict"--
The short and most important answer here is that use strict is a way to voluntarily enforce stricter parsing and error handling on your JavaScript code at runtime. Code errors that would otherwise have been ignored or would have failed silently will now generate errors or throw exceptions. In general, it is a good practice.

Some of the key benefits of strict mode include:

Makes debugging easier. Code errors that would otherwise have been ignored or would have failed silently will now generate errors or throw exceptions, alerting you sooner to problems in your code and directing you more quickly to their source.
Prevents accidental globals. Without strict mode, assigning a value to an undeclared variable automatically creates a global variable with that name. This is one of the most common errors in JavaScript. In strict mode, attempting to do so throws an error.
Eliminates this coercion. Without strict mode, a reference to a this value of null or undefined is automatically coerced to the global. This can cause many headfakes and pull-out-your-hair kind of bugs. In strict mode, referencing a a this value of null or undefined throws an error.
Disallows duplicate parameter values. Strict mode throws an error when it detects a duplicate named argument for a function (e.g., function foo(val1, val2, val1){}), thereby catching what is almost certainly a bug in your code that you might otherwise have wasted lots of time tracking down.
Note: It used to be (in ECMAScript 5) that strict mode would disallow duplicate property names (e.g. var object = {foo: "bar", foo: "baz"};) but as of ECMAScript 2015 this is no longer the case.
Makes eval() safer. There are some differences in the way eval() behaves in strict mode and in non-strict mode. Most significantly, in strict mode, variables and functions declared inside of an eval() statement are not created in the containing scope (they are created in the containing scope in non-strict mode, which can also be a common source of problems).
Throws error on invalid usage of delete. The delete operator (used to remove properties from objects) cannot be used on non-configurable properties of the object. Non-strict code will fail silently when an attempt is made to delete a non-configurable property, whereas strict mode will throw an error in such a case.

 -->
