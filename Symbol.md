# Symbol Object
- Symbol is quite similar to characters but not character
- Symbol cannot be edited. Mainly used as a identifier of object property.
- Symbol object is a primitive data type's implicit wrapper.

``` javascript
var sym1 = Symbol()
var sym2 = Symbol("foo")
var sym3 = Symbol("foo")

Symbol("foo") === Symbol("foo") //false
```
- Even though there are two Symbols that have the same name, they are unique rather than the same.

- Symbol does not use "new" operator
``` javascript
var sym = new Symbol() // type error
var sym1 = Symbol("foo")
var symObj = Object(sym1);
typeof sym1 //"Symbol"
typeof symObj //"Object"
```
### Using for...in with Symbol
``` javascript
var obj = {}
obj[Symbol("a")] = "a"
obj[Symbol.for("b")] = "b"
obj["c"] = "c"
obj.d = "d"

for(var i in obj) {
    console.log(i) 
}
// "c" and "d"
```
- We cannot see 'a' and 'b' because Symbol is not presented in 'for...in'
- We need to get Object.getOwnPropertyNames() and Object.getOwnPropertySymbols()