# Structures and Classes

## structs vs. class

* static methods and properties 
* more on optionals
* __Dictionary<KeyType,ValueType>__
* (time permitting) __UIStackView__ and autolayout

Now, when we create a new Swift file in our project, we're going to name it after the most important methods inside of the respective file. Then when we declare our class, we need to first consider our public API.

An API is just a file of the instance variables and methods we're going to allow to be publically accessible. Other classes can call them.


Structures and Classes are almost the same in Swift! The two major differences:

1. structs have NO inheritance
2. Structs are value types, and classes are reference types.

### What are value types? 

Passed as argument, put it into an array, or assign it to another variable, __it gets copied__. 

Whenever an instance variable is used in a method, a __copy_ of the var is made.

These are all structs:

* array
* ints
* strings
* dictionaries

It doesn't copy all of the bits, it only makes a real copy when it is modified. It's called _copy on write semantics_.

#### What are reference types?

This is what you're used to in other langauges, our instance variable lives on the heap. You have a pointer towards it. When you pass it around, you're not actually passing the data, but a pointer to the data. So you may have a __whole__ bunch of code with pointers to the same object.  

How do we create an array of cards?

var cards = Array<Card>()

    // We could use this syntax:
    var cards: Array<Cards>()
    
    // But more generally we would use this syntax:
    var cards = [Card]()

    Other _init_s array has, reserve capacity for an array, create an array from another array.

Note the parenthesis, these can accept various arguments and these cooresponde with _init_. Much like Python. A special _class_ _method_ called initialization or _init_, and can be used with whatever arguments/multiple arguments. This is an __empty__ array.

Classes get a free init with no arguments, as long as all their vars are initialized.

## Struct

In C 

The free initializer they get is for all _vars_.

## Classes



### Sidenotes to be moved

*  the__\___ keyword is used for loops and stands for nothing, just an empty variable you won't use

```swift
init(numberOfPairsOfCards: Int){
    for _ in 1...numberOfPairsOfCards {
        let card = Card()
        cards += [card,card]
    }
```

* keyword __lazy__ allow you to initalize and use a variable without actually initializing it, until it's eventually used
    + one restriction, you __cannot__ use a _didSet{}

### property observers

Can't be used with _lazy_ vars. There are methods that are called after 
 