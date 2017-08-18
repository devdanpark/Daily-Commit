# EVENTS
- Notifications that are sent to notify the code that something happned on the webpage
- Examples : clicking a button...
- Event Listener : A function that performs an action based on a certain event. It waits for a specific event to happen.

## querySelector 
- A method that checks the object.
``` javascript
var li = document.querySelectior('li')
/// selecting 'li' property
```
``` javascript
var li = document.querySelector('.active');
li.style.color = 'blue'
// '.active' means class property.
// switch the color that has class property 'active'

var li2 = document.querySelectorAll('li')
//Select all that has property 'li'
```