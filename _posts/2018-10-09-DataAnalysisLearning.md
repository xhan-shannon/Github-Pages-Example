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

===========================================
read csv file
with open("file.fq") as f:
        for line in f:
                length=(len(line)-2)
                if line.startswith('@'):
                        line=line[:length]+''+line[length+1:]
                        print(line)

图示：
https://blog.csdn.net/wsp_1138886114/article/details/80509375
https://zhuanlan.zhihu.com/p/37915271
https://www.oschina.net/translate/5-quick-and-easy-data-visualizations-in-python
https://cloud.tencent.com/developer/article/1041505
https://www.cnblogs.com/lemonbit/p/6896499.html
http://www.sohu.com/a/239394291_464026
https://www.jianshu.com/p/9a2a0a4c76dd
https://www.jianshu.com/p/4fedbc832899
https://cloud.tencent.com/developer/article/1038594
https://www.yiibai.com/ai_with_python/ai_with_python_analyzing_time_series_data.html
https://zhuanlan.zhihu.com/p/29371291
https://blog.csdn.net/pipisorry/article/details/52209377
https://blog.csdn.net/shandianke/article/details/73730314
https://blog.csdn.net/shanguier/article/details/77575565

https://machinelearningmastery.com/time-series-data-visualization-with-python/
https://jakevdp.github.io/PythonDataScienceHandbook/03.11-working-with-time-series.html
[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
