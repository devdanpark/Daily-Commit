# Exception(try, catch, finally)
- example
``` javascript
var i = 1;
try {
    i = i * j
} catch(e) {
    console.log(e.message)
} finally {
    console.log('process done')
}
// j is not defined
// process done
```
- finally can be ommitted
- We need to avoid using catch ~ try in a loop.

## throw
``` javascript
var x = 1
var y = 0
try{
    if(y === 0)
    {
    trhow new Error('tried to divide into 0')
    }
        var z = x / y
    }catch(e){
        console.log(e.message)
    }
}
//output : tried to divide into 0
```
