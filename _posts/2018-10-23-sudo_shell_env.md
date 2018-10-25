---
layout: post
title: sudo shell path environment
description: change the path when using sudo in the command line
category: blog
---

If you can live with replacing the secure_path value instead of appending it, you can use a much easier solution. Usually sudo has a config directory like /etc/sudoers.d where you can drop additional configuration files.

Just create a file there with your complete secure_path value:

Defaults secure_path="<default value>:/usr/local/bin"
This overwrites the value from the main config. If the path value is the same for all your machines this can easily be deployed with scripts or a package.

This has the additional advantage that you don't have to check and possibly merge config files when the sudo package is updated in the future.

This is normally set by the secure_path option in /etc/sudoers. From man sudoers:

 secure_path   Path used for every command run from sudo.  If you don't
               trust the people running sudo to have a sane PATH environ‐
               ment variable you may want to use this.  Another use is if
               you want to have the “root path” be separate from the “user
               path”.  Users in the group specified by the exempt_group
               option are not affected by secure_path.  This option is not
               set by default.
To run commands that are not in the default $PATH, you can either

Use the full path: sudo ~/bin/my-command; or

Add the directory containing the command to secure_path. Run sudo visudo and edit the secure path line:

https://superuser.com/questions/927512/how-to-set-path-for-sudo-commands

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
