# Layout cards

This lab shows a zellij layout block, which draws a card that opens a terminal layout when you click it.

## Open the panes

Click the card. The terminal splits into a server pane and a client pane, and the card turns green.

```zellij layout="server-client"
```

> [!WARNING]
> Click the card before you run the blocks below. A server or client block run before its layout is open fails with "Open the layout above this block first".

## Start the server

```shell panel="server"
python3 -m http.server 8000
```

## Call it from the client

```shell panel="client"
curl -sI http://localhost:8000
```

## A card with a caption

A block body is the card's caption, the same as the text of an inline layout link.

```zellij layout="server-client"
Reset the two panes
```
