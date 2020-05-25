# Why is JS so weird

As far as I understand it (and this is more of an attempt at me
explaining it to myself than anything else) JS is weird by design, as it
was conceived as a tool to make the web interactive. 

Looking through the LearnCode.academy Youtube Videos about this topic,
there are 5 language quirks that make it incredible 

1. **Functions are Objects**
1. **JS is Event-Driven**
1. **JS keeps its state in Memory after a Function has been executed (Closure)**
1. **Scope** allows you to access data declared in the memory of the
parent.


## Functions are objects in Javascript
Actually, almost everything is an object in JavaScript. Arrays are
objects and functions are objects. That makes it so you can declare a
function in many different ways i.e.
```js
function regularFunction(){
	console.log("regularFunction")
	}

var functionExpression = function(){
	console.log("functionExpression")
	}

var arrowFunction = ()=>{
	console.log("arrowFunction")
	}
```

You can pass any of these functions as parameters in other functions.
```js
function callBackDemo(func1, func2, func3){
	func1();
	func2();
	func3();
	}

callBackDemo(regularFunction, functionExpression, arrowFunction);
```
### Output
```js
> regularFunction
> functionExpression
> arrowFunction
```

## JS is event-driven
Javascript was built for making the web interactable.
it therefre keeps listeners for certain events, like button clicks,
mouseovers, async responses, and many other quircky things. 

so if you do the following:
```js
function someFunction(){
	alert("someFunction called")
	};

var a = document.getElementById('button1').addEventListener('click',
someFunction);
```

this will make it so that someFunction is called everytime a person
clicks button a. 

