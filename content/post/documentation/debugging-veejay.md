---
title: debugging veejay
name: debugging-veejay
type: post
date: "Wed, 18 Feb 2009 20:39:10 +0000"
author: matthijs
category: documentation
---
To help us fix things in veejay faster, please provide the followinginformation:1. full veejay console output(always run veejay with the '-v' commandline option)In case of segmentation faults,1. Run configure with '--enable- debug ' for both server and client2. Run veejay-server and reloaded in the debugger$ gdb /full/path/to/veejay(gdb) r -v /path/to/some/videofile.avi3. When it crashes,(gdb) btAnd copy&amp;paste the outputAlso, valgrind is an excellent tool for debugging veejay, I'm alwaysinterested ina few valgrind logs to make veejay more robuust. This will only beusefull ifyou have run configure with --enable- debug (from a clean source tree)$ valgrind --log-file=/tmp/veejay.log --leak-resolution=high --leak-check=full /full/path/to/veejay -v /path/to/videofile.avi