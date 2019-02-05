---
title: Disabling Blanking on Raspberry Pi
date: 2018-08-08 19:31:18
tags:
layout:
categories:
    - programming
---

This worked best:

Edit `/etc/X11/xorg.conf`:

``` bash
Section "Monitor"
    Identifier "Monitor"
    Option "DPMS" "false"
EndSection

Section "ServerLayout"
    Identifier "ServerLayout0"
    Option "BlankTime"  "0"
    Option "StandbyTime" "0"
    Option "SuspendTime" "0"
    Option "OffTime" "0"
EndSection
```
