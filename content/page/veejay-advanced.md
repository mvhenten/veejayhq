---
title: Veejay Advanced
name: veejay-advanced
type: page
date: "Mon, 17 Nov 2008 22:49:54 +0000"
author: niels
category: uncategorized
---
# VIMS

VIMS is veejay's internal message system - its simple and in plain ASCII.All control data is distributed via VIMS. Each (atomical) message consists of an Action Identifier and a list of zero or more Arguments which can be used to control Video Clips, Video Streams, the Effect Chain and many other things.Reloaded, veejay's client, uses a dual socket to read status and write back VIMSmessages.VIMS allows events to be triggered through:SDL Keyboard Event (libsdl)OSC (Open Sound Control)And ItselfAfter intalling veejay, you will have a commandline utility 'sayVIMS' which youcan use to send text messages.

Use the command$ veejay -u -n |lessto dump all VIMS messages.

## The Message Format

A message is described as:&lt;Action Identifier&gt; : &lt;Argument List&gt; ;Examples:

    080:;099:0 0;

### &lt;Action Identifier&gt;

The action identifier is a 3 digit number describing a Network EventThe colon is used to indicate the start of the Argument List and must be given.

### &lt;Argument List&gt;

The Argument List is described by a printf() style formatted templatewhich describes the number and type of arguments to be used.The semicolon must be given to indicate the end of this message

## Reserved Values

Some reserved numbers:<table><tr><td>clip id</td><td>0</td><td>select currently playing sample</td></tr><tr><td>clip id</td><td>-1</td><td> select highest sample number</td></tr><tr><td>chain entry</td><td>-1</td><td>select current chain entry</td></tr><tr><td>stream id</td><td>0</td><td>select currently playing stream</td></tr><tr><td>stream id</td><td>-1</td><td>select highest stream number</td></tr><tr><td>key modifier</td><td> 0 = nonone, 1= alt , 2 = ctrl, 3 = shift</td><td></td></tr><tr><td> frame</td><td> -1</td><td>use highest possible frame number</td></tr><tr><td>playback mode </td><td>0 = clip, 1 = stream, 2 = plain</td><td></td></tr><tr><td>data format</td><td> yv16 (yuv 4:2:2 raw) , mpeg4, divx, msmpeg4v3,div3, dvvideo, dvsd, mjpeg, i420 and yv12 (yuv 4:2:0 raw)</td><td></td></tr><tr><td>loop type</td><td>0 = no looping, 1 = normal loop, 2 = pingpong (bounce) loop</td><td></td></tr></table>  
  
