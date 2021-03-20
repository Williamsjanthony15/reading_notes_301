# ES6

## a way to really dumb down constructors to more of a conversation standpoint rather than a "Coding" stand point. Easier to understand and A LOT more easier to code. Does everything a constructor does but it saves memory and storage which will in turn allow the browser to load faster.


 // **This is a portion of code taken from CodeFellows Assignment "Prep: ES6 Classes", This code does not belong to me. It is strictly being used in a way of notation** // 

 
Prototypal Inheritance
function Animal(name) {
  this.name = name;
}
Animal.prototype.walk = function() {}

function Bird(name) {
  // I can do all the things animals can do!
  Animal.call(this, name);
}
// Unlike other animals, birds can fly
Bird.prototype.fly = function() {}

// Make a new bird ..
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();
ES6 Classes
The same thing with classes (much cleaner!)

function() becomes class {}
call() becomes extends
Classes are standalone, self-contained object (instance) factories
Ultimately, they result in a prototype
But for the developer, they are many orders of magnitude easier to comprehend and work with
class Animal {
  constructor(name) {
    this.name  = name;
  }

  walk() {}
}

// Thanks to 'extends', all birds can now do all things animals can
class Bird extends Animal {
  // Birds can walk, becuase they're animals also do their own thing.
  fly() {}
}

// Make one (the same was as before, but wasn't the class creation much easier?)
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();


 // **This is a portion of code taken from CodeFellows Assignment "Prep: ES6 Classes", This code does not belong to me. It is strictly being used in a way of notation** // 