---
layout: post
title: Configure Jenkins Node
description: Record the node configuration steps
category: blog
---

To add node, follow the steps "Manage Jenkins" -> "Manage Nodes",
Initialize the node, need install jdk.
If the host is Ubuntu16.04, and it happened there is error when being installed jdk, use the command below.
     sudo apt-get -o Dpkg::Options::="--force-overwrite" install openjdk-9-jdk

Then using ssh agent launch mode to add the node.


[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
