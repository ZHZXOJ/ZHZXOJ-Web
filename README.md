# ZHZXOJ-Web
基于SYZOJ前端改版，现在仍在开发ing

## 若要使用错误响应页面，请在oj的nginx配置文件中加入以下语句
```
proxy_intercept_errors on;
error_page 404 https://$server_name/404?code=404-NOF;
#以下为可选项
#access_log  access.log;
#error_log  error.log;
```

## 用户标签（首页、个人主页、排行榜）
请在`user`表中插入`tg_name`和`tg_color`字段，并将其默认值为`null`。
```
tg_name:标签内容
tg_color:标签颜色
```