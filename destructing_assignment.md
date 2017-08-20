# Destructing Assignment

``` javascript
let data = [1,2,3,4,5];
let [a,b,c,d,e] = data
console.log(a) //1

let anotherData = [7,8,9,10,11,12,13,14]
let [a,b,c, ...other] = anotherData
console.log(a) //7
console.log(other) //[10,11,12,13,14]

let x = 1;
let y = 2;
[x,y] = [y, x]
console.log(x,y) // 2,1
```

- Properties of the object can be divided into variables
``` javascript
let book = { title: 'Master JS', publish: 'book', price: '222' }
let { price, title, memo = 'none' } = book;
console.log(title); // Master JS
console.log(price); //222
console.log(memo); //none
```
