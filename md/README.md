# Intelligente Wegführung von Mobilen Endgeräten auf der Basis von Hotspot
**Jin Zhang**

## [[Abstract]]
## [[Abstrakt]]
## [[Chapter1]] Introduction

## [[Chapter2]] Problem Statement
### Current problems(目前遇到的是什么问题)
### Current research results（别人研究出来啥玩意）
### Prospects of this study （本文研究的东西有没有前景）前景大大的

## [[Chapter3]] Methodology

### Research purpose（研究目标）
* find the network device (AP), which directly connects to a terminal
* HTTP Redirect
* dynamic

在转发启动的时候，所有的HTTP 请求都会被重定向到一个指定的服务器的IP 地址。这个服务器会返回一个网页，带有逃生路径的指示。

为了达到这个目标，需要找到任何一个终端所直连的网络设备。这不是一个特别精确的定位方式，但是比较快速。

### start Redirect (开启转发)

#### PF / PFCTL

#### iptables

#### DNS Redirect                (DNS 级别的转发)

### Command-line tool            (命令行工具)

#### SNMP commands               (SNMP 命令)
##### snmptable / snmpwalk
##### ipNetToMedia
##### Command on the switch       (在交换机上使用的命令)

#### ifconfig
#### arp -a / arp
#### ping / traceroute

### 构建网络拓扑结构
#### 为什么无法自动构建
#### 本文采用的构建方式

### Web 服务器
#### Apache
#### Python SimpleHTTPServer

### 编程语言
#### Python
#### Kivy
##### KvLang
#### Django
#### json
#### shell script

### 洪水算法
构建拓扑结构
寻找第一跳
递归查询

## [[Chapter4]] Implementation

### 实现中用到的设备
#### 苹果
安装和启动SNMP 服务
开启和关闭网络共享（两个方向），内核转发

#### 交换机
总是找不到它的IP
特殊的SNMP 命令

#### ASUS RT-N16
所有的接口MAC 相同
可以充当Router、AP 和Repeater

#### DLink
普通设备

### 开启/关闭转发
贴代码

### 启动/关闭服务
贴代码

### 管理界面
贴图

### 示例
#### 拓扑图

## [[Chapter5]] Evaluation
### 与其它研究的比较
最好能找到

### 有啥不足，也有啥贴金的地方
1. 无法自动构建网络
2. 延迟严重
3. 定位不精确
4. 命令没有加密
5. 子网的子网

我们最大的问题是，设备比较少，而且比较不专业、不统一。如果是进入实用环节，应该有统一的设备采购，采纳符合技术要求的设备。

### 未来的工作

## [[Chapter6]] Conclusion
