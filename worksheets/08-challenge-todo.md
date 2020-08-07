# Challenge: ToDo List

Using what you have learnt over these work sheets work out how to make a to-do list tool…

## The to-do list tool should be able to:

1. Accept new to-do items through an input field and then store it in [Local Storage](03-local-storage.md)
2. Display a list of each of the items in the to-do list
3. Allow the user to complete a task (this would remove the item from Local Storage)

## Stretch goals

- Could you make the list keep the completed tasks, but visually show that they are complete?
- If you have done the `HTML` and `CSS` course; could you add `CSS` to improve the layout and design of the to-do list?

Done this? Well done! But there's another one! - [Challenge 2: Scoreboard](09-challenge-scoreboard.md).

## Helpful extras

Local Storage can only contain strings (i.e. plain text). This means that if you wanted store an array in it you'll need to first convert it into a string...

To convert an array into a string you need to `stringify()` it:

```JS
var arrayToString = JSON.stringify(['one','two','three']);
localStorage.setItem('number', arrayToString);
```

When you need to read what you put into Local Storage back out, you'll need to `parse()` into an array:

```JS
var numberArray = JSON.parse(localStorage.getItem('numbers'));
```

You can read more about this process here: [MDN - Stringify](<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify#Example_of_using_JSON.stringify()_with_localStorage>)
