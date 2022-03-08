### 解决jenkins拉取gitlab https模式报128错误
```
git config --global http.sslVerify false
```


### 需要在挂载目录下创建ssl目录并放入证书

> 注意https监听端口  

### 生产环境建议使用外部redis 和 postgresql

> redis
> [设置外部redis](https://docs.gitlab.com/omnibus/settings/redis.html)
```
# Disable the bundled Redis
redis['enable'] = false

# Redis via TCP
gitlab_rails['redis_host'] = '127.0.0.1'
gitlab_rails['redis_port'] = 6379

# OR Redis via Unix domain sockets
gitlab_rails['redis_socket'] = '/tmp/redis.sock' # defaults to /var/opt/gitlab/redis/redis.socket

# Password to Authenticate to alternate local Redis if required
gitlab_rails['redis_password'] = '<redis_password>'
```

> postgresql
> [设置外部postgresql](https://docs.gitlab.com/ee/administration/postgresql/external.html)
```
# Disable the bundled Omnibus provided PostgreSQL
postgresql['enable'] = false

# PostgreSQL connection details
gitlab_rails['db_adapter'] = 'postgresql'
gitlab_rails['db_encoding'] = 'unicode'
gitlab_rails['db_host'] = '10.1.0.5' # IP/hostname of database server
gitlab_rails['db_password'] = 'DB password'
```
