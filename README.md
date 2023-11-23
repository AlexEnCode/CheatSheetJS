## If else

### If statement
```JS
let country = prompt("What country are you from?");  

if (country === "Portugal") {  
  alert("You are cool");
}

if (country !== "Portugal") {  
  alert("Too bad for you");
}
```
### If else statement
```JS
let age = prompt("How old are you?");

if (age < 18) {
  alert("You cannot apply");
} else {
  alert("You can apply");
}
```
### Nested if else statements
```JS
if (age < 18) {  
  alert("you can't apply");  
} else {  
  if (age > 120) {
    alert("you can't apply");  
  } else {  
    alert("you can apply");
  }
}
```
### Logical Or
```JS
if (age < 18 || gender === "male") {  
  alert("You can't join SheCodes 👩‍💻"); 
}
```
### Logical And
```JS
if (continent === "Europe" && language === "Portuguese") {  
  alert("You are from Portugal 🇵🇹");  
} else {
  alert("You are not from Portugal");  
}
```

# Math.

```JS
var pi = Math.PI;       // 3.141592653589793
Math.round(4.4);        // = 4 - rounded
Math.round(4.5);        // = 5
Math.pow(2,8);          // = 256 - 2 to the power of 8
Math.sqrt(49);          // = 7 - square root 
Math.abs(-3.14);        // = 3.14 - absolute, positive value
Math.ceil(3.14);        // = 4 - rounded up
Math.floor(3.99);       // = 3 - rounded down
Math.sin(0);            // = 0 - sine
Math.cos(Math.PI);      // OTHERS: tan,atan,asin,acos,
Math.min(0, 3, -2, 2);  // = -2 - the lowest value
Math.max(0, 3, -2, 2);  // = 3 - the highest value
Math.log(1);            // = 0 natural logarithm 
Math.exp(1);            // = 2.7182pow(E,x)
Math.random();          // random number between 0 and 1
Math.floor(Math.random() * 5) + 1;  // random integer, from 1 to 5
```
# Arrays

```JS
dogs.toString();                        // convert to string: results "Bulldog,Beagle,Labrador"
dogs.join(" * ");                       // join: "Bulldog * Beagle * Labrador"
dogs.pop();                             // remove last element
dogs.push("Chihuahua");                 // add new element to the end
dogs[dogs.length] = "Chihuahua";        // the same as push
dogs.shift();                           // remove first element
dogs.unshift("Chihuahua");              // add new element to the beginning
delete dogs[0];                         // change element to undefined (not recommended)
dogs.splice(2, 0, "Pug", "Boxer");      // add elements (where, how many to remove, element list)
var animals = dogs.concat(cats,birds);  // join two arrays (dogs followed by cats and birds)
dogs.slice(1,4);                        // elements from [1] to [4-1]
dogs.sort();                            // sort string alphabetically
dogs.reverse();                         // sort string in descending order
x.sort(function(a, b){return a - b});   // numeric sort
x.sort(function(a, b){return b - a});   // numeric descending sort
highest = x[0];                         // first item in sorted array is the lowest (or highest) value
x.sort(function(a, b){return 0.5 - Math.random()});     // random order sort
```
### while loop
```JS
let times = 0;
while (times < 10) {  
  console.log(times);  
  times = times + 1;
}
```
### forEeach loop
```JS
let fruits = ['apples', 'oranges', 'bananas'];  
fruits.forEach(function(fruit) {  
  alert("I have " + fruit + " in my shopping bag");
});
```
### do while loop
```JS
let times = 0;
do {
  console.log(times);
  times = times + 1;
} while(times < 10)
```
### do while loop
```JS
let times = 0;
do {
  console.log(times);
  times = times + 1;
} while(times < 10)
### for loop
for (let i = 0; i < 10; i++) {
  console.log("i is " + i);
}
```
```JS
for (let i = 0; i < myList.length; i++) {  
  alert("I have " + myList[i] + " in my shopping bag");
}
```
### Remove first item
```JS
fruits.shift()
```
# Functions

### JS Functions
```JS
function sayFact() {  
  let name = prompt("What's your name?");

  if (name === "Sofia") {  
    alert("Your name comes from the Greek -> Sophia");
  }
}

sayFact();
```
### JS Functions Parameters
```JS
function fullName(firstName, lastName) {  
  alert(firstName + " " + lastName);
}

let firstName = prompt("What's your first name?");  
let lastName = prompt("What's your last name?");  
fullName(firstName, lastName);  
fullName("Kate", "Robinson");
```
### JS Functions Return
```JS
function add(x, y) {
  return x + y;
}

let result = add(3, 4);
let result2 = add(result, 0);


function getFullName(firstName, lastName) {


  let fullName = firstName + " " + lastName;


  return fullName;
}

let userFullName = getFullName("Kate", "Robinson");


alert(userFullName); // Kate Robinson


alert(getFullName("Julie", "Smith")); // Julie Smith
```
### Closures
```JS
function hello() {
  function go(name) {
    alert(name);
  }

  let name = "SheCodes";
  go(name);
}

hello();
```
# Debugging

###  Console.log
```JS
console.log(name);
console.log("Let's code!");
```
# Selectors

### QuerySelector
```JS
let li = document.querySelector("li");


let day = document.querySelector(".day");


let paragraph = document.querySelector("ul#list p");
```
Returns the first element (if any) on the page matching the selector.

### QuerySelectorAll
```JS
let lis = document.querySelectorAll("li");
let paragraphs = document.querySelectorAll("li#special p");
```
Returns all elements (if any) on the page matching the selector.

# AJAX

### AJAX with Fetch

```JS
let root = 'https://jsonplaceholder.typicode.com'
let path = 'users/1'

fetch(root + '/' + path)
  .then(response => (
    response.json()
  ))
  .then(json => (
    console.log(json)
  ));
```
Note: We recommend axios instead

### AJAX with Axios
```JS
<!DOCTYPE html>
<html>
  <head>
    <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  </head>
  <body>
    <script>
      function showUser(response) {
        alert(`The user name is ${response.data.name}`);
      }

      let url = "https://jsonplaceholder.typicode.com/users/1";
      axios.get(url).then(showUser);
    </script>
  </body>
</html>
```
