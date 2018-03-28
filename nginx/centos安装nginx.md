# 准备工作
- gcc 安装
```
yum install gcc-c++
```
-  PCRE pcre-devel 安装
```
yum install -y pcre pcre-devel
```
-  zlib 安装
```
yum install -y zlib zlib-devel
```
- OpenSSL 安装
```
yum install -y openssl openssl-devel
```

# 下载nginx
- [ngxin官网下载](http://nginx.org/en/download.html)
```
$ tar xvf nginx-version.tar.gz

```
# 开始安装
- 进入解压完成的nginx 目录
```
$ cd /nginxpath
```

- 开始使用默认配置nginx
```
$ ./configure
```

- 编译nginx
```
$ make 
```
- make 完成后进行make install
```
$ make install
```
- 完成后可进行进入nginx安装好的目录
```
$ cd /usr/local/nginx
```