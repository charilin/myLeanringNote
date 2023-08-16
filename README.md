# myLeanringNote
## Mysql学习笔记
参考书目：[《mysql实战45讲》](https://funnylog.gitee.io/mysql45/)、《MYSQL技术内幕：innodb存储引擎》、《mysql是怎样运行的：从根上理解mysql》
### 1、Mysql的查询语句执行流程
1. Server层：
   - 连接客户端进行权限校验
   - （查询缓存）
   - 解析器
   - 优化器
   - 执行器
2. 引擎层innodb:
   - 进入表空间查询索引树
   - bufferpool（内存缓冲池）
   - 返回Server层
### 2、Mysql的更新语句执行流程
1. Server层：
   - 连接客户端进行权限校验
   - （查询缓存）
   - 解析器
   - 优化器-执行器
3. 引擎层innodb:
   - 进入表空间查询索引树
   - 加载到bufferpool（内存缓冲池,**可能延迟加载，使用changer buffer先保存修改记录，不实际从磁盘加载页**）
   - 保存undo日志
   - 更新redo log buffer
   - 提交事务
   - 持久化redo log
   - 持久化binlog
   - 更新后数据落盘（doublewrite）
### 3、事务的四个特性以及mysql如何保证事务
1. 原子性  
通过redo log和 undo log保证事务只有提交和回滚两种状态
2. 一致性  
由其他三种特性保证
3. 隔离性  
通过MVCC加锁保证
4. 持久性  
binlog保证数据持久化
### 4、Mysql的锁机制及MVCC

### 5、Mysql索引机制

### 6、Mysql索引失效情况

### 7、主从备份原理及如何恢复

### 8、join语句的执行流程

### 9、如何优化sql语句




