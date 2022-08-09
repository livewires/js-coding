# Forms and events

As we saw in the first worksheet, `HTML` provides the page structure, while `JS` adds the interaction. A lot of the time we use forms to create interaction…

## HTML form…

Let's add a simple `HTML` form to our page. Go into your `index.html` file and add the following lines in the `<body>` tag. It's really important that these go _before_ the `<script src="script.js"></script>` line:

```HTML
<form>
  <div>
    <button class="submit-button" type="submit">Hello</button>
  </div>
</form>
```

> 💡 **TIP**: when copying code from Github or other sources, it is good practice to check the spacing at the start of each line (indentation) is correct for the where you paste the code into. Do your `form` and `div` tags line up?

Refresh the page and you should have a happy little button. If you click it… very little will happen. But that's fine.

## Adding interactivity with events

`JS` can select items within the `HTML` to provide interactivity with it… Our form is good… but we want something to happen when we click the submit button.

First in our `JS` we need to find the `button`; we do this by using `document.querySelector` and looking for the element's ID:

```JS
var submitButton = document.querySelector('.submit-button');
```

Next we need create an `event`. An event is a trigger that `JS` waits for before running some code. We want to run an event when the button is clicked:

```JS
submitButton.addEventListener('click', function(event) {
  event.preventDefault();
  alert('Hello!');
});
```

By default the page will try and reload when you submit the form, by adding `event.preventDefault();` the default action is prevented.

What will happen instead is an `alert()` will popup with your message!

## Adding a text input

Now add a text field to the form, like this:

```HTML
<div>
  <label for="name">Name:</label>
  <input class="name-field" type="text" placeholder="Type in your name…" />
</div>
```

Remember how we got a variable for the button element, using its ID? We can do the same for the text field:

```JS
var nameField = document.querySelector('.name-field');
```

## Challenge

You now know how to get a variable containing an element (like a button or a text field), and trigger events when a user interacts with them.

Try changing your code so that when the submit button is pressed, the alert greets you by name. So if you've written your name as `"Cow"`, the alert message says `"Hello Cow"`!

All `<input>` elements in `HTML` have `value`s, so we can get what's been typed in the text field using:

```JS
var name = nameField.value;
```

And you can add two strings just like numbers: if you type `"Hello " + "Cow"` the result will be `"Hello Cow"`.

## Next

Next, lets look at [Local Storage](03-local-storage.md).
