# Splicing arrays

We've already seen that is it easy to add to the end of an array with `array.push('value')` and remove things off the end of an array with `array.pop()`. However sometimes you need to manipulate arrays with more control; doing things change their contents, remove items, add items places that are not at the end…

Enter `splice()`…

## Splice

To quote [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice):

> The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

Say that you have an array of colours like this:

```JS
var colours: [
  'red',
  'yellow',
  'teal',
  'blue',
  'indigo',
  'violet'
]
```

Suddenly you realise that you've missed your favourite colour; where is orange? It needs to be added after red… This is where `splice` is helpful.

```JS
array.splice(start_index, delete_count, value_to_add);
```

- `start_index` is the position in the array that you want to start editing the array. Remember that in `JS` arrays start counting from `0`, not `1`.
- `delete_count` is useful for when you want to remove a number of items from an array. If you don't want to remove anything… just leave it at `0`.
- `value_to_add` is an optional value that you can include when you want to add something to the array.

## Challenge…

So with this in mind… how would you go about adding `orange` into the correct place in the `colour` array?

```JS
colours.splice(start_index, delete_count, value_to_add);
```

Similarly… how might you swap the word `teal` to `green`?
