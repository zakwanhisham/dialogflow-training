# JavaScript Programming

## Table of Content

| First steps in Javascript Basic for Beginners |                                                   |
| --------------------------------------------- | ------------------------------------------------- |
| Lesson 1                                      | [What is Javascript](#what-is-javascript)         |
| Lesson 2                                      | [Javascript Variables](#javascript-variables)     |
| Lesson 3                                      | [Javascript Array Methods](#what-is-an-array)     |
| Lesson 4                                      | [Javascript Loops](#javascript-loops)             |
| Lesson 5                                      | [Conditional Statements](#conditional-statements) |

| Javascript Advance Stuff! |                                                     |
| ------------------------- | --------------------------------------------------- |
| Lesson 1                  | [Javascript Define & Call Functions]()              |
| Lesson 2                  | [Cookies in Javascript]()                           |
| Lesson 3                  | [Javascript DOM Tutorial]()                         |
| Lesson 4                  | [OOJS Tutorial]()                                   |
| Lesson 5                  | [Internal &External Javascript]()                   |
| Lesson 6                  | [Javascript Examples]()                             |
| Lesson 7                  | [Javascript Unit Testing Frameworks]()              |
| Lesson 8                  | [TypeScript Tutorial]()                             |
| Lesson 9                  | [TypeScript vs Javascript]()                        |
| Lesson 10                 | [Java vs JavaScript]()                              |
| Lesson 11                 | [QuickSort in JavaScript]()                         |
| Lesson 12                 | [Difference Between =, ==, and === in JavaScript]() |

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
- Example of the JavaScript program.

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
var name = "Zakwan";
```

OR

```javascript
var name;
name = "Zakwan";
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
    <script type="text/javascript">
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
