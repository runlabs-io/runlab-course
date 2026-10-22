# Open a web page

The terminal has started in two panes: **server** on the left and **client** on the right.
You met panes in the last lab. Here they get a job.

A lab can run a web server for you to look at.
You start the server in one pane and open its page in a browser tab.

## Make a page

In the client pane, write a one-line page:

```shell panel="client"
echo '<h1>Hello from a lab</h1>' > index.html
```

## Start the server

In the server pane, serve this folder on port 8000.
It keeps running, and prints a line for every request:

```shell panel="server"
python3 -m http.server 8000
```

## Open it

A **service** block opens a web page that is running in the lab, in a browser tab.
Press its button:

```service hello-server
```

The tab shows your heading.
Press the button again: it comes back to the same tab and does not open a new one.

## How it is written

A service block names a service, and the service is declared in the lab's `config.yaml`: a name and the port the server listens on.

````yaml
services:
- name: Hello server
  type: http
  port: 8000
  path: /
````

The block is the service's name, made lowercase with a dash: `hello-server`.

## Finish

Look at the server pane once more. Every time the tab loaded the page, a line was added.
The next lab is about that.
Press **Complete lab** when you are ready.
