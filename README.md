# myLeanringNote
## Mysql学习笔记
参考书目：[《mysql实战45讲》[(https://funnylog.gitee.io/mysql45/)、《MYSQL技术内幕：innodb存储引擎》、《mysql是怎样运行的：从根上理解mysql》
### 1、Mysql的查询语句执行流程
Server层：连接客户端进行权限校验-（查询缓存）-解析器-优化器-执行器
引擎层innodb:进入表空间查询索引树-bufferpool（内存缓冲池）-返回Server层
### 2、Mysql的更新语句执行流程
Server层：连接客户端进行权限校验-（查询缓存）-解析器-优化器-执行器
引擎层innodb:进入表空间查询索引树-bufferpool（内存缓冲池）-返回Server层
###3、事务的四个特性以及mysql如何保证事务

### 4、Mysql的锁机制及MVCC

### 5、Mysql索引机制

### 6、Mysql索引失效情况

### 7、主从备份原理及如何恢复

### 8、join语句的执行流程

### 9、如何优化sql语句




