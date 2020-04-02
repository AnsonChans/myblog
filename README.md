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
## router只关注路由分配，根据路由来分配相应的数据和数据格式  
## controller则只关注数据处理

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
