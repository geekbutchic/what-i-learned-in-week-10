# What I Learned in Week 10

## Application Building
* Todo Application 
* Readline Interface
* Interface.Question
* Arrow Functions 

### Todo Application 
1. Add a todo.
2. Remove a todo.
3. Remove all completed todos.
4. Toggle a todo's completion status.
5. Toggle a todo's priority.
6. Quit.

![Alt Text](https://www.monicahicks.com/wp-content/uploads/2019/08/to-do-list-flat-lay.jpg)

The readline module provides an interface for reading data from a Readable stream (such as process.stdin) one line at a time. It can be accessed using:
```javascript 
const readline = require('readline');

const interface = readline.createInterface({
  input: process.stdin,
  output: process.stdout
})
```
Once this code is invoked, the Node.js application will not terminate until the readline.Interface is closed because the interface waits for data to be received on the input stream.

```javascript 
interface.question(data, function)
```
One of the differences from readline and require is readline does not require ./ since it is built into node.

```javascript
const todos = require('./data.js');
// file requires ./ the path
```
```javascript
const readline = require('readline');
// is built into node and does not require ./ file path

```
Arrow Functions how to use them and why?

![Alt Text](https://cdn-images-1.medium.com/max/1200/1*o-wasL_EjWk4g8velrI8bg.jpeg)

Arrow functions are a great way to use less code.

```javascript 
// Non-Arrow Funtion for setTimeout:

setTimeout(function() {
    console.log('hello');
}, 1000)

// Arrow version easier to make one line functions:
setTimeout(() => console.log('Hello'), 1000)

```
If the function has only one statement, and the statement returns a value, you can remove the brackets and the return keyword:

