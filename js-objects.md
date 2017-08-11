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
