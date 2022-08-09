# Hello World

One of the first tasks that everyone does when learning a new programming language is to get the program to say 'Hello World'. It's a good place to start.

JavaScript (`JS`) runs in a web browser, so before we can start writing `JS` we need to first create a web page (an `HTML` file). Then, with the `HTML` we can include our `JS`.

## Setup

### At LiveWires

Open up the code editor (for example, VS Code) on the PC you are using and open up your named folder. Create a file named `index.html` in your named folder.

<details>
  <summary>If you're doing this at home…</summary>

### Glitch

If you are doing this course outside of LiveWires, you can use a website called Glitch that allows you to write code and share it with people very easily.

For this worksheet, you're going to need a Glitch project. This will be based on our starter project. Navigate to [glitch.com/~livewires-01-hello-world](https://glitch.com/~livewires-01-hello-world), and "remix" the project to create your own copy that you can edit:

![Remixing glitch project](img/glitch-remix.png)

You should now have a new Glitch project with four files in:

- `.env` (This can be ignored)
- `README.md`
- `index.html`
- `script.js`

Note: anonymous projects expire on Glitch after 5 days. If you wish to keep your code after LiveWires, you will need to either download the code, or create an account.

</details>

## Hello World in HTML…

If you have done the Web Building LiveWires course this will be _very_ familiar to you.

Open up the file called `index.html`. Then inside your `HTML` file write the following:

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

Open your `index.html` file in the web browser - this can be done by navigating to the file in your PC's file explorer/manager, right-clicking the file, click `Open with`, and select your web browser of choice.

> If using Glitch, click `Preview` at the bottom of the Glitch window and select `Open preview pane`.

You should get a blank page on the right-hand side of the screen. Nothing special there.

Time to fix that. Everything that appears on a web page gets added in between the two `<body>`...`</body>` tags. Between those two tags add:

```HTML
  <h1>Hello World</h1>
```

Either press F5 or click the refresh page button in your browser (If using Glitch, it should automatically refresh the preview pane).

## Hello world in JavaScript…

Right, that's a good start… but `HTML` is not `JS`. HTML gives structure to a webpage, but `JS` makes it interactive.

First, create a file called `script.js` (for example in VS Code, right-click on the left hand pane and select `New file`)

Next in your `script.js` file add the line…

```JavaScript
console.log('Console message!');
```

Save that, press the refresh button on the `index.html` webpage in your browser, and open up the browser console again. Normally this is F12, or right click on the page and select `Inspect`. It might help to hide errors and warnings. Can you spot the `Console message!` message?

No? Nothing happened because `index.html` doesn't know about `script.js` We need to let the `HTML` know that `script.js` exists. We can do that by adding a `<script>` tag to the `HTML`.

Go back into `index.html` and update the contents of `<body>`:

```HTML
  ...
  <body>
    <h1>Hello World</h1>
    <script src="script.js"></script>
  </body>
</html>
```

> ⚠️ It's _really_ important for these worksheets that the script is the very last thing before the closing `</body>` tag. When adding more `HTML` always add it above the `<script>` tag.

Now when you reload the preview you should see the `Console message!` displayed in the console section.

## Explore

Experiment with putting different content inside the brackets of the function call `console.log()`.

Try putting in some simple maths like `1 + 1`…

Now let's look at some [Forms and Events](02-forms-and-events.md).
