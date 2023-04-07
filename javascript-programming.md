# JavaScript Programming

## Table of Content

|          | First steps in Javascript Basic for Beginners     |
| -------- | ------------------------------------------------- |
| Lesson 1 | [What is Javascript](#what-is-javascript)         |
| Lesson 2 | [Javascript Variables](#javascript-variables)     |
| Lesson 3 | [Javascript Array Methods](#what-is-an-array)     |
| Lesson 4 | [Javascript Loops](#javascript-loops)             |
| Lesson 5 | [Conditional Statements](#conditional-statements) |

|          | Javascript Advance Stuff!                                                                           |
| -------- | --------------------------------------------------------------------------------------------------- |
| Lesson 1 | [Javascript Define & Call Functions](#javascript-define-&-call-functions)                           |
| Lesson 2 | [Cookies in Javascript](#cookies-in-javascript)                                                     |
| Lesson 3 | [Javascript DOM](#javascript-dom)                                                                   |
| Lesson 4 | [OOJS](#oojs)                                                                                       |
| Lesson 5 | [Internal & External Javascript](#internal-&-external-javascript)                                   |
| Lesson 6 | [Javascript Examples](#javascript-example)                                                          |
| Lesson 7 | [QuickSort in JavaScript](#quicksort-in-javascript)                                                 |
| Lesson 8 | [Difference Between =, ==, and === in JavaScript](#difference-between-=,-==,-and-===-in-javascript) |

---

### What is JavaScript

- JavaScript is a very powerful `client-side scripting language`.
- JavaScript is used mainly for `enhancing the interaction of a user with the webpage`.
  - In other words, you can make your webpage more lively and interactive, with the help of JavaScript.
- JavaScript is also being used widely in game development and mobile application development.

#### JavaScript History

- JavaScript was developed by `Brendan Eich in 1995`
  - Appear in Netscape(popular browser of that time)
- Initially called LiveScript and later change to JavaScript.
- Many think that `Java` and `JavaScript` are the same but they are very much unrelated.
  - Java is a very complex programming language
  - JavaScript is a scripting language
- Syntax of JavaScript is mostly influenced by `C`

#### How to Run JavaScript

- JavaScript `cannot run on its own`. The `browser is responsible for running JavaScript code`.
- Main advantage of using JavaScript is that all `modern web browser support it`.
- JavaScript also runs on any operating system.

#### Tools You Need

- You need a text editor to write your code:
  - Notepad++
  - Visual Studio Code
  - Sublime Text
  - or any other that you are comfortable with
- You also need web browser to run JavaScript:
  - Google Chrome (Preferred)
  - Firefox
  - Microsoft Edge
  - etc

#### A simple JavaScript Program

- You should place your code within a `<script> tags` if you are keeping it in HTML doc.
- It will help browser to distinguish your code from the rest of the code.
- Exercise:

```html
<html>
  <head>
    <title>My First JavaScript code</title>
    <script>
      alert("Hello World!");
    </script>
  </head>
  <body></body>
</html>
```

---

### JavaScript Variables

- Variables are used to `store values or expressions`.

#### Declare Variables in JavaScript

- Before using a variable, you can declare it first before use.

```javascript
var name;
```

#### Assign a value to the Variable

- You can assign a value to a variable either while declaring the variable or after.

```javascript
var name = "John";
```

OR

```javascript
var name;
name = "John";
```

#### Naming Variables

- It is a good practice to give descriptive and meaningful names to the variables.
- JavaScript uses `camelCase` as it naming convention.
- Exercise:

```html
<html>
  <head>
    <title>Variables</title>
    <script>
      var one = 22;
      var two = 3;
      var add = one + two;
      var minus = one - two;
      var multiply = one * two;
      var divide = one / two;
      document.write(
        "First No: = " + one + "<br/>Second No: = " + two + " <br/>"
      );
      document.write(one + " + " + two + " = " + add + "<br/>");
      document.write(one + " - " + two + " = " + minus + "<br/>");
      document.write(one + " * " + two + " = " + multiply + "<br/>");
      document.write(one + " / " + two + " = " + divide + "<br/>");
    </script>
  </head>
  <body></body>
</html>
```

---

### What is an Array?

- Object that can store a `collection of items`.
- Useful when you need to store large amounts of data of the same type.
- To access items inside array, you can refer to its `indexNumber` and the index start with `zero`.

### Javascript Create Array

```javascript
var students = ["John", "Ann", "Kevin"];
```

- If you want to add more to the array, you can use:

```javascript
students[3] = "Emma";
students[4] = "Rose";
```

- You can also create an array using `Array Constructor`:

```javascript
var students = new Array("John", "Ann", "Kevin");
```

OR

```javascript
var students = new Array();
students[0] = "John";
students[1] = "Ann";
students[2] = "Kevin";
```

#### JavaScript Array Methods

- The array object has many properties and methods which help developers to handle arrays easily and efficiently

1. `length property` -> number of elements inside an array.
2. `prototype property` -> add new properties and methods.
3. `reverse method` -> reverse the order of items inside an array.
4. `sort method` -> sort the items inside an array.
5. `pop method` -> remove the last item of an array.
6. `shift method` -> remove the first item of an array.
7. `push method` -> add a values as the last item of an array.

- Exercise:

```html
<html>
  <head>
    <title>Arrays</title>
    <script>
      var students = new Array("John", "Ann", "Aaron", "Edwin", "Elizabeth");
      Array.prototype.displayItems = function () {
        for (i = 0; i < this.length; i++) {
          document.write(this[i] + "<br />");
        }
      };
      document.write("students array<br />");
      students.displayItems();
      document.write(
        "<br />The number of items in students array is " +
          students.length +
          "<br />"
      );
      document.write("<br />The SORTED students array<br />");
      students.sort();
      students.displayItems();
      document.write("<br />The REVERSED students array<br />");
      students.reverse();
      students.displayItems();
      document.write(
        "<br />THE students array after REMOVING the LAST item<br />"
      );
      students.pop();
      students.displayItems();
      document.write("<br />THE students array after PUSH<br />");
      students.push("New Stuff");
      students.displayItems();
    </script>
  </head>
  <body></body>
</html>
```

---

### JavaScript Loops

#### How to use loops?

- Loops are useful when you have to execute the same lines of codes repeatedly, for a specific number of times or as long as a specific condition is true.
- There are mainly four types of loops in JS:
  1. for loop
  2. for/in a loop (will discuss later)
  3. while loop
  4. do...while loop

#### for loop

Syntax:

```javascript
for (statement1; statement2; statement3) {
  // lines of codes to be executed
}
```

- `statement1`: executed first even before executing the looping code. This statement is normally used to assign values to variables that will be used inside the loop.
- `statement2`: condition to execute the loop.
- `statement3`: executed every time after the looping code is executed.

- Exercise

```html
<html>
  <head>
    <script>
      var students = new Array("John", "Ann", "Aaron", "Edwin", "Elizabeth");
      document.write("<b>Using for loops </b><br />");
      for (i = 0; i < students.length; i++) {
        document.write(students[i] + "<br />");
      }
    </script>
  </head>
  <body></body>
</html>
```

#### while loop

Syntax:

```javascript
while (condition) {
  // lines of codes to be executed
}
```

- The `while loop` is executed as long as the specified condition is true. Inside the while loop, you should include the statement that will end the loop at some point of time. Otherwise, your loop will never end and your browser may crash.

- Exercise

```html
<html>
  <head>
    <script>
      document.write("<b>Using while loops </b><br />");
      var i = 0,
        j = 1,
        k;
      document.write("Fibonacci series less than 40<br />");
      while (i < 40) {
        document.write(i + "<br />");
        k = i + j;
        i = j;
        j = k;
      }
    </script>
  </head>
  <body></body>
</html>
```

#### do...while loop

Syntax:

```javascript
do {
  // block of codes to be executed
} while (condition);
```

- The `do...while loop` is very similar to `while loop`. The only difference is that in do...while loop, the block of code gets executed once even before checking the condition.

- Exercise

```html
<html>
  <head>
    <script>
      document.write("<b>Using do...while loops </b><br />");
      var i = 2;
      document.write("Even numbers less than 20<br />");
      do {
        document.write(i + "<br />");
        i = i + 2;
      } while (i < 20);
    </script>
  </head>
  <body></body>
</html>
```

---

### Conditional Statements

#### How to use conditional statements

- Conditional Statements are used to decide the flow of execution based on different conditions. If a condition is true, you can perform one action and if the condition is false, you can perform another action.
- There are mainly 3 types of conditional statements
  1. If statement
  2. If...Else statement
  3. If...Else If...Else statement

#### If Statement

Syntax:

```javascript
if (condition) {
  // lines of code to be execute
}
```

- Use `If statement` if you want to check only a specific condition

- Exercise:

```html
<html>
  <head>
    <title>IF Statments!!!</title>
    <script>
      var age = prompt("Please enter your age");
      if (age >= 18) document.write("You are an adult <br />");
      if (age < 18) document.write("You are NOT an adult <br />");
    </script>
  </head>
  <body></body>
</html>
```

#### If...Else Statement

Syntax:

```javascript
if (condition) {
  // lines of code to be execute
} else {
  // lines of code to be execute
}
```

- Use `If...Else statement` if you want to check two conditions and execute a different set of codes.

- Exercise

```html
<html>
  <head>
    <title>If...Else Statments!!!</title>
    <script>
      // Get the current hours
      var hours = new Date().getHours();
      if (hours < 12) document.write("Good Morning!!!<br />");
      else document.write("Good Afternoon!!!<br />");
    </script>
  </head>
  <body></body>
</html>
```

#### If...Else If...Else statement

```javascript
if (condition1) {
  // lines of code to be execute
} else if (condition2) {
  // lines of code to be execute
} else {
  // lines of code to be execute
}
```

- Use `If...Else If...Else statement` if you want to check more than two conditions.

- Exercise

```html
<html>
  <head>
    <script>
      var one = prompt("Enter the first number");
      var two = prompt("Enter the second number");
      one = parseInt(one);
      two = parseInt(two);
      if (one == two) document.write(one + " is equal to " + two + ".");
      else if (one < two) document.write(one + " is less than " + two + ".");
      else document.write(one + " is greater than " + two + ".");
    </script>
  </head>
  <body></body>
</html>
```

---

### JavaScript Define & Call Functions

#### What is function in JavaScript?

- A block of code which will be executed only if it is called.
- Very important and useful in any programming language as it makes the code reusable.

#### Creating Function in JavaScript

Syntax:

```javascript
function functionName() {
  // block of code
}
```

- Exercise

```html
<html>
  <head>
    <title>Functions</title>
    <script>
      function myFunction() {
        document.write("This is a simple function.<br />");
      }
      myFunction();
    </script>
  </head>
  <body></body>
</html>
```

#### Function with Argument

Syntax:

```javascript
function functionName(arg1, arg2) {
  // block of code
}
```

- Exercise

```html
<html>
  <head>
    <script>
      var count = 0;
      function countVowels(name) {
        for (var i = 0; i < name.length; i++) {
          if (
            name[i] == "a" ||
            name[i] == "e" ||
            name[i] == "i" ||
            name[i] == "o" ||
            name[i] == "u"
          )
            count = count + 1;
        }
        document.write(
          "Hello " + name + "!!! Your name has " + count + " vowels."
        );
      }
      var myName = prompt("Please enter your name");
      countVowels(myName);
    </script>
  </head>
  <body></body>
</html>
```

#### JavaScript Return Value

Syntax:

```javascript
function functionName(arg1, arg2) {
  // block of code
  return val1;
}
```

- Exercise

```html
<html>
  <head>
    <script>
      function returnSum(first, second) {
        var sum = first + second;
        return sum;
      }
      var firstNo = 78;
      var secondNo = 22;
      document.write(
        firstNo + " + " + secondNo + " = " + returnSum(firstNo, secondNo)
      );
    </script>
  </head>
  <body></body>
</html>
```

---

### Cookies in Javascript

#### What are Cookies

- Cookies is a piece of data that is stored on computer to be accesses on the browser.
- An example of cookie is the `remember password` feature.

#### Javascript set Cookie

- Create cookie using this syntax:

  ```javascript
  document.cookie = "cookiename=cookievalue";
  ```

- You can add `expiry date`. The `expiry date` should be set in the `UTC/GMT` format. If there is no expiry date, then the cookie will be remove when browser is close.

  ```javascript
  document.cookie =
    "cookiename=cookievalue; expires=Thu, 21 Aug 2023 20:00:00 UTC";
  ```

- You can also set the domain and path to specify to which domain and to which directories in the specific domain the cookie belongs to. By default, a cookie belongs to the page that sets the cookie.

```javascript
document.cookie =
  "cookiename=cookievalue; expires=Thu, 21 Aug 2014 20:00:00 UTC; path=/ ";
```

#### Javascript get Cookie

- You can access the cookies like this:

```javascript
var x = document.cookie;
```

#### Javascript Delete Cookie

- To delete a cookie, you just need to set the value of the cookie to empty and set the value of expires to a passed date

```javascript
document.cookie = "cookiename= ; expires=Thu, 01 Jab 1970 00:00:00 GMT";
```

- Exercise

```html
<html>
  <head>
    <title>Cookie!!!</title>
    <script>
      function createCookie(cookieName, cookieValue, daysToExpire) {
        var date = new Date();
        date.setTime(date.getTime() + daysToExpire * 24 * 60 * 60 * 1000);
        document.cookie =
          cookieName + "=" + cookieValue + "; expires=" + date.toGMTString();
      }
      function accessCookie(cookieName) {
        var name = cookieName + "=";
        var allCookieArray = document.cookie.split(";");
        for (var i = 0; i < allCookieArray.length; i++) {
          var temp = allCookieArray[i].trim();
          if (temp.indexOf(name) == 0)
            return temp.substring(name.length, temp.length);
        }
        return "";
      }
      function checkCookie() {
        var user = accessCookie("testCookie");
        if (user != "") alert("Welcome Back " + user + "!!!");
        else {
          user = prompt("Please enter your name");
          num = prompt(
            "How many days you want to store your name on your computer?"
          );
          if (user != "" && user != null) {
            createCookie("testCookie", user, num);
          }
        }
      }
    </script>
  </head>
  <body onload="checkCookie()"></body>
</html>
```

---

### Javascript DOM

#### What is DOM

- DOM - Document Object Model.
- Javascript can access all the elements in a webpage using DOM

![js-dom](https://www.guru99.com/images/JavaScript/javascript8_1.png)

#### How to use DOM and Events

- By using DOM, javascript can create new elements and attributes, change the existing elements and attributes and even remove existing elements and attributes.
- Can also react to existing events and create new ecents in the page.

#### getElementById, innerHTML

- getElementById = access elements and attributes whose id is set
- innerHTML = access the content of an element

```html
<html>
  <head>
    <title>DOM!!!</title>
  </head>
  <body>
    <h1 id="one">Welcome</h1>
    <p>This is the welcome message.</p>
    <h2>Technology</h2>
    <p>This is the technology section.</p>
    <script>
      var text = document.getElementById("one").innerHTML;
      alert("The first heading is " + text);
    </script>
  </body>
</html>
```

#### getElementsByTagName

- getElementsByTagName = access elements and attributes using tag name. Return an array of all the items with the same tag name

```html
<html>
  <head>
    <title>DOM!!!</title>
  </head>
  <body>
    <h1>Welcome</h1>
    <p>This is the welcome message.</p>
    <h2>Technology</h2>
    <p id="second">This is the technology section.</p>
    <script>
      var paragraphs = document.getElementsByTagName("p");
      alert("Content in the second paragraph is " + paragraphs[1].innerHTML);
      document.getElementById("second").innerHTML =
        "The orginal message is changed.";
    </script>
  </body>
</html>
```

#### Event handler

- createElement = create new element
- removeChild = remove an element

```javascript
document.getElementById(id).onclick = function () {
  //lines of code
};
```

OR

```javascript
document.getElementById(id).addEventListener("click", functionname);
```

- Example

```html
<html>
  <head>
    <title>DOM!!!</title>
  </head>
  <body>
    <input type="button" id="btnClick" value="Click Me!!" />
    <script>
      document.getElementById("btnClick").addEventListener("click", clicked);
      function clicked() {
        alert("You clicked me!!!");
      }
    </script>
  </body>
</html>
```

---

### OOJS

#### OOP concept in javascript

- create objects that act like real life objects.
- Eg: Student or home can be an object that have many unique characteristics of their own.
  - properties nad methods to objects can be created easier

### How to create an object

```javascript
var objName = new Object();
objName.property1 = value1;
objName.property2 = value2;
objName.method1 = function () {
  // lines of code
};
```

OR

```javascript
var objName = {
  property1: value1,
  property2: value2,
  method1: function () {
    // lines of code
  },
};
```

#### Access object properties an methds

- Access properties of an object:

```javascript
objName.propertyname;
```

- Access methods of an object:

```javascript
objName.methodname();
```

- Example

```html
<html>
  <head>
    <title>Objects!!!</title>
    <script>
      var student = new Object();
      student.fName = "John";
      student.lName = "Smith";
      student.id = 5;
      student.markE = 76;
      student.markM = 99;
      student.markS = 87;
      student.calculateAverage = function () {
        return (student.markE + student.markM + student.markS) / 3;
      };
      student.displayDetails = function () {
        document.write("Student Id: " + student.id + "<br />");
        document.write(
          "Name: " + student.fName + " " + student.lName + "<br />"
        );
        var avg = student.calculateAverage();
        document.write("Average Marks: " + avg);
      };
      student.displayDetails();
    </script>
  </head>
  <body></body>
</html>
```

#### OOP constructor

- Object constuctor helps create an object type which can be reused to meet the need.

```html
<html>
  <head>
    <script>
      function Student(first, last, id, english, maths, science) {
        this.fName = first;
        this.lName = last;
        this.id = id;
        this.markE = english;
        this.markM = maths;
        this.markS = science;
        this.calculateAverage = function () {
          return (this.markE + this.markM + this.markS) / 3;
        };
        this.displayDetails = function () {
          document.write("Student Id: " + this.id + "<br />");
          document.write("Name: " + this.fName + " " + this.lName + "<br />");
          var avg = this.calculateAverage();
          document.write("Average Marks: " + avg + "<br /><br />");
        };
      }
      var st1 = new Student("John", "Smith", 15, 85, 79, 90);
      var st2 = new Student("Hannah", "Turner", 23, 75, 80, 82);
      var st3 = new Student("Kevin", "White", 4, 93, 89, 90);
      var st4 = new Student("Rose", "Taylor", 11, 55, 63, 45);
      st1.displayDetails();
      st2.displayDetails();
      st3.displayDetails();
      st4.displayDetails();
    </script>
  </head>
  <body></body>
</html>
```

#### Loop through the properties of an object

```javascript
for (varName in objName) {
  // lines of codes
}
```

- Example

```html
<html>
  <head>
    <script>
      var employee = { first: "John", last: "Doe", department: "Accounts" };
      var details = "";
      document.write("<b>Using for/in loops </b><br />");
      for (var x in employee) {
        details = x + ": " + employee[x];
        document.write(details + "<br />");
      }
    </script>
  </head>
  <body></body>
</html>
```

---

### Internal & External javascript

- There are 2 ways to use javascript code:
  1. Internally within HTML doc
  2. Separate external file

#### Internal javascript

- Example

```html
<html>
  <head>
    <title>My First JavaScript code!!!</title>
    <script>
      // Create a Date Object
      var day = new Date();
      // Use getDay function to obtain todays Day.
      // getDay() method returns the day of the week as a number like 0 for Sunday, 1 for Monday,….., 5
      // This value is stored in today variable
      var today = day.getDay();
      // To get the name of the day as Sunday, Monday or Saturday, we have created an array named weekday and stored the values
      var weekday = new Array(7);
      weekday[0] = "Sunday";
      weekday[1] = "Monday";
      weekday[2] = "Tuesday";
      weekday[3] = "Wednesday";
      weekday[4] = "Thursday";
      weekday[5] = "Friday";
      weekday[6] = "Saturday";
      // weekday[today] will return the day of the week as we want
      document.write("Today is " + weekday[today] + ".");
    </script>
  </head>
  <body></body>
</html>
```

#### External javascript

- Add this line to the HTML doc

```html
<script src="currentdetails.js"></script>
```

- This is the `currentdetails.js` file

```javascript
var currentDate = new Date();
var day = currentDate.getDate();
var month = currentDate.getMonth() + 1;
var monthName;

var hours = currentDate.getHours();
var mins = currentDate.getMinutes();
var secs = currentDate.getSeconds();
var strToAppend;
if (hours > 12) {
  hours1 = "0" + (hours - 12);
  strToAppend = "PM";
} else if (hours < 12) {
  hours1 = "0" + hours;
  strToAppend = "AM";
} else {
  hours1 = hours;
  strToAppend = "PM";
}

if (mins < 10) mins = "0" + mins;
if (secs < 10) secs = "0" + secs;

switch (month) {
  case 1:
    monthName = "January";
    break;
  case 2:
    monthName = "February";
    break;
  case 3:
    monthName = "March";
    break;
  case 4:
    monthName = "April";
    break;
  case 5:
    monthName = "May";
    break;
  case 6:
    monthName = "June";
    break;
  case 7:
    monthName = "July";
    break;
  case 8:
    monthName = "August";
    break;
  case 9:
    monthName = "September";
    break;
  case 10:
    monthName = "October";
    break;
  case 11:
    monthName = "November";
    break;
  case 12:
    monthName = "December";
    break;
}

var year = currentDate.getFullYear();
var myString;
myString =
  "Today is " +
  day +
  " - " +
  monthName +
  " - " +
  year +
  ".<br />Current time is " +
  hours1 +
  ":" +
  mins +
  ":" +
  secs +
  " " +
  strToAppend +
  ".";
document.write(myString);
```

- The final file look like this

```html
<html>
  <head>
    <title>My External JavaScript Code!!!</title>
    <script src="currentdetails.js"></script>
  </head>
  <body></body>
</html>
```

#### When to use internal and external

- If you have only a few lines of code that is specific to a particular webpage, then it is better to keep javascript code internally

- If the javascript code is used in many web pages, then you can consider using external file.

---
