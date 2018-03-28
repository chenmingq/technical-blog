# nginx使用配置
```
$ cd /usrl/local/nginx/conf/
```
```
$ mkdir conf.d
```
```
$ touch xxx.conf
```
```
$ vim xxx.conf
```
```
server {
     listen      80;
     server_name requestDomainName; # 多个以空格隔开 a.com b.com
     root htmlPath; #如 /home/name/html/project/
     index index.html;

     location /api {
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_http_version 1.1;
        proxy_set_header Connection "";
        proxy_pass http://127.0.0.1:8080;
     }

     access_log logs/xxx.log;
}

```
```
$ cd ../

```
```
$ vim nginx.conf
```

```
worker_processes  1;

error_log logs/nginx_error.log warn;

pid /tmp/nginx.pid;

worker_rlimit_nofile 655360;

events {
    use epoll;
    worker_connections 102400;
}

http {

        add_header Z-Proxy $hostname;

        #include extra_conf_default_http.conf;
        #include extra_conf4proxy_log_format.conf;

        include conf.d/*.conf;
        include mime.types;
}

```
- 重启nginx
```
$ cd /usr/local/nginx/sbin
```
- 启动
```
 ./nginx
```
- 重启
```
 ./nginx -s reload
```
