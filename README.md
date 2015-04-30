# 考勤记录管理

## 上下班打卡记录管理和统计-使用thinkphp框架(3.x)

* 数据库使用的是sqlite，因为比较简单，配置文件修改一下也可以支持mysql

* Thinkphp里面修改了一个bug，是U方法中，参数的问题。按照[官方文档](http://document.thinkphp.cn/manual_3_2.html#action_bind)

>    'URL_PARAMS_BIND_TYPE'  =>  1, // 设置参数绑定按照变量顺序绑定  
query?id=1应该会生成query/1，但运行结果仍然是query/id/1，感觉是个bug，本人在U方法中做了修改。
还有就是ThinkPHP/Library/Think/Model.class.php里面_facade方法修改为直接返回，否则没法提交数据，原因不清楚。

记录管理中可以导入的csv格式文件格式是工号,日期 时间（不带标题），例子如下：（仅仅前面两列是有效的）

    15,2015-04-07 16:20:26,1,1,1,0
    
    8,2015-04-07 16:45:53,1,1,1,0
    
    10,2015-04-07 17:17:55,1,1,1,0
    
    5,2015-04-07 18:18:22,1,1,1,0
    
    6,2015-04-07 18:43:22,1,1,1,0
    
    12,2015-04-07 19:34:35,1,1,1,0
    
    7,2015-04-07 19:35:50,1,1,1,0
 


