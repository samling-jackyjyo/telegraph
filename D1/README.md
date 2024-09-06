# 简介

支持worker&pages部署。使用cloudflare d1数据库作为储存。

# 更新
一般情况下，只需更新[_worker.js](https://raw.githubusercontent.com/0-RTT/telegraph/main/D1/_worker.js)文件中的代码。如有特殊情况，将另行通知。

# 需要使用的变量

| 变量名          | 说明                                                                 |
|-----------------|----------------------------------------------------------------------|
| DOMAIN          | 自定义域名 示例：example.com                                         |
| USERNAME        | 用于身份验证的用户名 示例：123                                       |
| PASSWORD        | 用于身份验证的密码 示例：123                                         |
| ADMIN_PATH      | 管理页面的路径 示例：admin                                           |
| ENABLE_AUTH     | 设置为true时开启启用身份验证                                         |
| NSFW_THRESHOLD  | 图片审查的强度，0-1，越接近1越宽松                                   |
| DATABASE        | 数据库绑定的变量                                                     |
| NSFW_API_URL    | 填写图片审查API意味着开启该功能，填写变量后开启。示例 API: https://api.jiasu.in/nsfw |

数据库初始化命令
```
CREATE TABLE media (
    key TEXT PRIMARY KEY,
    timestamp INTEGER NOT NULL,
    url TEXT NOT NULL
);

```

图片教程稍后更新。。。
