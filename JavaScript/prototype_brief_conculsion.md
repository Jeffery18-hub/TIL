## Brief Overview of JavaScript Prototype

In JavaScript, a prototype is a fundamental concept central to the prototype-based inheritance model of the language. It is an object from which other objects inherit properties and methods.

JavaScript 规定，每个函数都有一个`prototype`属性，指向一个对象。

总结一下，原型对象的作用，就是定义所有实例对象共享的属性和方法。这也是它被称为原型对象的原因，而实例对象可以视作从原型对象衍生出来的子对象。

### Key Characteristics of Prototypes:



1. Prototype Object

   - Every JavaScript function has a `prototype` property (except arrow functions) that is used when creating instances from that function using `new`. This `prototype` property is an object from which all instances of the function will inherit.



2. Prototype Chain

   - Each object in JavaScript has an internal link to another object, called its prototype. This linked object has its own prototype, forming a chain that ends when a null prototype is reached.

   - When a property or method is accessed on an object, JavaScript will look up the property on the object itself. If not found, it will search the object’s prototype, then the prototype’s prototype, and so on, until the property is found or the end of the prototype chain is reached.



3. Inheritance

   - Prototypal inheritance allows an object to inherit properties and methods from another object (its prototype). This is different from classical inheritance where classes inherit from other classes.



4. Prototype Property vs. `__proto__`

   - The `prototype` property is a property of a function and is the prototype of objects constructed by that function.

   - Each object has a `__proto__` property (though it’s considered deprecated in favor of `Object.getPrototypeOf()`) that points to the prototype from which it directly inherits.



5. Uses:

   - Prototypes are used for defining properties and methods that should be shared by all instances of a class.

   - They provide a way to implement inheritance and share functionalities across objects.



###  Example



Here's a simple example to demonstrate prototypes in JavaScript:



```js
function Animal(name) {
    this.name = name;
}

Animal.prototype.speak = function() {
    console.log(`${this.name} makes a noise.`);
};

const dog = new Animal('Rex');

dog.speak(); // Output: Rex makes a noise.```
```



In this example, `speak` method is defined on `Animal.prototype`, so all instances of `Animal` (like `dog`) inherit and share the `speak` method.



Understanding prototypes is crucial for working with JavaScript effectively, especially for object creation and inheritance.

