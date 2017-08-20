# Objects

``` javascript
var john = {
    name: 'john',
    lastName: 'Smith',
    yearOfBirth: 1992,
    job: 'programmer',
    isMarried: true
};

console.log(john.name)
console.log(john['lastName']);

var xyz = 'job';
console.log(john[xyz]); //programmer

john.lastName = 'Park'
john['job'] = 'CEO'
console.log(john.job) //CEO

var daniel = new Object();
daniel.name = 'daniel'
daniel.lastName = 'Park'
daniel['yearOfBirth'] = 1992;
daniel.isMarried = true;

console.log(daniel)
```

## Objects and Methods
``` javascript
var john = {
    name: 'john'
    lastName: 'Park'
    yearOfBirth: 1992,
    job: 'student',
    isMarried: true,
    family: ['jane', 'john', 'mimi']
    calculateAge: function() {
        return 2017 - this.yearOfBirth;
    }
};

console.log(john);
console.log(john.calculateAge())

var age = john.calculateAge();
john.age = age;
console.log(john)
```
## Object.create
``` javascript
var personProto = {
    calculateAge: function() {
        console.log(2017-this.yearOfBirth);
    }
};

var daniel = Object.create(personProto);
daniel.name = 'John'
daniel.yearOfBirth = 1992;
daniel.job = 'CEO'

var jane = Object.create(personProto);
{
    name: { value: 'Jane' },
    yearOfBirth: { value: 1992 };
    job: { value: 'designer' }; 
}
```
## Primitives vs Objects
- Variables associated with objects do not actually contain the object.
- They contian a reference to the place in memory where the object sits, where the object is stored.
- Variable just points to the object

``` javascript
var a = 23;
var b = a;
a = 46;
console.log(a) //46
console.log(b) //23

var obj1 = {
    name: 'john'
    age: 26
};
var obj2 = obj1;
obj1.age = 30;
console.log(obj1.age); //30
console.log(obj2.age); //30

var age = 27;
var obj = {
    name: 'Jonas'
    city: 'lisbon'
};

function change(a, b){
    a = 30;
    b.city = 'SF'
}

change(age, obj);
console.log(age); //27
console.log(obj.city); //SF
```