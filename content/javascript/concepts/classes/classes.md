Title: 'Classes'
Description: 'JavaScript classes provide a template for creating objects with properties and methods.'
Subjects:

- 'Web Development'
- 'Computer Science'
  Tags:
- 'Classes'
- 'Objects'
- 'OOP'
- 'JavaScript'
  CatalogContent:
- 'introduction-to-javascript'
- 'paths/create-a-back-end-app-with-javascript'

---

A class is a template used to create objects in JavaScript. It defines the properties and methods that objects created from the class can use.

The "class" keyword is used to declare a class. A class can include a "constructor" method, which initializes an object's properties when a new instance is created.

Creating a Class

To create a class, use the "class" keyword followed by a class name. Class names are conventionally written using PascalCase.

The "constructor()" method is called automatically when a new object is created using the "new" keyword.

Example

class Car {
  constructor(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
  }
}

const car1 = new Car('Toyota', 'Corolla', 2022);

console.log(car1.make);
// Output: Toyota

console.log(car1.model);
// Output: Corolla

console.log(car1.year);
// Output: 2022

Class Methods

Methods are functions defined inside a class. They describe actions that objects created from the class can perform.

Methods can access an object's properties using the "this" keyword.

Example

class Dog {
  constructor(name, breed) {
    this.name = name;
    this.breed = breed;
  }

  bark() {
    return `${this.name} says Woof!`;
  }
}

const dog1 = new Dog('Buddy', 'Labrador');

console.log(dog1.bark());
// Output: Buddy says Woof!

In this example, the "Dog" class defines a "bark()" method. The method uses "this.name" to access the name of the object.

Creating Multiple Objects

A single class can be used to create multiple objects. Each object has its own property values while sharing the methods defined in the class.

Example

class Student {
  constructor(name, grade) {
    this.name = name;
    this.grade = grade;
  }

  introduce() {
    return `My name is ${this.name} and I am in grade ${this.grade}.`;
  }
}

const student1 = new Student('Alex', 10);
const student2 = new Student('Sam', 12);

console.log(student1.introduce());
// Output: My name is Alex and I am in grade 10.

console.log(student2.introduce());
// Output: My name is Sam and I am in grade 12.

Here, "student1" and "student2" are separate objects created from the same "Student" class. Each object stores its own name and grade.

