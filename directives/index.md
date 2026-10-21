# The lesson directives

A lesson is mostly explanation, and a few steps the learner does. A **directive** is one of those steps: something that happens when you click. There are four, and each comes in two forms. A **block** stands out as a task. A **link** fits inside a sentence. Use a block for a step the learner has to do, and a link for something optional.

This lab's terminal opens in two panes: `server` on top and `client` below.

## run

A shell block has a Run button. It types the command into the pane named by `panel`. The header shows the language, and Copy puts the same command on the clipboard to paste.

```shell panel="server"
python3 -m http.server 8000 --directory data
```

The same step as a link: [list the files](<run:ls data>){panel="client"}. The command sits between angle brackets, so it can have spaces. Hover the link to see the command.

## view

A view block shows a file with `bat`. It holds one path, and the header shows the file type.

```view panel="client"
data/hello.txt
```

The same step as a link: [look at hello.txt](view:data/hello.txt){panel="client"}. Copy on the block gives the command it ran, `bat -- data/hello.txt`.

## service

A service block opens a service the lab declares in `config.yaml`, in a new tab. The header shows the service's `type`. Copy puts the address on the clipboard.

```service hello-server subpath="/hello.txt" subpath-caption="hello.txt"
```

The same step as a link: [open the server](service:hello-server).

## key

Ask the server for the file from the client pane:

```shell panel="client"
curl -s http://localhost:8000/hello.txt
```

Then stop the server. A key block presses the keys in the pane it names. There is nothing to paste, so it has no Copy button.

```key panel="server"
Ctrl+C
```

The same step as a link: [press Ctrl+C](key:Ctrl+C){panel="server"}.

## How each one is written

Blocks are fences:

````markdown
```shell panel="server"
python3 -m http.server 8000 --directory data
```

```view panel="client"
data/hello.txt
```

```service hello-server subpath="/hello.txt" subpath-caption="hello.txt"
```

```key panel="server"
Ctrl+C
```
````

Links name the directive before the colon:

````markdown
[list the files](<run:ls data>){panel="client"}
[look at hello.txt](view:data/hello.txt){panel="client"}
[open the server](service:hello-server)
[press Ctrl+C](key:Ctrl+C){panel="server"}
````

Everything except `service` takes a `panel`, because a service opens a tab and not a pane.
