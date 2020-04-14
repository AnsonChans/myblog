# myblog
20190421
# 时隔一年重拾博客～惭愧，趁着休假（20200315
## 目标  
### 个人博客  
## 需求  
1.  文章列表
## 技术方案  
1.前端：react+webpack+antd+axios(暂定  
2.后台：koa2/express+mysql+redis（暂定  
### router和controller分开  
#### router只关注路由分配，根据路由来分配相应的数据和数据格式  
#### controller则只关注数据处理  

### server和前端的区别  
- 服务稳定性  
- 内存CPU(优化、拓展  
- 日志记录  
- 安全  
- 集群和服务拆分


# 服务端
### 路由和api  
## API
- 前端和后台、不同端（子系统）之间对接的一个术语  
- url 输入 输出  

## 路由
- API的一部分  
- 后端系统内部的一个定义  

***  
## mysql
- 安装下载（mysql,workbeach  
- 如何建库建表  
- 建表时常用的数据类型（int,bigint,varchar,longtext)  
- sql语句实现增删改查  
- [解决Node.js mysql客户端不支持认证协议引发](https://waylau.com/node.js-mysql-client-does-not-support-authentication-protocol/)


## api对接mysql（node原生  
- node连接mysql  
1. 创建链接对象   
2. connect()  
3. 执行操作(query)    
4. 断开连接
- 根据node_env区分配置  
- 封装exec函数 

## 登录  
- cookie和session  
### cookie  
- cookie定义和特点  
- 前后端如何查看修改cookie  
- 如何使用cookie登录验证  
### session  
- 不使用redis：  
1. session直接是js变量，放在nodejs进程内存中  
2. 进程内存有限，访问量过大时，内存爆增  
3. 正式线上多进程，进程之间内存无法共享  
- session写入redis  
1. web server最常用的缓存数据库，数据存放在内存中（读写快，昂贵）
2. session访问频繁，对性能要求高  
3. session可不考虑断电丢失数据的问题（内存硬伤  
4. session的数据量不会太大
- nginx反向代理  
1. 高性能的web服务器，开源免费  
2. 一般用于做静态服务、负载均衡  
3. 反向代理

1. session直接是js变量，放在nodejs进程内存中  

### 日志  
#### 分类  
- 访问日志（access log)  
- 自定义日志（自定义事件，错误） 
#### 步骤  
- nodejs 文件操作 node stream(提高性能    
- 日志功能开发和使用  
- 日志文件拆分（contrab，日志内容分析(readline  
### 安全  
#### 分类  
- sql注入：窃取数据库内容  
1. 原理  
2. 危害  
3. 预防（escape
- XSS攻击：窃取前端cookie内容  
1. 在页面展示内容参杂js代码,获取网页信息  
2. 预防（转换生成js的特殊字符
- 密码加密  
1. 使用crypto  


## 核心知识点(NODE原生  
1. http，nodejs处理http,处理路由，mysql  
2. cookie,session,redis,nginx反向代理  
3. sql注入，xss攻击，加密  
4. 日志，stream，contrab,readline  

## 线上环境  
1. 服务器稳定性  
2. 充分利用服务器硬件资源，提高性能  
3. 线上日志记录  

## PM2  
1. 进程守护，系统崩溃自动重启  
2. 启动多线程，充分使用CPU和内存  
3. 自带日志功能  

## PM2使用  
1. 下载安装  
2. 基本使用，和nodemon的区别  
3. 常用命令，包括：list start restart stop delete info log monit. 

## PM2配置  
1. PM2配置文件（包括进程数量，日志文件目录等  
2. 修改PM2启动命令，重启  
3. 访问server,检查日志文件的内容（日志记录是否生效

