# Capture a value

Set a name in this shell, save a command's output under a second name, and use that name in the next command.

## Set a name

```shell
NS=demo
```

This sets `NS` in the current shell. It is not exported.

## Capture it

Run this. It reads `$NS` from this shell and saves the output as `NS_COPY`.

```env var="NS_COPY" interpolated="true"
echo -n "$NS"
```

You should see `NS_COPY` and `demo`. A new shell would not have `NS`, so the value would be empty.

## Use the name

This runs in the same shell, so `$NS_COPY` is the value you just captured.

```shell completion="true"
echo "the name is $NS_COPY"
```

## Summary

- A shell command can set a name for the commands after it.
- An env fence runs a command and keeps the output in that shell.
- A later command can use the captured name.
