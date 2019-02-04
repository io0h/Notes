1.centos安装mongodb

```
yum install mongodb
yum install mongodb-server
```


2.配置mongodb的db目录，先在/data 下面创建名称为mongod的目录

3.修改目录的所有者

```
chown -R mongodb:mongodb /data/mongo
```

4.修改mongo的配置文件

```
vim /etc/mongodb.conf
```

设置

```
dbpath = /data/mongo/
```

5.启动mongod


```
service mongod start
```

6.连接mongo后配置mongo的用户名和密码

```
mongo

use admin
db.addUser('username','password')
exit
```

7.修改mongodb.conf

注释`bind_ip`
反注释`auth = true`


```
#bind_ip = 127.0.0.1
auth = true 
```

8.重启monogd


```
service mongod restart
```

9.配置mongodb 开机启动


```
chkconfig mongod on
```
