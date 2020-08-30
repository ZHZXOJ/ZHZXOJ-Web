# ZHZXOJ-Web
基于SYZOJ前端改版，现在仍在开发ing

## 若要使用https，请在oj的nginx配置文件中加入以下语句
```
listen 443 ssl http2;
if ($server_port !~ 443){
    rewrite ^(/.*)$ https://$host$1 permanent;
}
ssl_certificate  *.crt;
ssl_certificate_key  *.key;
#以下为可选项
#ssl_protocols TLSv1.1 TLSv1.2 TLSv1.3;
#ssl_ciphers ECDHE-RSA-AES128-GCM-SHA256:HIGH:!aNULL:!MD5:!RC4:!DHE;
#ssl_prefer_server_ciphers on;
#ssl_session_timeout 10m;
#ssl_session_cache shared:SSL:10m;
#error_page 497  https://$host$request_uri;
```

## 用户标签（首页、个人主页、排行榜）
可以使用`nameplate`字段，为了方便操作管理，该分支在`user`表中插入了`tg_name`和`tg_color`字段。
```
tg_name:标签内容
tg_color:标签颜色
```
