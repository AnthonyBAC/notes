1. **Variables**
	1. **`let`:**
	    1. Reassignment is allowed
	    2. No need for an initial value
	    3. Value can change over time
        
	2. **`const`:**
	    1. Reassignment is not allowed
	    2. Must be initialized with a value
	    3. The variable itself can’t be reassigned, but object or array contents can be mutated

2. Functions
	1. Functions use parameters and arguments.
		**Parameters** are the names listed inside the parentheses `()` in the function declaration. They act as **placeholders** for the values the function will receive.
		**Arguments** are the **actual values** passed to the function when it is called. These values replace the parameters.

```javascript
function favoriteAnimal(animal) {
    return animal + " is my favorite animal!"
}

console.log(favoriteAnimal('Goat'))
```
