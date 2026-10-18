# Capture a value

This lab sets a name in the shell, captures a command that uses it, and then uses the captured name.

## Set a name

This sets `NS` in the current shell. It is not exported.

```shell
NS=demo
```

## Capture it

Run this. It reads `$NS` from that same shell and saves the output as `NS_COPY`.

```env var="NS_COPY" interpolated="true"
printf %s "$NS"
```

The page shows `NS_COPY` and the value. If this ran in a new shell, the value would be empty.

## Use the name

The next command runs in that same shell, so `$NS_COPY` is the value you just captured.

```shell completion="true"
echo "the name is $NS_COPY"
```

A new shell does not have `NS_COPY`. Nothing was written to a file.

## Summary

- A shell command can set a name for the commands after it.
- An env fence runs a command and keeps the output in that shell.
- A later command can use the captured name.
