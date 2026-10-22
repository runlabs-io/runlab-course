# Run a command, show a file

In the first lab a code block ran a command.
Blocks come in two kinds you will use all the time, and each is a one-line change.
Each shows its kind in its header, so you always know what a press will do.

## Run: type a command

A `shell` block types its command into the terminal and runs it.
This one makes a small file:

```shell
echo "one" > notes.txt
echo "two" >> notes.txt
```

## View: show a file

A `view` block shows a file in the terminal.
The file here is `notes.txt`, which the block above just made.
Press its button:

```view
notes.txt
```

Its header says `view`, and what it types is the command that shows the file.
**Copy** copies that command, so you can use it yourself.

## The same, inline

Both also work inside a sentence, as links.
This one runs a command: [list the folder](<run:ls -l>).
This one shows a file: [look at notes.txt again](view:notes.txt).

## When to use which

Use `shell` for anything a learner should run, and `view` when the point is to read a file without opening an editor.
Because the command is always visible in the block, a learner can see what is happening and copy it to use later.

## Finish

Press **Complete lab** when you are ready.
