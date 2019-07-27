# Creating HTML with Javascript (DOM Manipulation)

Back in [forms and events](02-forms-and-events.md) we learnt how to find items in the `HTML` code using this code:

```JS
var htmlElement = document.querySelector('.js-class-name');
```

`JS` knows what the `HTML` looks like because it creates it's own map of the page structure. It calls it the _Document Object Model_ or `DOM` for short. `JS` isn't just able to query elements in the `DOM` and run events on them, it can be used to create new elements, edit existing or delete them entirely.

## Creating new elements

In your `HTML` you need a container to inject a new element into with Javascript. So over in `index.htm` create a new `div` like this:

```HTML
<div class="js-container">
  Hello
</div>
```

Now… the first step in `JS` is to select the new `js-container`.

```JS
var container = document.querySelector('.js-container');
```

Then we need to write some new `HTML` to add to it:

```JS
var newContent = `
  <div>
    <h2>Hello</h2>
    <p>This will be inserted… like magic</p>
  </div>
`
```

Finally add the `newContent` to the `container`:

```JS
container.innerHTML = newContent;
```

Refresh the page and see what happens.

`innerHTML` can also be used to empty a container:

```JS
container.innerHTML = null;
```

You can also use it to append to the end, rather than entirely overwriting the content:

```JS
container.innerHTML += `
  <p>This is another paragraph…</p>
`;
```

## Challenge

With your [form](02-forms-and-events.md) update your event handler so that rather than alerting the name that is entered, it creates a new `<h1>` element with the name on it.

As a stretch task, when you add the name add a button next to it that will allow you to delete it…
