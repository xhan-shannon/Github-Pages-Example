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


[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
