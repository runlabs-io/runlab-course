# Watch a request arrive

Serve in one pane, call from the other, and watch the log scroll.
It is the simplest way to understand a service, and it works for a web server, an API, a gateway, anything that answers requests.

The terminal is in two panes: **server** on the left, **client** on the right.

## 1. Serve

Make a page, then start the server in the server pane:

```shell panel="client"
echo '<h1>Hello from a lab</h1>' > index.html
```

```shell panel="server"
python3 -m http.server 8000
```

The server pane is now waiting. Nothing has asked it for anything yet.

## 2. Call

In the client pane, make one request:

```shell panel="client"
curl -s http://localhost:8000/
```

Look at the server pane. A line appeared: the address that asked, the time, and `GET / HTTP/1.1 200`, which means "asked for the front page, and it was served".

## 3. Call again, differently

Ask for something that is not there:

```shell panel="client"
curl -s -o /dev/null -w '%{http_code}\n' http://localhost:8000/nothing
```

The client printed `404`, and the server logged the same request with `404`.
The log is the server's side of the story.

## 4. Call from a browser

Open the page in a tab:

```service hello-server
```

Reload the tab a few times, and watch the lines arrive in the server pane.

## 5. Stop

The server is still running. Stop it with a key block:

```key panel="server"
Ctrl+C
```

## The pattern

1. Start the thing in one pane, so its log is in front of you.
2. Poke it from the other.
3. Read what it said.

You will use it all the time: to see what a gateway does with a request, what a service logs when something fails, or whether a change took effect.

## Finish

Press **Complete lab** when you are ready.
