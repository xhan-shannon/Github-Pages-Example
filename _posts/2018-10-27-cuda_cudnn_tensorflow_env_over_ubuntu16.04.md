---
layout: post
title: Setup cuda/cudnn/tensorflow
description: Install dependents over ubuntu14
category: blog
---

1. check your GPU product type and model
   $ lspci
2. Then install nvidia driver
   https://www.nvidia.com/Download/index.aspx
3. Download cuda and install it
   https://developer.nvidia.com/cuda-downloads
4. Download cudnn
   https://developer.nvidia.com/rdp/cudnn-download
5. install tensorflow
   pip3 install tensorflow-gpu

6. verify tensorflow can work
   import tensorflow

https://www.techforgeek.info/enable_disable_service_on_ubuntu.html

Note: should keep the version map(CUDA9.0 CuDNN7.1)

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
