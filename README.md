# Computer-network
计算机网络的基本知识

<h3>计算机网络的TCP/IP五层模型</h3>
从上至下：<br>
应用层：SMTP（邮件传输协议）、HTTP（超文本传输协议）、DNS（域名解析协议）、FTP（文件传输协议）<br>
传输层：TCP（面向连接的，可靠的字节流服务）、UDP（面向无连接的，不可靠的数据报服务）<br>
网络层:IP（不可靠、无连接的传送服务）、ARP（解析IP地址获取MAC地址）<br>
数据链路层:帧<br>
物理层:物理媒介<br>

<h3>为什么要三次握手</h3>
三次握手：客户端向服务器发送SYN请求连接，服务端发送ACK确认连接，客户端发送ACK确认连接<br>
有时客户端发送请求时发生阻塞客户端会再发送一次，服务端于是收到了两个请求有两个响应，但实际只要一个，若多次发送请求会造成资源浪费<br>

四次挥手：客户端向服务器发送FIN请求断开连接，服务端发送ACK确认断开，再发送FIN断开和客户端的连接，客户端发送ACK确认断开连接

<h3>当在浏览器输入了一个网址后发生了什么</h3>
1.首先dns协议解析网址，获得服务器的IP地址<br>
2.TCP三次握手建立连接<br>
3.浏览器发送HTTP请求（请求头、请求行、空行、请求数据）<br>
4.服务器处理请求<br>
5.浏览器渲染页面<br>
6.断开连接，TCP四次挥手<br>

<h3>HTTP和HTTPS的区别</h3>
HTTP是明文传输的，数据未加密，安全性差，HTTPS除了HTTP还包括SSL加密，更加安全<br>
HTTP的端口为80，HTTPS的端口为443<br>
HTTP的响应速度更快，HTTP使用TCP三次握手，三个包，而HTTPS除了TCP还有SSL，需要9个包，共12个包，所以HTTPS也更消耗服务器资源<br>
HTTPS需要CA证书，需要一定的费用<br>

<h3>HTTP1.0和HTTP1.1的区别总结</h3>
长连接<br>
Host域<br>
带宽优化<br>
消息传递<br>
缓存<br>

