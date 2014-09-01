cdbk
====

A simple zsh function to make management of zsh
named directories easier.  It keeps all named directories in a
file and uses grep, sed, echo, and perl to parse and modify 
this file in order to add, change or remove bookmarks.

Because it uses the zsh named directory function, full zsh path
completion is possible.  Further, very simple cdbk completion is
included to make replacing and deleting bookmarks easier.

This program was heavily inspired by Stan Angeloff's function 
of the same name found here:
http://blog.angeloff.name/post/1027007406/cd-with-bookmarks-and-auto-completion-for-zsh

This file also provides the function ``folder_name()``, which returns
a formatted list of the names of the current folder for use in 
a prompt. To include the folder name in your prompt use e.g.:
export ``PROMPT=$PROMPT $(folder_name)``

Usage: cdbk {-a,-r,-d,-l} <name> [path] (run with no paramaters for info)
       -a: Create bookmark (uses current dir if no path)
       -r: Replace bookmark (uses current dir if no path)
       -d: Delete bookmark
       -l: List all currently enabled bookmarks

Requirements: Needs to be sourced from a zsh startup file, or use oh-my-zsh

Created by: Mike Dacre 
Created on: 19-11-11
Version: 1.1

License: MIT License - Open Source. Use as you wish
