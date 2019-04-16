# 系统配置

系统中有 3 个配置文件: 
 * `application.properties`: 核心配置文件, 一般用于配置系统通用的选项
 * `application-dev.properties`: 开发环境配置文件，对于相同值，会覆盖核心配置文件
 * `application-prod.properties`: 生产环境配置文件，对于相同值，会覆盖核心配置文件


> 可在 `application.properties` 中配置启用 `dev` 环境还是 `prod` 环境 : `spring.profiles.active=dev`

## 超级管理员

对于权限系统，一般都有一个**超级管理员**用来分配权限，做一些系统的初始化工作，配置方式为：

```properties
security.super-admin.username=admin
```

> 可在相应的 dev 和 prod 环境中配置不同的超级管理员，如不配置，默认值为 `admin`。

## 登录验证码

配置登录时是否开启验证码功能，默认值为 `false`。

```properties
security.login.verify=false
```

## 登录失败次数


配置在 10 分钟内登录失败次数限制，默认值为 `5` 次。

```properties
security.retry.count=5
```

## 登录日志

配置是否记录登录日志，一般开发环境关闭，生产环境开启。关闭后首页的 `近七天登录次数统计图` 也不会再更新。

```properties
log.login = false
```

## 操作日志

配置是否记录操作日志，一般开发环境关闭，生产环境开启。

```properties
log.operation = false
```