# GoKu API Gateway CE（悟空API网关 开源版）

![](http://data.eolinker.com/course/Y9EYfxU069c9bc2f7a7f1e211966173e296cd04f768ee82)

## 简介

**GoKu API Gateway CE，中文名：悟空API网关（开源版），是国内首个开源go语言API网关，帮助企业进行API服务治理、API性能安全维护，为企业数字化赋能。**

GoKu API Gateway CE，支持OpenAPI与微服务管理，支持私有云部署，实现API转发、请求参数转换、数据校验等功能，提供图形化界面管理，能够快速管理多个API网关，提高API业务安全性。

## 特性

1. **免费且开源**：GoKu API Gateway秉承开源精神，是国内第一个企业开源的API接口网关，为广大的开发、运维以及管理人员提供专业的产品。

2. **多种鉴权方式**：支持Basic 认证、API Key授权、IP认证、无认证等方式。

3. **支持Open API**：不同账户拥有独立的访问密钥。

4. **权限管理**：可针对不同策略组设置流量控制策略，包括访问QPS、访问总次数、访问IP、访问时间段等

5. **请求转发**：默认支持http路由。

6. **IP黑白名单**：支持全局IP白名单、也可自定义某个接口的IP白名单。

7. **数据整形**：支持参数的转换与绑定，支持formdata、raw数据、json。

8. **配置文件**：支持配置文件修改网关配置。

9. **快速部署**：支持手动部署与Docker部署。

## Roadmap

1. **UI界面**：支持通过UI界面修改网关配置。

2. **API支持**：支持通过API对网关进行操作。

3. **兼容eoLinker-AMS**：可与国内最大的接口管理平台打通。

4. **支持Restful**：支持rest路由。

6. **告警设置**：当系统达到预设告警条件时，邮件通知运维人员。

7. **超时设置**：配置访问超时时间，网关控制超时后立即返回，防止系统雪崩。

	**……**

## 图片介绍

![](http://data.eolinker.com/course/a9l9ZzQfe7cfc0f93578629db01a1a3197864dd51fa9dab)

![](http://data.eolinker.com/course/3KDiWxscb527a460477f5bbb95fc3db6c09426c47de96f1)

![](http://data.eolinker.com/course/pRMJNTb1974cd4d502bf17f5b477b236cf5c090496af571)


## 部署要求

* go 1.8及以上版本

## 相关链接

* 官方网站：https://agw.eolinker.com

* Github：https://github.com/eolinker/GoKu-API-Gateway

* 码云：https://gitee.com/eoLinker-API-Management/API-Gateway

* Coding：https://git.coding.net/eolinker/Goku-API-Gateway.git

* 教程文档：http://help.eolinker.com/agw

* 官方交流Q群：[用户交流1群](https://jq.qq.com/?_wv=1027&k=5ikfC2S)（群号：725853895）

## 更新日志

#### V1.0.0(2018/4/17)
新增：

1. “网关概况”新增监控信息，方便监控API运行状况，包括：请求总数、成功请求数、失败请求数、每分钟实时访问次数等；
2. “权限控制”新增策略组，每个策略组下包括鉴权方式、IP黑白名单、流量控制三大模块；
3. 强化鉴权方式，包括Basic Auth、API Key、无认证；
4. 强化流量控制，支持允许访问时间段与禁止访问时间段；
5. 强化流量控制，支持设置每秒最大访问次数、每分钟最大访问次数、每小时最大访问次数、每天最大访问次数。

优化：

1. 全面优化界面；
2. 优化访问性能。

其他：

1. 加入开源声明。

#### V1.0.1（2018/4/17）
修复：

1. 某个脚本的编码错误。

#### V1.0.2（2018/4/19）
新增:

1. “接口分组”与“接口详情”可选择拼接网关地址与策略组id，方便查看请求地址。

修复：

1. “鉴权方式”里API Key显示错位问题;
2. 修复mysql5.7环境下，sql脚本执行失败;
3. 修复访问网关后端服务时，请求提示错误的问题。

#### V1.0.3（2018/4/20）
修复：

1. 修复“鉴权方式”编辑页错位问题。

#### V2.0.0（2018/5/4）
新增：

1. 通过配置文件修改网关配置；
2. 新增全局IP黑白名单；
3. 参数新增支持json类型。

优化：

1. 架构优化，减少第三方依赖，提升网关性能；
2. 弃置mysql、redis数据库的使用，改用配置文件方式读取文件配置。