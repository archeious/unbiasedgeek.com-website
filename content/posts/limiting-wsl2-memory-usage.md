+++
categories = ["tech"]
date = 2022-09-29T03:12:47Z
title = "What to do when WSL2 decides to eat all your RAM."
tags = [
    "WSL2",
]
+++

## What to do when Windows Linux Subsystem 2 decides to eat all your RAM.

I left several WSL terminals running over night and when I returns I noticed my PC (that is a personal computer) was running slow.  I checked the memory usuage and a process named **vmmem** was using nearly 32g.  After a bit of research aka typing my problem into Google and clicking on the first [LINK](https://www.koskila.net/how-to-solve-vmmem-consuming-ungodly-amounts-of-ram-when-running-docker-on-wsl/), I found out that **vmmem** is the process that handles the system resources of the virtual machine WSL2 runs in.  

I ran `wsl --shutdown` to free up the memory.  Then created the file `%UserProfile%/.wslconfig`[^1].   This will limit the RAM used in the future.
```
[wsl2]
memory=8GB
```

[^1]: Advanced settings configuration in WSL - https://learn.microsoft.com/en-us/windows/wsl/wsl-config
