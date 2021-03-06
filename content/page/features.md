---
title: Features
name: features
type: page
date: "Sun, 16 Nov 2008 22:27:51 +0000"
author: niels
category: uncategorized
---
# Veejay version 1.5.22

December 30, 2012**Veejay, a visual instrument for GNU**[http://veejayhq.net][0][http://veejay.dyne.org][1]

**Veejay is a visual instrument and real-time video sampler.It allows you to "play" the video like you would play a piano.While playing, you can record the resulting video directly to disk (video sampling).**

  
  
  
[Camera calibration with veejay][2]&nbsp;&nbsp;&nbsp;[Reloaded][3]

## FEATURE OVERVIEW

### General

# Free Software (GNU GPL) (1)# Servent architecture (2)# Soft realtime (3)# Frame accurate (4)# Loop based editing (5)# Native YUV processing# Crash recovery# Support for multi core cpu

### Media

# Codecs: MJPEG,MPNG, DV, LossLess JPEG, MJPEG-b,YUV (raw)# Containers: AVI , Quicktime, rawDV# Devices: USB webcams, DV1394, TV capture cards, etc (v4l2)# Support for unlimited capture devices# Support for Image files (PNG ,JPEG,TIFF,etc)# Support for JPEG streaming webcams

### Editing

# 137 built-in FX , many unique and original FX filters# FX chain (20 slots, first 3 are rendered in mixing mode)# All FX parameters can be animated.# Mix up to two layers per FX slot# Non destructive edit decision lists (cut/copy/paste/crop video)# Simple text editor# Sample editor# Sequence editor# Live disk recorder (sampling)# Full deck save/restore# Live clip loading# Live sample sequencing

### Trickplay

# VIMS event recording/playback (6)# Various looping modes including bounce looping# Playback speed and direction# Video scratching# Change in-and out points of a sample (marker)# Slow motion audio / video (7)# Fast motion audio / video# Dynamic framerate# Random frame play# Random sample play# Access up to 4096 video samples instantly

### Output

# Audio trough Jack (low latency audio server) (8)# SDL# Headless# Network streaming (unicast and multicast)# Preview rendering# V42L loopback# YUV4mpeg# [TwinView / One BigDesktop][4]

### Interaction

# Programmable keyboard interface# VIMS (tcp/ip)# OSC (udp)# PureData trough sendVIMS external

### Viewing

# Full screen or windowed mode# Camera/Projector calibration (9)

### Additional

# Support for FreeFrame plugins# Support for Frei0r plugins

  
What is

(1) Free SoftwareA matter of liberty, not price. You should think of “free” as in free speech.  
Free software is the matter of the users freedom to run, copy, distribute, study, change and improve the software.  
(2) A servent architecture is a peer-to-peer network mode with both functionalities of a server and a client. The setup is designed so that each veejay-node can send and receive video,allowing for the creation and maintenance of ad-hoc veejay-networks. **Reloaded** , veejay's graphical interface, is a thin client and can be run from another computerto track one or more **veejay** servers.(3) Soft realtime: A system is realtime if the correctness of the application not only depends onthe logical correctness but also upon the time at which it was performed. Veejay tolerates such lateness and responds by dropping video frames. You can instruct veejay to ignore the time aspect of the video and render all frames, effectifly turning the server into a frame producer.(4) VIMS: Veejay Internal Message System. Control data is distributed via this message system,each message consists of an 'event selector' with a list of arguments. VIMS is the lowest level control interface available. The keyboard interface and OSC server are built on top of it. Also all veejay clients communicate usings VIMS.(5) Loop based editing: Loops are (short) sections of video (up to any length) that are repeatedcontinuously. While playing, you can change the properties of the video sample, add filters to itand record it on the fly to a new sample (which can be used instantly).(6) Frame accurate: In veejay, every frame is a key-frame (a whole image). As a consequence, veejay has no support for video codecs that make use of difference frames.(7) In trickplay mode, veejay will always resample the audio analogous to varying the speedof an analogue tape recorder . Halve the speed results in the pitch going down an octave. Slow motion video is produced by linearly interpolating in-between frames and faster motion is accomplished by skipping video frames or, if playing without audio,by changing the framerate dynamically.(8) JACK: A low latency audio server that can connect a number of different applications to an audio device,allowing them to share audio between themselves.(9) [Perspective Transform][5]

[0]: http://veejayhq.net
[1]: http://veejay.dyne.org
[2]: http://www.veejayhq.net/2008/11/projectorcamera-calibration-augmented-reality
[3]: http://www.veejayhq.net/screens/
[4]: http://www.veejayhq.net/docs/veejay-environment-variables/
[5]: http://www.veejayhq.net/2008/11/projectorcamera-calibration-augmented-reality/