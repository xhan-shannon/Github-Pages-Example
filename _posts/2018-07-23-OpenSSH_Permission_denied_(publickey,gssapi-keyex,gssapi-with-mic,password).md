---
layout: post
title: debug ssh connection
description: how to get an idea to solve ssh problem
category: blog
---

I have happened to change some config for ssh. However, I forgot what I did and why I did that. 
The final result is I could not access any other remote compute using ssh for this host.

The error is Permission denied (publickey,gssapi-keyex,gssapi-with-mic,password).

I tried to find some resolution for this problem via google, but failed. Even though I filed 
a help request for our IT support, it did not help.

Then I search the keywords again, the method to open the debug mode appears in the answer list.
It really helps.

I add -vvv in the option list of ssh command. Then I found that I missed configuring the ssh. 
After correcting the configuration item, it works again.

I have learned that how important the debug information is. I would arrange my debug information
in my program.

The second, if you meet some problem of one software. First, calm down, try to collect enough debug 
information for analyzing.

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
