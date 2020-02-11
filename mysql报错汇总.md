## 1.mysql.sock找不到

ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)

#### 解决：sudo sh mysql.server start 报错

. ERROR! The server quit without updating PID file (/usr/local/mysql/data/miky.local.pid).

  更新/etc/my.cnf如下：
  
```
 bind-address = 127.0.0.1
datadir=/usr/local/mysql/data
log-error=/usr/local/mysql/data/error.log
# 进程文件
pid-file=/usr/local/mysql/data/mysql.pid
user=mysql
tmpdir=/tmp
#导入文件存放路径
secure-file-priv='/User/zhengjian/Desktop' 
 ``` 
#### 2.
