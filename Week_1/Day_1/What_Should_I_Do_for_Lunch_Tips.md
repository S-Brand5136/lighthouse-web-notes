### Tips

Try experimenting with the comparison operators (`<`, `>`, `===`, etc.) in the node REPL, which you can launch using the `node` command in Vagrant.

Work on your code iteratively – that means in small pieces.

To help you figure out how to use `hungry` and `availableTime` inside your function, try outputting their values to the Terminal as follows.

```javascript
function whatToDoForLunch(hungry, availableTime) {
  console.log("hungry is", hungry);
  console.log("availableTime is", availableTime);
}
```

##### process.argv

`process.argv` is a global object. Arguments are passed to a Node.js Application, and then accessed with the `process.argv` array.

```bash
$ [runtime] [script_name] [argument-1 argument-2 argument-3 ... argument-n]
```

Files are printed out in this order.

- The path pointing to the node executable
- name of the JS file
- the first argument passed by the user

```bash
$ node processargv.js tom jack 43
0 -> /Users/scott/.nvm/versions/node/v4.8.0/bin/node
1 -> /Users/scott/javascript/processargv.js
2 -> tom
3 -> jack
4 -> 43
```
