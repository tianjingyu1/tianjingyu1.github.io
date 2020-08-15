# 功能介绍

Burp Suite是用于攻击web应用程序的集成平台，包含了许多工具。Burp Suite为这些工具设计了许多接口，以加快攻击应用程序的过程。所有工具都共享一个请求，并能处理对应的HTTP消息、持久性、认证、代理、日志、警报。

Burp Suite是由JAVA语言编写，所以Burpsuite是一款跨平台的软件。但是在测试过程中BurpSuite不像其他自动化测试工具不需要输入任何内容即可完成测试，而需要手动配置某些参数触发对应的行为才会完成测试。

BurpSuite 官方网址 https://portswigger.net/burp/

各版本的最主要区别在于web漏洞扫描

# 设置burpsuite字体

user options-> Display

# 配置浏览器代理

## 在浏览器中安装BurpSuite CA证书

1. 使用系统管理员权限打开浏览器
2. 再浏览器中输入http://burp/
3. 安装CA证书

# Proxy模块

Burp Proxy是Burp Suite以用户驱动测试流程功能的核心，通过代理模式，可以让我们拦截、查看、修改所有在客户端和服务端之间传输的数据

## intercept介绍

Forward表示将截断的HTTP或HTTPS请求发送到服务器
Drop表示将截断的HTTP或HTTPS请求丢弃
Intercept is on 和Intercept is off表示开启或关闭代理截断功能
Action表示将代理截断的HTTP或HTTPS请求发送到其他模块或做其他处理
对Intercept进行Raw Hex Params Header切换查看不同的数据格式

## HTTP history介绍

HTTP history用来查看提交过的HTTP请求
Filter可以过滤显示某些HTTP请求。点击FILTER就可以打开。对于指定URL可以选中右键点击，执行其他操作。WebSockets history与HTTP history功能类似

## Options介绍

Options具有的功能：代理监听设置、截断客户端请求、截断服务器响应、截断WebSocket通信服务端响应修改（绕过JS验证文件上传）、匹配与替换HTTP消息中的内容、通过SSL连接Web服务器配置、其他配置选项

### 设置Proxy Listener

通过设置Proxy Listeners来截断数据流量。比如设置监听端口等

### 设置Intercept lient Requests

通过设置Intercept Client Requests来截断符合条件的HTTP请求

### 设置Intercept Server Response

通过设置Intercept Server Response来筛选出符合条件的HTTP响应

### 设置截断Websocket通信以及修改Response的内容

### 匹配以及修改HTTP消息

可以修改HTTP请求和HTTP响应中的内容

### 设置使用SSL连接到Web服务器

设置使用Burp直接通过SSL直连到目标服务器

### 杂项设置

通过杂项设置对应的请求头等信息
