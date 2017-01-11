---
title: 将SOCKS代理转为http代理
date: 2017-01-11 22:21:38
tags:
---

## 将SOCKS代理转为http代理

*[Polipo](https://www.irif.fr/~jch/software/polipo/) is a small and fast caching web proxy (a web cache, an HTTP proxy, a proxy server)*

#### 配置
安装好polipo，编辑它的配置文件(etc/polico/config)
```
proxyAddress = "0.0.0.0"#使用本机作为代理服务器
proxyPort = 8123#http代理服务端口
socksParentProxy = "0.0.0.0:1028"#把后面的1028改成刚刚配置的shadowsocks本地端口
socksProxyType = socks5 #shdadowsocks为socks5代理
```
