# Local Storage

## The concept

Local Storage allows you to save user data in the browser. This means that if the user closes the browser window, the next time they go back to that webpage you can still access the content they entered.

In this example we're going to store the name `Bob` in LocalStorage and then retrieve it to display it.

## Writing to Local Storage

In your `script.js` file add a new line as follows:

```JS
localStorage.setItem("name", "Bob");
```

This does what it says on the tin, it creates a record identified with the key `name` and sets the value of `Bob`.

## Checking it has worked…

Now when you refresh your page nothing obvious happens…

However if you open up the Chrome inspector and navigate to `Application` > `LocalStorage` you'll be able to see the the key and value listed out.

## Getting it back out…

That's all well and good to see it in the inspector… but it's more helpful to be able to read it back out on to a page.

When you created local storage you used `setItem`. To get an item out you need to `getItem`:

```JS
localStorage.getItem("name");
```

This will fetch the data with the key of `name`. Try wrapping that in an `alert()`…

## Deleting it…

As you can `setItem` and `getItem`, you can remove an item with the `removeItem` function:

```JS
localStorage.removeItem("name");
```

## Updating local storage

Updating local storage is easy - you just set it again.

```JS
localStorage.setItem("name", "Tom");
localStorage.setItem("name", "Harry");
localStorage.setItem("name", "Susan");
```

After running these three lines `name` will be set to Susan.

## Challenge

In the last worksheet you explored [forms and events](02-forms-and-events.md).

1. Make an text input asks the user's name, stores it to Local Storage
2. Add a button which deletes the `name` from Local Storage

Once you've done those, move onto [Arrays and Objects](04-arrays-objects.md).