# Panes

The terminal on this page is a set of panes. A lesson can arrange them: one pane, two side by side, two stacked. This lab shows how. Each step is a **layout** block, pink like the layout links in other lessons. The header lists the panes the layout creates, and the button is **arrange**.

## One pane

The terminal starts as a single pane. Everything you type goes there.

## Two panes, side by side

Click arrange. The terminal splits into a `server` pane on the left and a `client` pane on the right.

```zellij layout="two-pane"
```

Start a server in the first pane:

```shell panel="server"
python3 -m http.server 8000
```

Call it from the second:

```shell panel="client"
curl -sI http://localhost:8000
```

> [!NOTE]
> Click arrange before you run the blocks above. A block that names a pane the terminal doesn't have yet fails with "Open the layout above this block first".

Stop the server:

```key panel="server"
Ctrl+C
```

## Two panes, stacked

The same kind of block can arrange a different split. A caption in the body replaces the default "Open panes" text.

```zellij layout="stacked"
Stack the panes: one above the other
```

## Back to one pane

Arranging replaces the layout, so this block puts the terminal back as it started:

```zellij layout="one-pane"
Back to one pane
```

If you ever type `exit` in a single pane and land in a bare terminal, any arrange block puts the panes back. Click it again whenever the panes aren't how you want them.

## As a link

The same step fits in a sentence: [arrange two panes](zellij:two-pane), or go [back to one](zellij:one-pane). Hover the link to see which panes it makes.

## How it is written

````markdown
```zellij layout="two-pane"
```

```zellij layout="stacked"
Stack the panes: one above the other
```

[arrange two panes](zellij:two-pane)
````

The name, such as `two-pane`, is the name of a **layout file** that the lab carries in its `data/` folder: `data/two-pane.kdl`.
A layout file says which panes exist, what they are called, and how they are split.
Layouts come from [Zellij](https://zellij.dev), the program that manages the panes in the terminal, and they are written in a small format called KDL.
You do not need to know either to use one: start from a layout file that does nearly what you want, and change the pane names.
The three used here are in this lab's folder on [GitHub](https://github.com/runlabs-io/runlab-labs/tree/main/tutorial/layout-card/data).
