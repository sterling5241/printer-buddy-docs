# Remote access

By default Printer Buddy only works on your home network. Remote access lets you check a printer from anywhere with a **share link**.

## Turning it on

Pick **Remote access = on** in the installer, or open **9) Remote / share links** in the installer menu:

- **1) Set up automatically** installs a secure tunnel (`cloudflared`) and registers it.
- **2) Remove tunnel** takes it away again.

The menu shows your tunnel's state and your ID.

## Share links

Share a printer's view with someone else. Links look like:

```
https://www.printerbuddy.stream/share/user/<your id>/...
```

## Who can see what

There's no login. Each share link has its own long, secret code, and **anyone with the link can see that printer**, so only send it to people you trust. Links can be set to expire, and you can delete a link any time to stop it working.
