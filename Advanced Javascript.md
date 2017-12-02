# Privmitives VS Objects

- primitives are immutable
- Objects are mutable and stored by reference


### Passing by reference VS passing by Values

### This
- Refers to an object that's set at the creation of a new execution
- In the global execution context, refers to global objects
- If the function is called as a method of an object, 'this' is bound to the object the method is called on
### Setting this Manually 
- bind(), apply(), call()
- arrow notation in ES6

# First class functions
- Functions are treated the same way as objects. 
  - Can be assigned to variables, array values, object values.
  - Can be passed as arguments to other functions
  - Can be returned from functions
- Allows for the creaion of higher-order functions
  - Either takes one or more functions as arguments or returns a function
  - map(), filter(), reduce()

## Synchronous? Async? Single Threaded?
- JS is a single-threaded. synchronous language.
- A function that takes a long time to run will cause a page to become unresponsive
- JS has functions that act asynchronously
