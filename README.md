# Common JS Interview Questions
###A repository of common interview questions and their answers

#### Basic, non-coding based questions

* Explain javascript closures
- Explain event bubbling
- Explain event delegation
- What does apply() do
- What does bind() do
- Explain what the js map function does provide an example
- What is strict mode
- Whats the difference between a promise and a callback

#### Coding based questions

###### What will the output of the following code be?

```
function(){
	var a = b = 3;
});
();

console.log('a defined?' + (typeof a !== 'undefined'));

console.log('a defined?' + (typeof a !== 'undefined'));
```
##### The Answer

`a` will be undefined and `b` will be equal to 3. But why? This function is not running in a `use strict mode`. So what appears to be happening in the code is that 

``` 
var a = b;
var b = 3; 
```

What reads like a simple logic if A then B problem, is in reality,

```
b = 3;
var a = b;

```
In this case scenario `b` is being defined as a global variable, so it has global scope. `a` has a local scope, therefore will be undefined outside of the function.  

- [source 1]()
- [source 2]()
- [source 3]()
- [source 4]()
- [source 5]()
- [source 6]()