wiki.nginx.org/3rdPartyModules

user:worker进程的用户或用户组
worker_processes:cpu核数* 1.5~2

nginx AIO机制与sendfile机制

非http类型的上游服务器 upstream
memcached fastcgi

nginx:
try_files的配置可以看一下
internal

geoip
基于原始地址阻止流量

反向代理服务器优化:
缓冲: proxy_buffer
缓存: proxy_cache
    etag
    
    cache-control:
    no-cache
    no-store
    private
    max-age
    
    expires
存储: proxy_store_access
压缩: gzip

satisfy any
autoindex
disable_symlinks
limit_req

$binary_remote_addr

流媒体：
location /videos {
    mp4;
}

addition模块
在响应前或后添加文本

sub模块
在响应前或后替换文本

xslt
使用xslt样式表转换xml

SSI:server side includes
网页中嵌入处理逻辑

nginx决策
perl模块

创建安全链接
试用于不想使用完整认证系统的
文件1.txt,密码123456
echo -n '1.txt123456' | md5sum
7a8ea3316169e9e080ed9dfdbde3bc4c 
http://10.1.11.41/download/7a8ea3316169e9e080ed9dfdbde3bc4c/1.txt

location /download/ {
    secure_link_secret 123456;
    if ($secure_link = "") {
        return 403;
    }
    try_files /download/$secure_link =404;
}

处理图像
image_filter
empty_gif

跟踪网站访问者
userid

防止意外代码执行
include fastcgi_params

kill -USR2 nginx.pid
启动一个新的nginx  master进程，nginx.pid会重命名成nginx.pid.oldbin

kill -WINCH nginx.pid.oldbin
旧的nginx停止新的请求，并当请求处理完成之后淘汰旧的worker

kill -QUIT nginx.pid.oldbin
退出旧的nginx

回滚就的nginx
kill -HUP nginx.pid.oldbin
kill -QUIT nginx.pid 

强制终止nginx
kill -TERM nginx.pid 

error_log级别
debug_core 
debug_alloc
debug_mutex
debug_event
debug_http
debug_imap

用tryfiles代替if

stub status 自检模块，统计nginx请求
