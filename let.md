## let 
- added in ES2015 
- let is quite similar to "var"

``` javascript
let msg;
let x,y;
let greeting = "hello JS"
```
- let does not allow repeated variable.
``` javascript
let x = 1;
let x = 2;
// In this case, it gets an error
// "Identifier 'x' has already been declared."
var x = 1;
var x = 2;
// possible.
```
- By using 'let' detail scope can be managed.