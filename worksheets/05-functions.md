# Functions

## The concept

Have you had a situation yet where you need to copy and paste a line of code to use it again?

Function are a way of using separating out code and then using it again and again throughout your program. You've actually already used a couple already… For example `alert('hello world')` runs a prewritten function provided by `JS`. You didn't need to write the code to create the `alert`, `JS` gave it to you for free.

## Trying it out

Here is a _really_ simple function that triggers an `console.log` to say 'hello'

```JS
function sayHello() {
  console.log('Hello, world!');
}
```

Add that to your code and refresh your browser…

You'll be unsurprised that nothing happens. Nothing happens because we haven't run your function.

To run a function you need this code:

```JS
  sayHello();
```

Refresh your page and look in the console… oh look! `Hello, world!`;

Try putting your `sayHello()` function into a [loop](04-arrays-object.md)… you should see your message repeated several times (or a number appearing next to it which indicates that the same message has been looped several times…).

## Taking variables in…

Functions can also take in values and do something with them… you remember that `alert()` takes in a `string` and displays it…

We can modify our `sayHello()` function to take in a name at the same time:

```JS
function sayHello(name) {
  console.log('Hello ' + name);
}
```

Now when you call `sayHello()` you can add a name between the brackets:

```JS
sayHello('Magical Trevor');
```

## Sending something back…

Our `sayHello()` is useful for displaying something, but sometimes we want to change what comes in and send it back so our code can keep on using what the function does…

For example… you may need a function that multiplies two numbers together:

```JS
function multiplyMe(a, b) {
  return a * b;
}
```

What this function does is to take in two numbers (`a` and `b`), multiply them together and return them. Test it out:

```JS
console.log(multiplyMe(2,8));
```

The result should be `16` in your console.

## Challenge

In the [Arrays and Objects](04-arrays-object.md) sheet we gave you the code to get a random item from an array. It looked like this:

```JS
var randomColour = colours[Math.floor(Math.random() * colours.length)];
```

You might have needed to use this line a couple of times… Go back to your code and see if you can improve how it was written using a function or two.

Once you've done that… it's time to learn about magically creating `HTML` with `JS` using [DOM manipulation](06-dom-manipulation.md).
