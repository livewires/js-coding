# Programming basics

# Variables
Try typing this on the console:

```
var a = 17;
```

You’ll see that it returns the value as `undefined`. undefined just means that the thing you typed doesn’t really have a value. However, this did something else: it created a variable named `a`.

Now try typing `a` on the console. You should see that you get back

1. Variables are a way of giving names to values so that you can use them later.

Try typing these:

```
var b = 12;
var c = a + b;
```

Now look at the values of b and c. See how it’s storing the values of these expressions?

A line starting with `var` is a variable definition. You should use this whenever you are creating a new variable.

You can also change the value of a variable. That’s why it’s a “variable”: because its value can vary. Try this:

```
b = 2;
```

Notice that you don’t have `var` this time. If you just have a variable name, an equals sign, and an expression, then this is a variable assignment, which changes the value of a variable that you defined earlier.

You’ve just changed the value of `b`. Remember that you defined `c` to be `a + b`? Look at `c` again and see if it has changed.

You should see that `c` has stayed the same. Now try assigning it again:

```
c = a + b;
```

See that it’s changed this time? This is because the expression `a + b` is converted into its value immediately when it is used.
