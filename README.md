       当前实现的工具从用户的角度讲分两类，一类是面向开发人员的，另一类主要是面向开发DBA的，带有”DBA”后缀，具体有：
       1、Export table to Word - 把表结构导出成WORD文档，用于查看表与字段的设计，可读性比PDM强；这个参考了叶正盛大师的同类工具，但特点是导出多表（几百张）时速度也是很快的，而且可以选择导出索引与统计信息；
        2、Pdm Diff with DB - PDM文件与数据库表及字段比对工具，主要用于检查PDM与数据库的表及字段的差异，还可以实现字段级的更新，即根据数据库的字段去更新PDM的字段，这对手工维护一份最新的PDM是很提升效率的；
        3、Tablespace Autoextend - 表空间自动扩展，这是因为公司的开发环境与测试环境主要由开发与测试维护，一遇到表空间不足的问题常常措手无策，主要是提供给他们快速解决问题的，这个叶正盛大师有功能更全的同类工具，这个相当于一个简化快速版；
       4、Sql favor and edit - 常用SQL收藏与编辑，以及配置图表临控指标SQL的工具；
       5、Get full sql text(DBA) - 主要用于保垒机上取SQL文本，实现了owner替换与参数代入的功能，这样就能（基本）直接运行了；
       6、Show Plan detail(DBA) - 给黄玮大师的show plan SQL做了个图形化的壳，SQL优化利器；
       7、Show Sql Monitor(DBA) - 显示SQL monitor中top sql的信息，SQL优化利器；
       8、AWR_ASH report(DBA) - 参考了TOAD（好工具但要注册）的相同功能，快速生成AWR/ASH报告；
       9、Sql profile Gen(DBA) - 只需提供两个SQL_ID,就能生成用一个SQL执行计划去固化目标SQL计划的脚本,脚本源自Kerry Osborne大师，图形化了一下；
      10、Db performance chart(DBA) - 原意是用做数据库的性能趋势图，但只要配置好了SQL，亦可作其他用途；
      11、Show raw timestamp(DBA) - 小工具，将timestamp参数值可读化转换；

    需要说明的是，开发过程中参考了一些业内大师的同类工具或脚本，如有版权问题请与我联系：106820310@qq.com;    
    此为简单介绍，后续将为一些重点工具进行详细介绍；
    
    详细说明博客：  http://blog.itpub.net/13365316/cid-181206-list-1/
    
  64位已经可用了：myDbtools64.zip    由于控件因素，SQL收藏与图表两个功能去掉了，其他一致，sqlmon作了小优化；
   2016-07-29 更新：32位的进行了更新，主要是优化了sqlmon功能；

  2016-07-30更新：32位进行了更新，增加了“add owner”右键菜单，主要用于对表名增加owner,不用选定，只需要在表名单击右键；
                               对ASH报告进行了优化，当在nls_language没有与服务器一致，有可能报“无效的月份”错误，对此进行了优化，效果还有待更多场景验证；
                               对Get full sql text功能进行了较大的重构，可靠性更高了，对于没有替换到owner的表，可以通过"add owner"补齐；而对于绑定变量的替换更准确与细致了；
                                基本上，这个功能让我自己比较满意了；
