#Wordpress-hyperdb

预先安装了hyperdb的Wordpress镜像
能够让Wordpress配置多个数据库连接，并且分离数据库的读写操作到不同的数据库

写操作 -> mysql master
读操作 -> mysql slave

### 配置
新增如下环境变量

REPLICA_DB_HOST：只读数据库地址
REPLICA_DB_PORT：只读数据库端口
REPLICA_DB_USER: 只读数据库连接用户
REPLICA_DB_PASSWORD: 只读数据库连接密码
REPLICA_DB_NAME: 只读数据库名


## build镜像

```
docker build -t registry-bj.capitalonline.net/cck-example/wordpress:hyperdb
```



