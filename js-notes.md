# JS Notes

**var** local variables (scoped to function)
**const** declared once (can't be reasssigned) - unless it is an array or object
**let** similar to 'var', can be reassigned

### Triple dots (...)

Means "all" in array
`const foo = ['a', 'b', 'c'] console.log(...foo) triple dots returns "a" "b" "c"`

### Static properties

_Static properties_ exist directly on the class (cant be changed). Can call it like:
`class Foo { static bar = 'hello' } console.log(Foo.bar) gives "hello"`

### Class Properties

When declaring prperties of a class, dont have to give var etc
constructor runs when new class instance is declared
`class Cat { name: "Tom" state = { running: true } constructor() { console.log(this.name, this.state.running) } }`

### Object.keys

Object.keys allows you to create an arry that can be looped over of key names from an object

### Boolean conditional

{isAvailable ? 'Add To Order' : 'Sold Out!'}

### Array Methods

.map always creates a new array with the info provided

### Promises

Like an event listener but can either succeed or fail then exit.

- fulfilled promise succeeded
- rejected promise failed
- pending still waiting
- settled completed. Either fulfilled or rejected

**How to create a promise**
`var promise = new Promise(function(resolve, reject) {
// do a thing, possibly async, then…

if (/_ everything turned out fine _/) {
resolve("Stuff worked!");
}
else {
reject(Error("It broke"));
}
});`

**How to use the promise**
`promise.then(function(result) { console.log(result); // "Stuff worked!" }, function(err) { console.log(err); // Error: "It broke" });`

`.then`

takes two arguments. One for the success case and one for the failure case.
