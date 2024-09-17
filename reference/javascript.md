# JavaScript

JavaScript is an interpreted programming language that runs natively in browsers, and also has other runtimes such as Node.js, commonly used to write server applications in JavaScript.

- [Primary reference on JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

**If you have no prior experience in JavaScript, or, you want to refresh your knowledge, then you can take the following free courses at Codecademy:**

- [Learn JavaScript on Codecademy](https://www.codecademy.com/learn/introduction-to-javascript)
- [Learn Asynchronous JavaScript on Codecademy](https://www.codecademy.com/learn/asynchronous-javascript)

## Notable features

- Originally created for an early web browser
- Intepreted, and/or [JIT](https://en.wikipedia.org/wiki/Just-in-time_compilation) compiled
- [First-class functions](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function)
- [Prototype based](https://developer.mozilla.org/en-US/docs/Glossary/Prototype-based_programming)
- [Dyanmically typed](https://developer.mozilla.org/en-US/docs/Glossary/Dynamic_typing)
- [Single-threaded *](https://developer.mozilla.org/en-US/docs/Glossary/Thread)
- [Event loop runtime](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)

## Basic example

```javascript
const API_BASE = 'https://api.squiggle.com.au';
const API_ENDPOINT = `${API_BASE}/?q=teams`;
const IMAGE_BASE = 'https://squiggle.com.au';

const app = document.getElementById('app');

async function getData() {
  const response = await fetch(API_ENDPOINT);
  data = await response.json();
  return data;
}

async function render() {
  data = await getData();
  const { teams } = data;
  for (const team of teams) {
    // do stuff with team data
  }
}
```

## A quick look at the language features and semantics

### Data types [↗](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)

- null
- undefined
- boolean
- number
- bigint
- string
- string
- symbol

```js
null
undefined

// boolean
true
false

//number
47
47.12

// bigint
9007199254740991n

// string
'My Value'
"My Value"

const dogName = 'Jesse'
`My dog's name is ${dogName}`

// symbol
const mySymbol = Symbol('foo');
```

### Data structures [↗](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)

- [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)
- [JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)

```js
// Object
const paul = {
    name: "Paul",
    age: 47,
    "city": "Tel Aviv"
};
Object.entries(paul);

// array
const myArray = [
    "Noya",
    paul
];
Array.of(...myArray);

// date
const now  = Date.now();
const unixZeroIsoformat = '01 Jan 1970 00:00:00 GMT';
const unixTimeZero = Date.parse(unixZeroIsoformat);
const xmas = new Date('December 25, 2022 00:00:00');

// JSON
const myAPIPayload = JSON.stringify(myArray);
const inboundData = JSON.parse(
'{"name": "Tim", "age": 21, "city": "New York"}'
);
```

### Functions [↗](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)

- [Definition](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#defining_functions) - a few ways
- [Scope](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#function_scope) - Functions access their variables and their parent's
- [Recursion](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#recursion) - Functions can call themselves
- [Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#closures) - Functions can be defined inside functions
- [Parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#function_parameters) - Default and rest
- [Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#arrow_functions) - Always anonymous

```js
// function declaration
function greet(name) {
    return `Hello, ${name}`;
}

const greet = function (name) {
    return `Hello, ${name}`;
}

const greet = name => `Hello, ${name}`;

const hey = greet("Michelle");
```

### Classes [↗](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

- A template to create an object
- Must be defined before they are constructed
- Further reading on [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this#class_context)

```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

const myRectangle = new Rectangle(200, 400);
```

### Variables

- Declaration
- Scoping
- Destructuring

```js
const name = 'My Name';

let age = 30;
age = 31;
age = 'thirty one';

function yourName () {
  const name = 'your name';
  return name;
}

function myName() {
  return name;
}

console.log(name) // returns 'my name'
console.log(yourName()) // returns 'your name'
console.log(myName()) // returns 'my name'
console.log(myName() === name) // returns true

const paul = {
    name: "Paul",
    age: 47,
    "city": "Tel Aviv"
};
const { name, age, city } = paul;
```

### Object methods

- [Object documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- Static methods
- Instance methods

```js
const myObject = { name: 'Theo', age: 47, height: 180 };

Object.keys(myObject)

Object.values(myObject)

for (const [key, value] of Object.entries(myObject)) {
  console.log(value);
}

const myUpdatedObject = Object.assign(
  myObject,
  {name: 'Theodore'}
);
```

### Array methods

- [Array documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- Static methods
- Instance methods

```js
const myArray = [ 47, 65, 79, 81, 99 ];

myArray[3];
myArray.slice(2);
myArray.push(115);

Array.of(7);
Array(7);
Array.from('Theodore');

// iterate with side effects
myArray.forEach(item => console.log(item));

// alternate method
for (const item of myArray) {
  console.log(item);
}

// iterate and produce new values
myArray.map(item => item * 2);
myArray.filter(item => item >= 81);
const initialValue = 0;
myArray.reduce(
  (previousValue, currentValue) => previousValue * currentValue,
  initialValue
);
```

### async / await

- JavaScript is based on an [Event Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)
- All network calls are asyncronous
- Several paradigms - callbacks, promises
- [async / await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function) is a way to write promise-based code in a cleaner style

```js
async function myAsyncCall(parameter) {
  //statements
}

const url = '/api/results.json';
const result = await myAsyncCall(url);
```
