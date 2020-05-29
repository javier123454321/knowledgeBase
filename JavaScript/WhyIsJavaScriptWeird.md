# Why is JS so weird

As far as I understand it (and this is more of an attempt at me
explaining it to myself than anything else) JS is weird by design, as it
was conceived as a tool to make the web interactive. 

Looking through the LearnCode.academy Youtube Videos about this topic,
there are 5 language quirks that make it incredible 

I found this playlist that gives a quick explanation on 5 elements of js:
[Playlist](https://www.youtube.com/watch?v=JEq7Ehw-qk8)


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
//or you can declare it in the argument itself:
callBackDemo(
	regularFunction, 
	regularFunction, 
	()=>{
		console.log("callback declared in the argument");
	})
```
### Output
>
> regularFunction
> functionExpression
> arrowFunction
> 
> regularFunction
> regularFunction
> callback declared in the argument 
>

This is useful for handling click and other events
so if we declare a `handleclick` function, for example:

```js
function handleClick(){
	alert("click happened")
	}

document.getElementById("btn1").addEventListener("click", handleClick);
```

## JS is event-driven
Javascript was built for making the web interactable.
it therefre keeps listeners for certain events, like button clicks,
mouseovers, async responses, and many other quircky things. 

so in the last example:
```js
function handleClick(){
	alert("click happened")
	}

document.getElementById("btn1").addEventListener("click", handleClick);
``` 

this will make it so that handleClick is called everytime a person
clicks button of id `#btn1`. 

This is different than scripting languages where once the program reaches the bottom of the file, it 'dies'. 

In Javascrpit, the alert will not happen UNTIL the button is clicked. 

JS keeps its memory open for events when you instruct it to.

likewise if you run:
```js
var buttonMessage = "button clicked";
console.log("initial set-up");

function handleClick(){
	console.log(buttonMessage)
	}

document.getElementById("btn1").addEventListener("click", handleClick);
```

### Output:
> initial set-up

And after btn1 is clicked:
> button clicked

The second message ("button clicked") is the output after a button click, meaning that the entire file does not have to run from the top again (there is no initial set-up message on the console). Javascript keeps the variable in working memory while there is an event listener for it.

This allows Node to be so performant, making it only call the parts of memory which are necessary to perform for that portion of the application.

