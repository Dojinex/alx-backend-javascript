# ES6 Classes
ES6 (ECMAScript 2015) introduced a more structured way to create and work with classes in JavaScript, making it easier to implement object-oriented programming concepts. This guide will cover the basics of defining classes, adding methods, working with static methods, extending classes, and briefly touch on metaprogramming using symbols.

## Resources
**Read or watch:**

- [Classes](https://intranet.alxswe.com/rltoken/ke2dSL31JbpAUBW0qWE9WA)
- [Metaprogramming](https://intranet.alxswe.com/rltoken/6OgF5QGbYclp_cwATfq-0g)

## Table of Contents
- How to Define a Class
- Adding Methods to a Class
- Static Methods
- Extending a Class
- Metaprogramming and Symbols

# How to Define a Class
In ES6, you can define a class using the class keyword. Here's the basic syntax:

"""
class ClassName {
  constructor() {
    // Constructor method
  }

  // Other methods and properties
}

"""
Example
"""
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

"""

## Adding Methods to a Class
You can add methods to a class by defining them within the class block. Methods are functions that can be called on instances of the class.

Example:

"""
class Calculator {
  add(a, b) {
    return a + b;
  }

  subtract(a, b) {
    return a - b;
  }
}

"""

## Static Methods
Static methods are called on the class itself, rather than on instances of the class. They are defined using the static keyword.

"""
class MathHelper {
  static square(x) {
    return x * x;
  }
}

// Usage
const result = MathHelper.square(5); // Returns 25

"""

Static methods are useful for utility functions that are not tied to specific instances.

## Extending a Class
You can create a new class that extends another class using the extends keyword. This is known as inheritance, where the child class inherits properties and methods from the parent class.

"""
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog('Buddy');
dog.speak(); // Outputs: "Buddy barks."

"""

## Metaprogramming and Symbols
Symbols are a new primitive data type introduced in ES6. They can be used to create unique property keys for objects, which is useful for metaprogramming, among other things.

"""
const symbolKey = Symbol('description');

const obj = {
  [symbolKey]: 'This is a symbol property',
};

console.log(obj[symbolKey]); // Outputs: "This is a symbol property"

"""

Symbols allow you to define properties that are not accidentally overwritten or accessed by other parts of your code.
