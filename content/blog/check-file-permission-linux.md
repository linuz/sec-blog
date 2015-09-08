Title: Check the a file permission number on linux
Date: 2015-09-08 17:15
Tags: Linux, Command

Here is how to check a specific file/folder permission number on Linux

`stat -c %a /home`

This will return something like:

`755`

<img src='http://kernelmeltdown.org/blog/images/stat-command.png'>
