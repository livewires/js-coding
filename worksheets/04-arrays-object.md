# Arrays and objects

## Arrays
Arrays are a special type of variable that can store multiple values. The easiest way to create a JavaScript array is using square brackets `[...]` also known as an array literal.

```
var array = [value1, ..., valueX]
```

1. Create an array called `dorms` which stores the names of all the dorms at LiveWires

Each value in the array has an index which tells you where in the array the value is stored. Remember in JavaScript that the first index is always zero. The statement `array[index]` will give you the value located at that index in the array.

2. Use `dorms[1]` to find the 2nd value in your dorms array.
3. Log to the console the 1st value from the array (clue: which index does JavaScript start at?)

## Looping through arrays

We’ve so far used code to find and log to the console single values from the array. If an array is small enough, it would be quite easy to find out many or all the values in an array using the same code repeated but changing each index. However, this would be much less efficient for larger arrays.

A conditional `for` loop can be used to apply methods to multiple values in an array. 

```
for (i = 0, i < 5, i++)
   // code block to be executed
}
```

The first statement `i = 0` sets the variable to be used before the loop starts. The second state `i < 5` indicates the condition(s) in which the loop will run. The third statement `i++` increases the value of the variable i each time the code block in the loop is executed.

For an array there is an alternative way to loop through all the contents as shown below. This will apply the code block for each value in the array.
 
```
for (x in array) {
  // code block to be executed
}
```

4. How could you use one of these for loops to log to the console all the values in your dorms array on separate lines?


## The concept

## Creating an array

## Loop through an array

Console log the results of the array

## Push and pop in and out of arrays

## Objects

An array is a special type of object. Objects much like real life objects have properties, for example an object describing a car could have properties including manufacturer, model, colour, etc. Therefore, many values can be stored in a single object variable, much like an array. However, instead of using an index to find a value, the name of the property can be used.

The easiest way to create a JavaScript object is using curly brackets `{...}`, also known as an object literal.
