# Sprint Challenge: JavaScript Fundamentals

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a survey of problems. This Sprint explored JavaScript Fundamentals. During this Sprint, you studied variables, functions, object literals, arrays, this keyword, prototypes, and class syntax. In your challenge this week, you will demonstrate proficiency by completing a survey of JavaScript problems.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in JavaScript fundamentals.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

You will notice there are several JavaScript files being brought into the index.html file.  Each of those files contain JavaScript problems you need to solve.  **If you get stuck on something, skip over it and come back to it later.**

In meeting the minimum viable product (MVP) specifications listed below, you should have a console full of correct responses to the problems given.

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

**Edit this document** to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

---

1. Describe the biggest difference between `.forEach` & `.map`.

- `.foreach()` executes a given callback function once for each element in a given array transforming the contents of the array or using their contents for a specific task. `.map()`, just like the previous function, executes a given callback function once for each element in the given array. However, it is different in that it actually creates a new array with the results of the callback function and returns the newly created array.

2. What is the difference between a function and a method?

- Practically speaking functions and methods are the same thing, snippets of code that perform a specific task. Methods though are functions which are properties of a given object. Example:
```javascript
// This is a function.
// This function will return a random integer between the maximum and minimum values provided (inclusive).
function rndInt(min, max) {
  return Math.floor(Math.random() * (max - min+1)) + min;
}
// This is a Class.
// This class extablishes certain values based on provided information and provides methods to return some string representations of the information.
class Person {
  constructor(obj) {
    this.firstName = obj.firstName;
    this.lastName = obj.lastName;
    this.favLanguage = obj.favLanguage;
    this.catchPhrase = obj.catchPhrase;
  }
  // This is a method!
  introduce() {
    return `Hi! I'm ${this.firstName} ${this.lastName} and my favorite programming language is ${this.favLanguage}.`;
  }
  // This is a method too!
  speak() {
    return `${this.catchPhrase}`;
  }
}

const person = new Person({
  firstName: `Eric`,
  lastName: `SarragaLugo`,
  favLanguage: `JavaScript`,
  catchPhrase: `This is a generic catchphrase.`
});
//This is how we use a method.
console.log(person.introduce());
//Here we use the method and a regular function.
for (let i=0; i<rndInt(1, 5); i++) {
  console.log(person.speak());
}
```

3. What is closure?

- Closure is a feature of JavaScript (not exclusive to JavaScript) where a written inner function has access to a wrapping function's variables (if any), its own variables and, of course, global variables. In essence the function, when stored, remembers the environment it was created in. This feature allows you to create things like function factories.

4. Describe the four rules of the 'this' keyword.

- Window Binding: In the absense of any other form of binding, the `this` keyword defaults to the window object.
- Implicit Binding: When contained within an object the `this` keyword is implied to represent the parent object to the location of `this`. In other words, if you were to invoke a method within the parent function `this` represents whatever is to the left of the `.` (e.g. character in `character.speak();`).
- Explicit Binding: The `this` keyword can be bound to a specific (explicitly stated) object by using the `.call()`, `.apply()`, and `.bind()` functions.
- New Binding: When creating a new object via a constructor the `this` keyword binds to the newly created object.

5. Why do we need super() in an extended class?

- The `super` keyword is used to access functions in the parent element. This is relevant when extending a parent class because `super(obj);` is essentially like calling the parent's constructor method within the child.

---

## Project Set up

Follow these steps to set up and work on your project:

- [x] Create a forked copy of this project.
- [x] Add PM as collaborator on Github.
- [x] Clone your OWN version of Repo (Not Lambda's by mistake!).
- [x] Create a new Branch on the clone: git checkout -b `<firstName-lastName>`.
- [x] Create a pull request before you start working on the project requirements.  You will continuously push your updates throughout the project.
- [x] You are now ready to build this project with your preferred IDE
- [x] Implement the project on your Branch, committing changes regularly.
- [x] Push commits: git push origin `<firstName-lastName>`.

Follow these steps for completing your project:

- [x] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo).
- [ ] Add your Project Manager as a Reviewer on the Pull-request
- [ ] PM then will count the HW as done by  merging the branch back into master.


## Minimum Viable Product

Your finished project must include all of the following requirements:

**Pro tip for this challenge: If something seems like it isn't working locally, copy and paste your code up to codepen and take another look at the console.**

## Task 1: Objects and Arrays
Test your knowledge of objects and arrays. 
* [ ] Use the [objects-arrays.js](challenges/objects-arrays.js) link to get started.  Read the instructions carefully!

## Task 2: Functions
This challenge takes a look at callbacks and closures as well as scope. 
* [ ] Use the [functions.js](challenges/functions.js) link to get started. Read the instructions carefully!

## Task 3: Prototypes
Create constructors, bind methods, and create cuboids in this prototypes challenge.
* [ ] Use the [prototypes.js](challenges/prototypes.js) link to get started. Read the instructions carefully!

## Task 4: Classes
Once you have completed the prototypes challenge, it's time to convert all your hard work into classes.
* [ ] Use the [classes.js](challenges/classes.js) link to get started. Read the instructions carefully!

In your solutions, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

There are a few stretch problems found throughout the files, don't work on them until you are finished with MVP requirements!

---

### This fork is maintained by: Eric SarragaLugo