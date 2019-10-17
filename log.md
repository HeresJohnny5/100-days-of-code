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

#### Setting State Correctly
You never want to manipulate the State directly instead you want to go through React's ```setState()``` function, which is a built-in React method for changing a Component's state. Think of ```setState()``` as a request rather than an immediate command to update the Component. For better perceived performance, React may delay it, and then update several Components in a single pass. React does not guarantee that the state changes are applied immediately.

You can call ```setState()``` in any instance method **except the constructor**. The constructor function is meant to initialize a Component's state, not change it. 

The ```setState()``` function takes an object describing the state change and patches the state object. Keys that you do not specify will not change.

```javascript
import React, { Component } from 'react';

class Button extends Component {
	constructor(props) {
		super(props);
		this.state = {
			gameStart: true,
			gameValue: 1,
		}
	}

	clickRandomNum = () => {
		let randomNum = Math.floor(Math.random() * 10) + 1;
		
		if (this.state.gameValue === 7) {
			this.setState({ gameStart: false, gameValue: randomNum });
		} else {
			this.setState({ gameStart: true, gameValue: randomNum });
		}
	};
	
	render() {
		return (
			<div>
				<h1>Number is {this.state.gameValue}</h1>
				{this.state.gameValue === 7 ?
					<p>You Win!</p> :
					<button onClick={this.clickRandomNum}>Random Number</button>
				}
			</div>
		);
	}
}
export default Button;
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

### Day 3: October 14, 2019
**Today’s Progress**:
#### Updating existing state
If a call to ```setState()``` depends on *current state* the safest thing is to use the alternative **callback form**. Instead of passing an object, pass ```setState()``` a callback with the current state as a parameter. The callback should return an object representing the new state.

```javascript
import React, { Component } from 'react';

class Button extends Component {
	constructor(props) {
		super(props);
		this.state = {
			kills: 0
		}
	}
	
	clickUpdateKills = () => {
		this.setState(this.incrementKills(this.state));
	};
	
	incrementKills = (currentState) => {
		return { kills: currentState.kills + 1 };
	}
	
	render() {
		return (
			<div>
				<h1>Number is {this.state.kills}</h1>
				<button onClick={this.clickUpdateKills}>Kills</button>
			</div>
		);
	}
}
export default Button;
```

### Day 4: October 15, 2019
**Today’s Progress**:
- Today I started up a small React application based on a [lotto](https://github.com/HeresJohnny5/react-lotto) game to help reinforce my understanding of React state and how to update existing state.
- I also made several small updates to my portfolio.

### Day 4: October 16, 2019
**Today’s Progress**:
- Today I spent the entirety of the night prepping for a technical phone screening for a UI Developer role.
- For anyone looking to gain a deeper understanding of JavaScript core concepts, please check out Web Developer / Tech Writer[Sukhjinder Arora Bits and Pieces at ](https://blog.bitsrc.io/@Sukhjinder). I read his articles on:
	- **Understanding Execution Context and Execution Stack in JavaScript**
	- **Hoisting in Modern JavaScript - let, const, and var**
	- **Undertanding Closures in JavaScript**
	- **Understanding Asynchronous JavaScript**
	- **Understanding Scope and Scope Chain in JavaScript**

### Day 4: October 17, 2019
**Today’s Progress**:
