# Programming basics

Here we are going to introduce a few basics of programming to help before you start on the first worksheet. We are going to be using Javascript as our language so let's talk about that first...

## Javascript
JavaScript (`JS`) runs in a web browser, and gives interactivity to webpages. This means we are going to mostly be using our browser to see the results of our code. The other thing we need is the browser console. This shows us logging output that we want to see while we're writing our code but we don't want visible on the webpage. We can get this up in our browser by (in most browsers) hitting F12 or right-clicking on a webpage and clicking "Inspect" (or similar, depending on your browser).

## Variables
Try typing this on the console:

```js
var a = 17;
```

You’ll see that it returns the value as `undefined`. undefined just means that the thing you typed doesn’t really have a value. However, this did something else: it created a variable named `a`.

Now try typing `a` on the console. You should see that you get back

1. Variables are a way of giving names to values so that you can use them later.

Try typing these:

```js
var b = 12;
var c = a + b;
```

Now look at the values of b and c. See how it’s storing the values of these expressions?

A line starting with `var` is a variable definition. You should use this whenever you are creating a new variable.

You can also change the value of a variable. That’s why it’s a “variable”: because its value can vary. Try this:

```js
b = 2;
```

Notice that you don’t have `var` this time. If you just have a variable name, an equals sign, and an expression, then this is a variable assignment, which changes the value of a variable that you defined earlier.

You’ve just changed the value of `b`. Remember that you defined `c` to be `a + b`? Look at `c` again and see if it has changed.

You should see that `c` has stayed the same. Now try assigning it again:

```js
c = a + b;
```

See that it’s changed this time? This is because the expression `a + b` is converted into its value immediately when it is used.

## Functions

Start by typing this on the console:

```JS
function sayHello() { console.log('Hello!'); }
```

It won’t do anything just yet. This thing is a function definition. You can recognise it because it starts with the word `function`. It creates a new function named `sayHello`.

Now try typing this:

```JS
sayHello();
```

This thing is a function call. You can recognise it because it’s a name with `()` immediately afterwards. Try calling sayHello again.

Let’s make a larger function:

```JS
function conversation() {
  sayHello();
  console.log('How are you?');
  console.log('Goodbye');
}
```
(You can use Shift+Enter to write on a new line without running the code.)

Try calling the `conversation()` function on the console. See how it did all three things in order? Functions are lists of things to do. When you call the function, it does all the things in its definition.

You will see more about functions [later on](05-functions)

## Statements
We’ve been putting semicolons `;` in various places. A semicolon marks the end of a statement. So far we have been writing one line for each statement, but this is not required. With a few exceptions, you can add extra spaces and newlines anywhere you like. The following statements all mean exactly the same thing:

```JS
console.log('How are you?');
```
```JS
console.log(
  'How are you?');
```
```JS
console.log(
  'How are you?'
);
```

Use spaces and newlines to make your program easy to read. When you’re just starting out, it won’t be immediately clear to you what makes things easier to read, so just try to follow the patterns that we use in the tutorials. As you read and write more programs this will start to make sense to you.

## Comments

Sometimes we want to be able to write something in our code file without Javascript trying to execute it. This might be to help explain something (so we or others can understand it later) and to remind us that what we wanted to do later. We also use them in our courses so that we can show you where you need to put things in code examples.

To write a comment, start the line with double slash `//`. Anything you write after this on that line will be ignored when the code is run.

```JS
// this is a comment
this is not a comment and will cause errors
var example // you can also write comments at the end of lines
```

You can also write a multi-line comment, though we probably won't use this in this course. You can do this using `/*` to start and `/*` to end.

```JS
/* This is a multi-line comment
We can use this for longer pieces of text
*/
var thing
```


Now you can go onto [Hello World](01-hello-world.md).
