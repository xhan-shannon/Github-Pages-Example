---
layout: post
title: rabbitmq in openstack
description: To learn and make clear how rabbitmq works in openstack
category: blog
---

## python unittest with mock

# import the mock module

import unittest
try:
    from unittest import mock
except:
    import mock

def func1():
    
import mock
from example import func1, func2

class TestFuncWithMoc(unittest.TestCase):
    @mock.patch("example.func1")
    def test_func2_with_mock(self, mock_func1):
        mock_func1.return_value = 10
        self.assertEqual(20, func2(2))

    def test_func2(self):
        self.assertEqual(24, func2(3))


if __name__ == "__main__":
    unittest.main()
~                      

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
