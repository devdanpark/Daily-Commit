# Class in Javascript(ES6)
(source from 'you don't know js')

## CLASS

``` javascript
class Widget {
    constructor(width, height) {
        this.width = width || 50;
        this.height = height || 50;
        this.$elem = null;
    }
    render($where) {
        if(this.$elem) {
            this.$elem.css( { 
                width: this.width + "px";
                height: this.height + "px";
            }).appendTo( $where );
        }
    }
}

class Button extends Widget {
    constructor(width, height, label) {
        super( width, height );
        this.label = label || "Default";
        this.$elem = $("<button>").text( this.label );
            }
            render($where) {
                super.render( $where );
                this.$elem.click( this.onClick.bind( this ));

            }
            onClick(evt) {
                console.log( "Button " + this.label + "clicked!");
            }
    }
```
- No more referrence to .prototype cluttering the code.
- Button is declared directly to "inherit" from Widget.(Not using Object.create(...))
- super(...) now gives us a very helpful relative polymorphism capability, so that any method at one level of the chain can refer relatively one level up the chain to a method of the same name.
- class literal syntax has no affordance specifying properties. 
- extends lets you extend even built-in object(sub) types such as Array.

``` javascript
class P {
    foo() {console.log("P.foo");
    }
}

class C extends P {
    foo() {
        super();
    }
}

var c1 = new C();
c1.foo(); //"P.foo"

var D = {
    foo: function() {console.log("D.foo");
    }
};

var E = {
    foo: C.prototype.foo
};
// Link E to D for delegation
Object.setPrototypeOf( E, D );
E.foo(); //"P.foo"
```
