# 快速入门

## 演示地址

在线地址 : [http://shiro.zhaojun.im/](http://shiro.zhaojun.im/)

?> 默认管理员账号: `admin`，密码: `123456`。<br> 普通用户账号: `user`，密码: `123456`。

!> 为了不影响其他人的浏览体验, 请尽量不要进行删除类的敏感操作.

## 运行环境

* JDK 1.8
* MySQL 5.7
* Redis

## 下载项目

```git
git clone https://github.com/zhaojun1998/Shiro-Action.git
```

## 导入项目

使用自己的 IDE 导入, Eclipse 和 Intellij IDEA 均可.

## 导入数据库

创建数据库, 字符集选择 `utf8`, 排序规则选择 `utf8_general_ci`.

然后导入 `shiro_action.sql` 到数据库中.


## 配置文件

打开 `application.properties` 修改 `MySQL` 和 `Redis` 连接信息.

```properties
spring.redis.host=127.0.0.1
spring.redis.port=6379
spring.cache.type=redis

spring.datasource.username=root
spring.datasource.password=123456
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/shiro_action?useSSL=false&characterEncoding=UTF8
```

## 启动项目
在完成了上述步骤后，找到 ShiroActionApplication 启动类, 启动即可.

启动后访问地址为：http://localhost:8080 , 用户名：admin, 密码：123456.