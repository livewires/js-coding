# Forms and events

As we saw in the first worksheet, `HTML` provides the page structure, while `JS` adds the interaction. A lot of the time we use forms to create interaction…

## HTML form…

Let's add a simple `HTML` form to our page. Go into your `index.htm` file and add the following lines in the `<body>` tag:

```HTML
<form>
  <div>
    <input class="js-name-form-submit" type="submit" value="Hello" />
  </div>
</form>
```

Refresh the page and you should have a happy little button. If you click it… very little will happen. But that's fine.

## Adding interactivity with events

`JS` can select items within the `HTML` to provide interactivity with it… Our form is good… but we want something to happen when we click the submit button.

First in our `JS` we need to find the `input`; we do this by using `document.querySelector` and looking for the input's `class`:

```JS
var nameFormButton = document.querySelector('.js-name-form-submit');
```

Next we need create an `event`. An event is a trigger that `JS` waits for before running some code. We want to run an event when the button is clicked:

```JS
nameFormButton.addEventListener('click', function(event) {
  event.preventDefault();
  alert('You clicked a button');
});
```

By default the page will try and reload when you submit the form, by adding `event.preventDefault();` the default action is prevented.

What will happen instead is an `alert()` will popup.

Did you see that the submit button had a `value` in it? All input elements in `HTML` have values, and `JS` can read them too:

```JS
var buttonValue = nameFormButton.value();
```

Try modifying your event so that rather than alerting 'you clicked a button' it alerts the the value of the button…

## Challenge

You now know how to select elements with `JS`, get their values, even trigger events when a user interacts with them. Try writing some code that when the submit button is pressed the page pops up an alert saying `Hello #{name}` taking their name from a text input.

You can create a text input like this:

```HTML
<div>
  <label for="name">Name:</label>
  <input class="js-name-field" type="name" placeholder="Type in your name…" />
</div>
```
