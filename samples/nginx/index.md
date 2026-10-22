# Nginx lab

Hello dear student.

This lab opens a machine where nginx is already running. You do not start it.

## Open its page

Click nginx in the bar at the top. It opens in a new browser tab.

You can also [click through to the service](service:nginx) from the lab instructions.

The page is nginx's welcome page.

## See it from this machine

The same server is listening here.

```shell
curl http://127.0.0.1/
```

The reply is the same welcome page.

## Check the service

```shell
systemctl status nginx
```

Active and running means nginx is up.

## Summary

The web server was already listening when this lab opened:

- the nginx link opens that page in your browser
- `curl http://127.0.0.1/` fetches the same page from this machine
- `systemctl status nginx` shows the service is running

You've reached the end of this lab. Click Complete lab to finish.
