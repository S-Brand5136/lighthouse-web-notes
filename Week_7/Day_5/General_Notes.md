# Notes

### Spread operator

- Copying an Object

```Javascript
  const original = { one: 1 };
  const bad = original;
  const good = { ...original };

  console.log(original === original); // true
  console.log(original === bad); // true
  console.log(original === good); // false
```

- Adding to an Object

```js
  const original = { one: 1 };
  const copy = { ...original, two: 2 };

  console.log(original === copy); // false

  /* original */
  {
    one: 1
  }

  /* copy */
  {
    one: 1,
    two: 2
  }
```

- Updating an Object

```js
  const original = { one: 1, two: 3 };
  const copy = { ...original, two: 2 };

  console.log(original === copy); // false

  /* original */
  {
    one: 1,
    two: 3
  }

  /* copy */
  {
    one: 1,
    two: 2
  }
```

- Merging Multiple Objects

```javascript
  const first = { one: 1 };
  const second = { two: 2 };
  const copy = { ...first, ...second };
  {
  one: 1,
  two: 2
  }
```
