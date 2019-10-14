# 100 Days of Code: Round 1 - John Erickson
### I'm a Software Engineer working in the greater Pittsburgh footprint where I primarily focus on UI/Frontend responsibilities.  

The tech stack I use in my current role:
```javascript
let workTechStack: string[] = ['HTML', 'CSS', 'SASS', 'Bootstrap', 'JavaScript', 'jQuery', 'TypeScript', 'Angular', 'C#'];
```
#### To remain on the page and open a hyperlink in a new browser window use the following shortkeys:
	- Mac: Command + Click 
	- Windows: Controle + Click 

## Over the next 100 days I want to:
- I want to gain a deeper understanding of intermediate/advanced Vanilla JavaScript: 
	- *Functional Programming using pure functions*
	- *Object Oriented Programming*
	- *Closures*
	- *Asynchronous JavaScript using several APIs: callbacks, Promises, async/await*
- Working with Angular for the past several months in a production setting has provided me a solid understanding of fundamentals of the framework, however, I have much to learn and thus I'm investing a lot of my free time w/ online resources to understand intermediate-level concepts: 
	- Udemy course: [Angular 7 (formerly Angular 2) - The Complete Guide](https://www.udemy.com/the-complete-guide-to-angular-2/) by *Maximilian Schwarzmüller*
	- Udemy course: [The Complete Angular Course: Beginner to Advanced](https://www.udemy.com/the-complete-angular-master-class/) by *Mosh Hamedani*
- With having a better understanding of JavaScript frameworks and libraries I hope to start learning React no different than Angular:
	- Udemy course: [The Modern React Bootcamp (Hooks, Context, NextJS, Router)](https://www.udemy.com/course/modern-react-bootcamp/) by *Colt Steele*
- Continue to update my [portfolio](https://johnerickson.netlify.com/) website including new projects which will showcase my abilities and harness the power of *Advanced CSS/SASS*, *Angular*, *Angular Material*, *React*, *RxJS and/or Redux Patterns*, *Node*, *MongoDB* and *C#*. 
- I want to read in full **Clean Code** by *Robert C. Martin*.

---

# Accomplishments:
- 

---

### Day 1: October 12, 2019
**Today’s Progress**:
- I completed *Section 6: Introducing State* in Colt Steele's *The Modern React Bootcamp*.
	- Concepts Learned:
		- How to initialize, set and change state without mutating data.
		
#### What is React State?
In React, State is an instance attribute on a Component. React State is a Plain Old JavaScript Object (POJO).

If your Component is stateless, you can omit the constructor function, however if you're building a Component with state, you need a standard React constructor.

```javascript
import React, { Component } from 'react';

class Pokecard extends Component {
	constructor(props) {
		super(props);
		this.state = {
			// initial state goes here
		};
	}
	
	render() {
		return (
			<div></div>
		)
	}

}
export default Pokecard;
// constructor takes one argument, props
// you MUST call super(props) at the start of the constructor, which registers your class as a React Component
// this.state is React boilerplate and cannot be changed
// anytime a class extends from another you MUST invoke the constructor function of the parent class before you do anything else. In React you do this by invoking the super function
// if you want access to props in the constructor function you MUST pass props into the super function 
```

---

### Day 2: October 13, 2019
**Today’s Progress**:
- Renforcing what I've learned thus far in Colt Steele's *The Modern React Bootcamp* I was able to wrap my [Pokedex game](https://github.com/HeresJohnny5/pokedex).
	- Concepts Learned:
		- JSX
		- React Props
		- Using CSS to style React Components
	
- I was able to update my [LinkedIn](https://www.linkedin.com/in/johnerickson5/), Glassdoor and network with several new Developers and User Experience Designers.

---
