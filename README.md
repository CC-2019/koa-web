# koa-web
nodejs koa web

## How to use
首要要安装nodejs，nodejs 的版本必须7.6.0以上

```bash
$ node -v
v8.0.0
```

使用git下载代码库
```bash
$ git clone https://github.com/CC-2019/koa-web.git
```

安装依赖库

```bash
$ cd koa-web
$ npm install
```

启动

```bash
$ node app.js
```
linux 服务器后台启动
```bash
$ nohup node app.js >> /home/work/logs/koa-web.log 2>&1 &
```

## 说明


**框架**
此web 使用了koa2 框架，依赖的库和中间件查看 package.json，只要在根目录下 执行 `npm install` 即可安装相关依赖

**网站概念**

url: 会包括域名，端口，子路径，和参数

```
http://www.czjb.site:8006/
hhttp://www.czjb.site:8006/signin
http://www.czjb.site:8006/getbook?bookid=1212
```

get/post

常用http请求，会包括get 和 post请求，此外还有 put delete 等，get请求的参数通常在问号后面，post的参数在请求的body里面

静态文件

一个网站会有很多静态文件，例如 css 文件， js 文件， image 文件，服务器在处理这种静态文件时，会直接返回文件

路由

服务器根据 url 路径，寻址到对应的处理函数过程

比如此demo中 的 http://www.czjb.site:8006/signin，会根据 signin 找到 controllers/signin.js 里面的处理方法

本demo中 如果想增加新的路由，只要在 controllers 下增加 新的js 文件，配置好相应路由和处理函数即可
