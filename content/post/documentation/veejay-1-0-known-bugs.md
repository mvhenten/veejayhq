---
title: veejay 1.0 known bugs
name: veejay-1-0-known-bugs
type: post
date: "Wed, 11 Apr 2007 12:09:50 +0000"
author: niels
category: documentation
---
There are currently 4 known bugs in veejay 1.01. The OSC server starts at port offset + 4,but the console reports port offset + 2.Use port 3494 instead of 34922. There's a glitch in the resampler, toworkarround it you must start jackdin the same samperate as veejay.For example, if the audio has 44.1Khz,start jackd with -r 44100 and thenstart veejay.3. On some systems, veejay's commandlineoption '-O4' (openGL) causes a segfault4. SDL and fullscreen in Xinerama does not work