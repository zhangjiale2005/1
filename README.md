这是一个封装好的由python的gate-api第三方库为核心的爬取指定时间区间数据的python文件,
使用过交易所api的都知道，gate只支持读取2000个时间节点之内的k线数据，
这个程序实现了可以读取任意长度的时间区间的数据
在运行前请安装第三方库

pip install time
pip install datetime
pip install ast
pip install gate_api

如果遇到问题请手动添加阿里源或者清华源

输入案例:#您需要爬取的时间范围
'''输入起始时间，如             2021-10-01 12:00:00'''<u>2021-10-01 12:00:00</u>#这里是你将输入的数据

'''输入结束时间，如           2021-12-01 12:00:00'''<u>2021-10-07 12:00:00</u>#这里是你将输入的数据

输出案例:#对应['c', 'h', 'l', 'o', 'sum', 't', 'v'][收盘价,最高价,最低价,开盘价,交易额,时间戳,合约大小]
组成的一个二维列表,默认为1min的k线下的数据,


[[43654.0, 43665.4, 43603.9, 43603.9, 773397.59, 1633060800.0, 177229.0], [43628.7, 43652.8, 43628.7, 43652.8, 258729.64, 1633060860.0, 59286.0], [43577.0, 43633.2, 43577.0, 43624.6, 123554.19, 1633060920.0, 28329.0], [43571.2, 43577.1, 43536.0, 43577.0, 307434.84, 1633060980.0, 70594.0], [43595.0, 43616.8, 43570.7, 43572.7, ....................................................................]



如果需要更改默认的1mink线数据为其他时间跨度数据，请找到代码中的interval变量,更改1m为其他数据,如5m

