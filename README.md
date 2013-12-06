afpmount-workflow
=================

An Alfred workflow that mounts AFP shares in the network using SMB host names.
Since I'm having trouble with mDNS / Bonjour, but nevertheless want to mount
network shares via AFP, I decided to write this Alfred Workflow that can lookup
IPs of an SMB share in the network and mounts an AFP share on the same
host / IP address.

(Obviously) only running on Macs (tested in OSX 10.9 Mavericks).

Usage
-----

If there is a server in the network that hosts an SMB share with name _data-grave_
as well as an AFP share on the same IP, you can run:

```
afpmount data-grave
```

It will do an SMB lookup for data-grave and get its IP. It will then further
mount "afp://<found-ip>", asking you for user name and which directory to mount
(think Finders "Connect to Server" feature).
