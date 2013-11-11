---
title: 'Powershell one-liners'
date: '2013-11-10'
description:
tags: [powershell, one-liners, cheatsheet, commands, windows]
---

Over the past year working at Microsoft, I've grown some appreciation of PowerShell. I live and
breathe in Mac and Linux environments with a terminal console, so not having an equivalency in
Windows was suffocating me. `cmd` makes me want to rage quit, so don't get me started.

I came across this [gem][source], and some will proof its usefulness 

Open `Document.pdf`, like `open` command in Mac.

    Invoke-Item Document.pdf

Stop all processes with matching name (Chrome, in this case)

    Stop-Process -processname chrome*

Find all "exe" files in a tree, list their full path, and sort "fullname":
    
    Get-ChildItem 'C:\Tree\Of\Files\' -recurse -include *.exe | select-object fullname | sort fullname | more

Find all mp3s and sort by ascending size:

    Get-ChildItem 'C:\Tree\Of\Files\' -recurse -include *.mp3 | select-object fullname,length | sort length

Start an interactive PowerShell session on the remote computer myserver:

    Enter-PsSession myserver

Run a command on a list of remote machines:

    Invoke-Command -computername myserver1, myserver2, myserver3 {get-Process}

I'll update this post as I learn more one-liners in Powershell

[source]: http://www.bashedupbits.com/2013/11/powershell-one-liners.html
