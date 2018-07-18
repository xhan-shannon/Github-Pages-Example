---
layout: post
title: python unittest with mock
description: To use mock in python unittest and examples
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
Note:
unittest部分

https://imsardine.wordpress.com/tech/unit-testing-in-python/

mock部分

https://evangui.com/2016/02/29/%E7%94%A8-mock-%E4%BE%86%E4%BD%9C-python-unit-test/

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
