# 生成ssl证书: 
```
openssl req -newkey rsa:2048 -nodes -sha256 -keyout certs/domain.key -x509 -days 365 -out certs/domain.crt
```



节点安装ca证书:
```
mkdir -p /etc/docker/certs.d/mydomain.com:5000
cp certs/domain.crt /etc/docker/certs.d/mydomain.com:5000/ca.crt
systemctl restart docker                                                 //安装证书后，重启Docker Daemon
```
