# Arrays and objects

## The concept

So we've seen that Javascript can manipulate things like words and numbers but often we'll find that we actually want to collect those kinds of things into collections. There are two broad concepts here: arrays and objects. Arrays are essentially lists of items (we call them each item an element) and objects are structures that can hold a set of key-value pairs (like a car could have key-values including manufacturer, model, colour, etc - we call each of these properties). Therefore, many values can be stored in a single object variable, much like an array. However, instead of using an index to find a value, the name of the property can be used.

Let's start with arrays...

## Creating an array

The easiest way to create a JavaScript array is using square brackets `[...]` also known as an array literal. Let's create an array called `dorms` which stores the names of all the dorms at LiveWires. Write this in your `script.js` file.

```JS
var dorms = ['durdle', 'bifold', 'gullwing', 'automatic', 'barn']
```

Each value in the array has an index which tells you where in the array the value is stored. We need to remember that in JavaScript that the first index is always zero. The statement `array[index]` will give you the value located at that index in the array.

So for example you can use `dorms[1]` to find the 2nd value in your dorms array.

### Challenge

Log to the console the 1st value from the array (clue: which index does JavaScript start at?)

## Looping through arrays

We’ve so far used code to find and log to the console single values from the array. If an array is small enough, it would be quite easy to find out many or all the values in an array using the same code repeated but changing each index. However, this would be much less efficient for larger arrays.

A conditional `for` loop can be used to apply methods to multiple values in an array.

```JS
for (i = 0; i < 5; i++)
   // code block to be executed
}
```

The first statement `i = 0` sets the variable to be used before the loop starts. The second state `i < 5` indicates the condition(s) in which the loop will run. The third statement `i++` increases the value of the variable i each time the code block in the loop is executed. Here we would need to use the loop index variable (`i`) to access the array value - like `dorms[i]`.

For an array there is an alternative way to loop through all the contents as shown below. This will apply the code block for each value in the array.

```JS
for (x in array) {
  // code block to be executed
}
```

### Challenge

Use one of these for loops to log to the console all the values in your `dorms` array on separate lines?

## Push in and pop out of arrays

Sometimes we actually need to add something else to our array. The easiest way to do this is to use `dorms.push(newElement)`. This will add the new item to the end of the list.

Try adding adding the non-YP dorm `'revolving'` to your dorms list using `push`. Put this before your console logging loop so you see your new element logged out.

We can also take the last-added element out of the array using `pop`.

```JS
var last = dorms.pop();
```

Here, the `last` variable will be the element that is taken out and the array will no longer have that element.

Have a play around with `push`, `pop` and your console logging loop to see what this does. Also try logging out the `last` element when popping.

That's the array basics out the way, now let's look at objects...

## Creating an object

The easiest way to create a JavaScript object is using curly brackets `{...}`, also known as an object literal. Let's create a car object. Put this in your script file.

```JS
var car = {make: 'VW', model: 'Beetle'}
```

## Accessing and modifying properties

You can access properties using a `.` after the object name. So we can use `car.make` to get the result `'VW'` - try this in the console.

We can use this to set the properties too.

```JS
car.model = 'passat';
```

Do this and then log the car to console to see it with the updated property value.

## Challenge

Arrays can also be properties in objects and objects can be in arrays. Let's create an array of objects.

Start by creating an array of colour names.

Then create a different array of car names.

Then, using a loop, like the one above (`for (i = 0; i < 5; i++)`) generate an object that contains a random car name and a random color. The aim is to get an object that looks like this:

```JS
{
  'car': 'ford',
  'color': 'signal orange'
}
```

You can select a random item from an array using this code:

```JS
var randomColour = colours[Math.floor(Math.random() * colours.length)];
```

Once you have created your new object, push it to a `cars[]` array.

After the loop, `console.log()` your `cars[]` array.

### Stretch goals

- Console.log the results of your loop, printing each of the properties with keys and values in a list with a clear separation between each different object.

Let's start playing with the [Document Object Model](05-dom-manipulation.md).
