---
layout: post
title: 'Ping a “host” until it Responds, Then Play a Sound !'
categories: SSH
---
Lets say we want to ping the domain name: sip01.telecomsxchange.com and if its up, we want our Mac to tell us that it is, if its down after 30 requests we want it to let us know that its down while we’re away from it.

1.Open Mac OS Terminal

```
ping -oc 30 sip01.telecomsxchange.com > /dev/null && say "TelecomsXChange server is up" || say "Oh Shit ! TelecomsXChange host is down"
```

To try this on other servers, just replace sip01.telecomsxchange.com with the domain name or IP-Address that you want to ping.

Another cool way to hear a sound whenever the server stops replying to ping by using this command:

```
ping -A 1.2.3.4
```

In this case you use the uppercase A parameter to send us a beep sound whenever the target stops replying to our ping or if there is a packet loss.

Hope you find it useful !
