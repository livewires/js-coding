# Hello World

One of the first tasks that everyone does when learning a new programming language is to get the program to say 'Hello World'. It's a good place to start.

JavaScript (`JS`) runs in a web browser, so before we can start writing `JS` we need to first create a web page (an `HTML` file). Then, with the `HTML` we can include our `JS`.

## Hello World in HTML…

If you have done the Web Building LiveWires course this will be _very_ familiar to you.

Open up your text editor (like Visual Studio Code, or Sublime text)and create a new file called `index.html`. Then inside your `HTML` file write the following:

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
  </head>

  <body>

  </body>
</html>
```

Now head to your web browser and open the `HTML` file that you have created.

You should get an blank page. Nothing special there.

Time to fix that. Everything that appears on a web page gets added in between the two `<body>`...`</body>` tags. Between those two tags add:

```HTML
  <h1>Hello World</h1>
```

Save the file and refresh your page.

## Hello world in JavaScript…

Right, that's a good start… but `HTML` is not `JS`. HTML gives structure to a webpage, but `JS` makes it interactive.

First, in the same folder as your `index.htm` file, create a new file called `script.js`.

Next in your `script.js` file add the lines…

```JavaScript
  alert('Alert!');
  console.log('Console log!');
```

Save that, and head back to your browser and refresh the page…

Nothing happened because `index.html` doesn't know about `script.js` We need to let the `HTML` know that `script.js` exists. We can do that by adding a `<script>` tag to the `HTML`.

This tag can be put in almost anywhere in the `HTML` tag, but to keep everything clean and separate we'll put it as the last thing before the closing `</body>` tag. Go back into `index.html` and update the contents of `<body>`:

```HTML
  ...
  <body>
    <h1>Hello World</h1>
    <script src="script.js"></script>
  </body>
</html>
```

Now when you reload the page you should get an alert that says 'Alert!' But what about the line `console.log()` that we added? That isn't seen on the page, but is hidden in the Javascript console. We'll be using this a lot in the future… Go into your browser, right click on the page and select `inspect`. In the window that appeared you should see the text `Console log!` displayed in the console section.

## Explore

Experiment with putting different content into `alert()` and `console.log()`.

Try putting in some simple maths like `1 + 1`…


Now let's look at some [Forms and Events](02-forms-and-events.md).