# 100 Days of Code: Round 1 - John Erickson
### I attempted to complete 100 Days of Code earlier this year however I fell short 64 days in. While I continued my coding journey dabbling in React, Flutter, and Swift post 64 days, I did not commit daily via GitHub nor on social feed via Twitter feed and thus I'm starting anew. 
## Over the next 100 days I want to:
- Create a portfolio website to showcase my web development talent and personal passion projects. 
- I want to gain a deeper understanding of intermediate/advanced Vanilla JavaScript features: 
	- Functional Programming
	- Object Oriented Programming
	- DOM using Vanilla JavaScript
	- Closures
	- Asynchronous code
- I want to invest dedicated time each and every week in code clinics i.e. *Exercism* 
- I want to gain a deeper understanding of CSS
- I want to continue to learn React
- I want to continue to learn mobile app development in iOS gaining a deeper understanding of Xcode and Swift
- I want to continue to learn mobile app development using Google's Flutter SDK

### Day 1: November 12, 2018
**Today’s Progress**:
I’m currently in the process of making my way through a Udemy course by Angela Yu on [iOS 12 and Swift - The Complete iOS App Development Bootcamp](https://www.udemy.com/ios-12-app-development-bootcamp/). Currently I’m 33% complete and while I’ve learned a lot figure it’s a good time to reinforce what I’ve learned and apply it to a real world application; [iOS 12 weather app](https://github.com/HeresJohnny5/portfolioiOSWeatherApp). While there’s several goals I hope to accomplish within the next 100 days I hope to showcase this weather app on my portfolio site which I hope to complete early next year. 

Wanting to gain a deeper understanding to intermediate JavaScript concepts I spent a little over an hour watching a Lynda.com course by Shaun Wassell: [Learning Functional Programming with JavaScript](https://www.lynda.com/JavaScript-tutorials/Learning-Functional-Programming-JavaScript/585272-2.html). Thus far I’ve learned core concepts of functional programming, what differentiates functional programming and Object-Oriented programming, assigning functions to variables via function expressions, and how you can passing functions as arguments via higher-order functions.

**Today's Thoughts**:
It’s always a daunting task to start learning a new topic, language, and/or framework and while Apple Developer Documentation is vast, I’m still having a difficult time using the resource. Like anything else I’ve learned thus far it’s just a matter of time and continued exposure. 

One of the many thing I continue to love regarding the development community is the infinite amount of amazing resources available, let alone people willing to help. I spent a good portion of the day communicating with peers via Udemy and 100 Days of Code Slack Channel.

---

### Day 2: November 13, 2018
**Today’s Progress**:
While I didn’t have much time throughout work I was able to wrap up Learning [Functional Programming with JavaScript](https://www.lynda.com/JavaScript-tutorials/Learning-Functional-Programming-JavaScript/585272-2.html) by Shaun Wassell, complete several JavaScript code challenges via [Exercism](https://exercism.io/) and start watching a [Recursion Crash Course](https://www.youtube.com/watch?v=lMBVwYrmFZQ) by Colt Steele.

**Today’s Thoughts**:
Knowing that my time would be limited today I decided rather continue my iOS journey to focus on Functional Programming in JavaScript. It’s an amazing feeling, especially for those who are not F/T programmers when you recall how something works e.g. JavaScript Array higher-order functions. While I do recall higher-order function core concepts it was nice to have a refresher on how they work.

I have very minimal exposure to Test Driven Development (TDD) concepts and frameworks and thus it took me a little longer than expected to get started with code challenges via Exercism. While my progress was slow at first it was nice to get exposed to how unit-tests work.

---

### Day 3: November 14, 2018
**Today’s Progress**:
While somewhat unexpected I found myself lost in a code clinic rabbit hole. Today I completed several Exercism.io challenges, brushed up on some core JavaScript concepts and read an interesting article by Stephen Chapman regarding Nested IF/ELSE statements.

**Today’s Thoughts**:
So it’s been a hot minute since I last attempted any code related challenge. While I absolutely love the mental stimulus one obtains when wrestling through a coding exercise it can be extremely frustrating especially when the challenge you face is supposedly an easy exercise. The problem I encountered is called Run Length Encoding (RLE), which challenges the programmer to create a simple form of data compression where consecutive data elements are replaced by just one data value and count.

`"WWWWWWWWWWWWBWWWWWWWWWWWWBBBWWWWWWWWWWWWWWWWWWWWWWWWB"  ->  "12WB12W3B24WB"`

While my solution passed all Exercism.io unit tests I can't help think I overcomplicated the problem. I still have the decoding part of the challenge to solve before submitting my solution.

```javascript
export const encode = (passedStr) => {
	let passedArr = passedStr.split('');
	let arrContainer = [];
	let finalStr = '';
	let compareChar = passedStr[0];
	let count = 0;

	if (passedStr === '') {
		return '';
	}

	for (var i = 0; i < passedArr.length; i++) {
		if (passedArr[i] === compareChar) {
			count++;
	  } else {
			arrContainer.push(count);
			arrContainer.push(compareChar);

			compareChar = passedArr[i];
			count = 1;
	  }
	};

	arrContainer.push(count);
	arrContainer.push(compareChar);

	let finalArry = arrContainer.filter(el => el !== 1);
	finalStr = finalArry.join('');

	return finalStr;
};
```

---

### Day 4: November 15, 2018
**Today’s Progress**:
Today I spent some much needed time reading up on [Swift](swift.org), played around with the [Open Weather Map API](https://openweathermap.org/) using the [Alamofire HTTP networking library](https://github.com/Alamofire/Alamofire) and wrapped up the Run Length Encoding (RLE) challenge, listed above.

**Today’s Thoughts**:
While I felt a great sense of relief being able to complete the Run Length Encoding (RLE) challenge I couldn't get myself to look at other's solutions. Call it fear, maybe a little embarassment that my solution overcomplicates what's listed as an easy challenge. Regardless, I take pride knowing that while it took longer than expected I solved the challenge and learned some new JavaScript tips and tricks along the way.

After taking a mental break I have all intent to review other's code throughout tomorrow. This should allow me the opportunity to reflect let alone learn from others on how they approached the problem.    

```javascript
export const encode = (passedStr) => {
	let passedArr = passedStr.split('');
	let arrContainer = [];
	let finalStr = '';
	let compareChar = passedStr[0];
	let count = 0;

	if (passedStr === '') {
		return '';
	}

	for (var i = 0; i < passedArr.length; i++) {
		if (passedArr[i] === compareChar) {
			count++;
	  } else {
			arrContainer.push(count);
			arrContainer.push(compareChar);

			compareChar = passedArr[i];
			count = 1;
	  }
	};

	arrContainer.push(count);
	arrContainer.push(compareChar);

	let finalArry = arrContainer.filter(el => el !== 1);
	finalStr = finalArry.join('');

	return finalStr;
};
```

---

### Day 5: November 16, 2018
**Today’s Progress**:
Due to encountering a Swift bug regarding Mapping and Geographical Information System (“MGIS”) I was nowhere near as productive today as I'd hope. Regardless, I spent time on Swift docs let alone Stack Overflow. I also started a Lynda course on [Swift 4](https://www.lynda.com/Swift-tutorials/Swift-4-Essential-Training/636121-2.html) by Harrison Ferrone. 

**Thoughts**:
The past couple days have been quite frustrating, between working on code challenges and encountering bugs, however as any programmer well know is part of the job. Being relatively new to Xcode and Swift I feel the process of working through bugs is slow, however I hope with more exposure to both the tool and language it'll get quicker in time.

---

### Day 6: November 17, 2018
**Today’s Progress**:
Rather continue plugging away on the weather app project I decided to spend my time learning more about the Swift programming language using resources i.e. Swift documentation, Swift 4: Essential Training and most important trial and error using Xcode's playground.

**Today's Thoughts**:
While I'm not a programmer by trade I got interested in programming after starting to learn JS. I'm really enjoying learning the differences between static and dynamic languages and unique Swift Collections e.g. Dictionaries, Sets, and Tuples.

- [Dictionary](https://developer.apple.com/documentation/swift/dictionary): A collection whose elements are key-value pairs.
- [Set](https://developer.apple.com/documentation/swift/set): An unordered collection of unique elements. A Set stores distinct values of the same type in a collection with no defined ordering. You can use a set instead of an array when the order of items is not important, or when you need to ensure that an item only appears once. 
- [Tuple](https://medium.com/swift-programming/swift-tuple-328aecff50e7): A tuple type is a comma-separated list of zero or more types, enclosed in parentheses.

---

### Day 7: November 18, 2018
**Today’s Progress**:
Today I refactored my first Exercism.io JS challenge based on feedback I got from a Mentor, not to mention complete the RNA-Transcript challenge. The only real challenge I encountered with the RNA-Transcript challenge was understanding how to pass a test which meant to throw an error. I spent some time learning about Application Control Flow in Swift using the guard statements.

**Today's Thoughts**:
It's becoming more and more interesting comparing one programming language to another, especially when comparing a dynamic vs static language. 

- [Guard Statement](https://medium.com/@chris_dus/the-guard-statement-in-swift-fdad41b08798): A guard statement is used to transfer program control out of a scope if one or more conditions aren’t met.
- [Swift Functions](https://docs.swift.org/swift-book/LanguageGuide/Functions.html)

*Function Parameters and Return Values*
```javascript
func sayHelloWorld() -> String {
    return "hello, world"
}
print(sayHelloWorld())
// Prints "hello, world"
```

---

### Day 8: November 19, 2018
**Today’s Progress**:
Today I dug deeper into Swift learning about Swift functions i.e. Overloading, Function Types, etc. I also started yet another code clinic challenge via Exercism.io. While I was able to get the code to work as expected using Google's Developer Tools I was unable to get the tests to pass.

**Today's Thoughts**:
So unlike JavaScript, Swift allows you to have multiple functions with the same name, as long as their function type or signature is different. When you have multiple functions with the same name it's called *overloading a function*. It's really useful in cases when you may need consistent functionality, but with different inputs and outputs.

```javascript
func greeting() {
    print("Hello There.")
}

func greeting(name: String) {
    print("Hello \(name).")
}

func greeting(firstName: String, lastName: String) -> Void {
    print("Hello \(firstName) \(lastName).")
}

greeting()
greeting(name: "John")
greeting(firstName: "John", lastName: "Erickson")
```
