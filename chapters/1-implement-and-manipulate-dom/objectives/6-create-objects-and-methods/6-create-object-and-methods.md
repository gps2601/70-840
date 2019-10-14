### Create and implement objects and methods

Two typs of objects in javascript:

- native objects (provided by js)
- custom objects (developers create to represent their own data constructs)

You can base objects on other objects in which they inherit behaviour.

#### Implementing native objects

static vs non static objects (instance vs global)

The 'new' keyword is used for instantiating new objects.

Multiple constructors is known as an overload constructor.

#### Creating custom objects

Create custom objects to encapsulate functionality.

A prototype provides a definition ot the object so you can create the object using the new keyword.

The following creates a prototype for the book object:

```
function Book(){
    this.isbn = '5555'
    this.lenth = 200
    this.flipTo = function FlipToPage(pnum){
        this.currentPage = pnum;
    }
}
```

Everything in Javascript is an object, each object is based on a prototype.

Objects can contain other objects if needed.

Set and objects prototype using this...

```
Book.prototype = {
    firstName: "",
    secondName: ""
    ....etc
}
```


#### Implementing inheritance

If the object has an "is-a" relationship, it is a candidate for inheritance (inherit from a supertype)

You can extend objects in Javascript...

```
var popupBook = Object.create(Book.prototype, 
                { hasSound: {value: true},
                showPopUp:{ value: function  showPop(){
                    /// logic here
                }}
    })
```

The first parameter takes the object too extend.

The Second parameter is a list of additional properties to extend it with.

...or, you can extend like this

```
function PopUpBook() {
    Book.call(this)
}
PopUpBook.prototype = Book.prototype;
PopUpBook.prototype.hasSound = false;

```

This now extends Book and adds its own functionality.