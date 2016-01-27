+++
date = "2016-01-27T21:56:58Z"
description = ""
keywords = ["awesomewm"]
title = "Awesome Window Manager"

+++

# Kanji

When people look over my shoulder, or do some work with me on my laptop, I am always asked about the Japanese/Chinese pictograms on the top left of my screen:

<p align=center>
<img src=/images/awesome_desktops.png>
<br />Kanji
</p>

These are the 10 workspaces I have available to me. I had to do a little research on them, and I think they are Chinese or Japanese number characters.

[九](https://en.wiktionary.org/wiki/%E4%B9%9D) - for example is Chinese Number 9, or Japanese Kanji 9

The reason I don't know what they are, is because I copied them from someone else's `rc.lua` for AwesomeWM. What I will say though, is that they look better than the English numbers 0-9.


# A Brief History

About 10 years ago, I was getting dispirited with all Desktop Environments (DE) and Window Managers (WM). I'd fully flipped from dual booting with Windows and made Linux take over my entire machine. This was around the time Gnome was moving from v2 to v3, if I remember correctly, and I was none too impressed with their excessive use of Compiz and losing the 'traditional' start menu bar. Basically, things were changing and I didn't like it. Also, KDE was never my bag; GTK has always looked better to me than Qt.

So, I was looking for a decent UI to work on. I wanted it to be lightweight with the ability to run VMware for a Windows virtual machine (I was tied into Outlook and some other Microsoft tools). XFCE and LXDE kept popping up. I tried them both, but neither ever felt quite right. I think I stopped on LXDE the longest. I even tried out Enlightenment 17 and 18!

Xmonad was getting a lot of attention on ArchLinux and looked like fun. I tried it and I failed to make anything decent. It was beyond my capabilities.

So then I get a new Ops gig with some guys who know what they are doing. I try and stick at Xmond for a bit, and then one of them passed me their `rc.lua` for Awesome, told me the basic shortcuts to jump windows, re-tile and switch workspaces. Suddenly things made sense and I persevered.


# Tiling

AwesomeWM is a tiling window manager. It is not like your usual desktop environment. There are no integrations out of the box and the default config is rather basic.

What AwesomeWM does, which makes it so productive, is it allows you to make the best use of your available screen estate, whilst allowing you to not need your mouse to jump around windows.

I use the mouse more than I should for this window manager, but, one key productivity feature is the ability to run quite a few terminal sessions on one workspace and have them arranged in equal sizes.

I currently have 13 different ways of arranging windows, from vertical and horizontal splits, to floating and spirals.

{{< figure src="/images/awesome_7windows.png" title="Arranging 7 Windows" >}}

As you can see, laying out 7 windows, above, uses every inch of my screen apart from a small bar top and bottom to tell the time, which workspace I'm on and a few system monitor bars.

Your fingers rarely need to leave the keyboard when working with windows. Using the Mod4 keys and various vim-style key-bindings, jumping between windows is as simple as jumping workspaces.

# Keyboard Shortcuts

Mod4 is the key to all AwesomeWM key strokes. Often labelled as the 'Windows' key on most keyboards, you can use `xev` to see the keycode your button makes:

```
KeyPress event, serial 33, synthetic NO, window 0x4c00001,
    root 0xd7, subw 0x0, time 666921407, (880,314), root:(881,331),
    state 0x10, keycode 133 (keysym 0xffeb, Super_L), same_screen YES,
    XLookupString gives 0 bytes: 
    XmbLookupString gives 0 bytes: 
    XFilterEvent returns: False
```
This on my machine is the Super Left (Super_L) key used as a modifier (mod4)

With that working, let's just go and list the really important keys that make moving around windows and workspaces easy. These are the ones I use most frequently

```
Mod4 + 1  - Switch to workspace 1. Replace 1 with 0-9 to hit up all workspaces
Mod4 + j  - Jump to the next window
Mod4 + k  - Jump to the previous window
Mod4 + f  - set window fullscreen
Mod4 + Return - Spawn a terminal emulator
Mod4 + Space  - switch workspace layout
Mod4 + Escape - Jump between workspace and previous workspace
```


# Independent Desktops

One final feature that I often take for granted is the independence of workspaces. When adding an external monitor to your laptop, or simply having two screens on your workspace, AwesomeWM treats both screen separately so you effectively double your number of workspaces!

Where on one you have 10, add another screen, get another 10 workspaces.

As you switch between them with your `Mod4+{0..9}` the left screen switches and the right one doesn't. Move to the right screen and set it workspace 5 and the left one doesn't change. 


# In Summary

From my twitter feed, I see many proponents of the i3 window manager as some people reject OSX as their work horses (well done!). I have not used i3 yet, and don't fully know it's capabilities. I should take a look and see if it offers anything over AwesomeWM.

I've now been using AwesomeWM for so long, using anything else becomes painful and difficult. It makes me productive; I can have things open across 10 workspaces, switch to them quickly, tile windows side by side for comparison or quickly full screen a terminal session to zoom in.

