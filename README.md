# HTTP_example
## http请求部分内容
### GET http://www.baidu.com/index.html HTTP/1.0
### User-Agent:Wget/1.12 (linux-gnu)
### Host:www.baidu.com
### connect:close

### GET http://www.baidu.com/index.html HTTP/1.0为请求行

#### GET只读的方式申请资源；
#### http请求方法
#### GET：申请获取资源，而不对服务器产生任何影响
#### HEAD：申请获取资源，但只要求服务器返回头部信息，而不需要传输任何实际内容
#### POST：客户端向服务器提交数据，会影响服务器，服务器会根据接收到的数据创建新的资源，或者更新已有资源
#### PUT：上传某个资源
#### DELETE：删除某个资源
#### TRACE：要求目标服务器返回原始http请求内容
#### OPTIONS：查看服务器对某个特定的url都支持哪些请求方法
#### CONNECT：用于某些代理服务器，将请求的链接转化为安全隧道
#### PATCH：对资源做部分修改

#### http://www.baidu.com/index.html为目标资源的url
#### http为scheme，即获取目标资源的应用层协议，包括ftp、rtsp和file等
#### www.baidu.com为目标资源所在的主机
#### index.html为资源文件的名字，服务器根目录中的索引文件

#### HTTP/1.0表示客户端使用的HTTP版本号为1.0

### User-Agent:Wget/1.12 (linux-gnu)
### Host:www.baidu.com
### connect:close
### 为HTTP请求的头部字段

### User-Agent:Wget/1.12 (linux-gnu)表示客户端使用的程序时Wget
### Host:www.baidu.com表示目标主机名为：www.baidu.com，头部必须包含该选项
### connect:close表示请求完成后立刻关闭（keep-alive表示请求完成后保持一段时间等待后续请求）
### 请求行和头部字段每一行以回车符和换行符结束

### 请求头部字段之后为一个空行，空行之后为可选消息体，如果有可选消息体，头部必须包含Content-Length段


## http应答部分
### HTTP/1.0 200 OK
### Server:BWS/1.0
### Content-Length:8024
### Content-Type:text/html;charset=gdk
### Set-Cookie:BAIDUD=A5B6C72D68CF639CE8896FD79A03FBD8:FG=1;expire=Wed,04 -Jul-42 00:10:47 GMT; path=/.;domain=.baidu.com
### via:1.0 localhost (squid/3.0 STABLE18)

### HTTP/1.0 200 OK为状态行
### HTTP/1.0为版本号，200 OK为状态码和状态信息
### 状态类型          状态码和状态信息        含义
### 1xx信息           100 Continue
### 2xx成功           200 OK
### 3xx重定向         301 Moved Permanently
### 3xx重定向         302 Found
### 3xx重定向         304 No Modified
### 3xx重定向         307 Temporary Redirect
### 4xx客户端错误     400 Bad Request 
### 4xx客户端错误     401 Unauthorized
### 4xx客户端错误     403 Forbidden
### 4xx客户端错误     404 No Found
### 4xx客户端错误     407 Proxy Authentication Require
### 5xx服务器错误     500 Internet Server Error
### 5xx服务器错误     503 Service Unavailable

### Server:BWS/1.0
### Content-Length:8024
### Content-Type:text/html;charset=gdk
### Set-Cookie:BAIDUD=A5B6C72D68CF639CE8896FD79A03FBD8:FG=1;expire=Wed,04 -Jul-42 00:10:47 GMT; path=/.;domain=.baidu.com
### via:1.0 localhost (squid/3.0 STABLE18)
### 为应答的头部字段

### Server:BWS/1.0表示web服务器的名字为BWS
### Content-Length:8024表示目标文档的长度为8024
### Content-Type:text/html;charset=gdk表示目标文档的MIME类型，text为主文档类型，html为子文档类型，charset=gdk文档的字符编码

### Set-Cookie:BAIDUD=A5B6C72D68CF639CE8896FD79A03FBD8:FG=1;expire=Wed,04 -Jul-42 00:10:47 GMT; path=/.;domain=.baidu.com
#### BAIDUD为Cookie的名字
#### expire指定Cookie的生存时间
#### path指定Cookie生效的路径 domain指定Cookie生效的域名
#### Cookie用于保持Cookie的连接状态，表示上下文信息

### via:1.0 localhost (squid/3.0 STABLE18)经过的代理服务器的名字和地址
### 请求行和头部字段每一行以回车符和换行符结束

### 请求头部字段之后为一个空行，空行之后为请求文档内容。
