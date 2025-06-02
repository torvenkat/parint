
---
date: 2025-06-01
title: Flushing DNS Cache in MacOS
tags:
  - macos
---

There are occasions when one needs to flush DNS Cache (such as when you change your DNS provider to third-party such as Cloudflare or Google). It can be done as follows;

In Terminal run

```
sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder
```

you will be prompted for the admin user password, type it. 

Note that there won't be any confirmation when you run this command, that is okay.  