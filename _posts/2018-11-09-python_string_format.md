---
layout: post
title: python string format
description: python string format
category: blog
---
Option 1: %-formatting:
Option 2: str.format():
Option 3: f-strings

Option 1: 
Example:
name = "Mickey"
"I am %s." % name

However, once you start using several parameters and longer strings, your code will quickly become much less easily readable.

Example 2: 
"I am %(name)s." % {'name'=name}


Option 2:
Example 1:
friend_name = "Robot"
your_name = "Matrix"
"Hello {}, I am {}".format(friend_name, your_name)

Example 2:
person = {"name': "eric",
          'age': 30}
"Hello {name}, I am {age}".format(**person)

Option 3:
Example 1:
name = "eric"
f"Hello {name}"


[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
