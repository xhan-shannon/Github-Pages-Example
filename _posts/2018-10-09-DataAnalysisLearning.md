---
layout: post
title: Data Science 
description: data analysis tools and knowledge 
category: blog
---

https://people.ok.ubc.ca/rlawrenc/teaching/301/notes/index.html

https://towardsdatascience.com/interactive-data-visualization-with-d3-js-43fc3428a27e

https://www.analyticsvidhya.com/learning-paths-data-science-business-analytics-business-intelligence-big-data/newbie-d3-js-expert-complete-path-create-interactive-visualization-d3-js/

1. open a csv file with chinese charaters
1) You can try this:

import codecs
x = codecs.open("testdata.csv", "r", "utf-8")

2) Another possibility can be theoretically this:

import pandas as pd
df = pd.DataFrame(pd.read_csv('testdata.csv',encoding='utf-8')) 

3) Maybe you should convert you csv file into utf-8 before importing with Python (for example in Notepad++)? It can be a solution for one-time-import, not for automatic process, of course.
https://stackoverflow.com/questions/39308065/how-to-display-chinese-characters-inside-a-pandas-dataframe

https://stackoverflow.com/questions/39308065/how-to-display-chinese-characters-inside-a-pandas-dataframe

首先 python文件开始 添加 一行 #-*- coding=utf-8 -*-
然后调用的时候 pd.read_csv(csvname,encoding="gb2312")
然后看看你的python是保存为什么编码的， 推荐用notepad++打开，然后转化为utf-8 无BOM格式的。 这样无论在liunx还是window都能保证无乱码。

https://www.zhihu.com/question/22016184 [pandas怎样处理中文？]

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
