# Chapter 3 Methodology

This chapter will 


## Console commands

To interactive with the network devices, console commands are used in different situations in this master thesis. It's used to activate /deactivate the server and redirection, get the list of media interfaces of the network devices, fetch the information of SNMP, and so on.

This section will list the console commands that used in this articles.


This 

#### (1) snmpwalk
The **snmpwalk** commnd describes the 

#### snmptable
The 

#### ping
The **ping** command

#### ifconfig

The command **ifconfig** means ***interface configuration***. 

##### _ifconfig_ output Sample 1
The output of  _ifconfig_ on a Mac Computer is listed below. 

```
lo0: flags=8049<UP,LOOPBACK,RUNNING,MULTICAST> mtu 16384
	options=3<RXCSUM,TXCSUM>
	inet6 ::1 prefixlen 128 
	inet 127.0.0.1 netmask 0xff000000 
	inet6 fe80::1%lo0 prefixlen 64 scopeid 0x1 
	nd6 options=1<PERFORMNUD>
gif0: flags=8010<POINTOPOINT,MULTICAST> mtu 1280
stf0: flags=0<> mtu 1280
en0: flags=8963<UP,BROADCAST,SMART,RUNNING,PROMISC,SIMPLEX,MULTICAST> mtu 1500
	options=10b<RXCSUM,TXCSUM,VLAN_HWTAGGING,AV>
	ether 40:6c:8f:04:e6:69 
	nd6 options=1<PERFORMNUD>
	media: autoselect (none)
	status: inactive
en1: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	ether 10:40:f3:9f:49:e2 
	inet6 fe80::1240:f3ff:fe9f:49e2%en1 prefixlen 64 scopeid 0x5 
	inet 192.168.0.35 netmask 0xffffff00 broadcast 192.168.0.255
	nd6 options=1<PERFORMNUD>
	media: autoselect
	status: active
en2: flags=963<UP,BROADCAST,SMART,RUNNING,PROMISC,SIMPLEX> mtu 1500
	options=60<TSO4,TSO6>
	ether d2:00:1d:59:c3:e0 
	media: autoselect <full-duplex>
	status: inactive
fw0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 4078
	lladdr 3c:07:54:ff:fe:d5:9c:3e 
	inet 192.168.2.1 netmask 0xffffff00 broadcast 192.168.2.255
	inet6 fe80::3e07:54ff:fed5:9c3e%fw0 prefixlen 64 scopeid 0x7 
	nd6 options=1<PERFORMNUD>
	media: autoselect <full-duplex>
	status: inactive
p2p0: flags=8843<UP,BROADCAST,RUNNING,SIMPLEX,MULTICAST> mtu 2304
	ether 02:40:f3:9f:49:e2 
	media: autoselect
	status: inactive
bridge0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=63<RXCSUM,TXCSUM,TSO4,TSO6>
	ether 42:6c:8f:40:07:00 
	inet 192.168.4.1 netmask 0xffffff00 broadcast 192.168.4.255
	inet6 fe80::406c:8fff:fe40:700%bridge0 prefixlen 64 scopeid 0x9 
	Configuration:
		id 0:0:0:0:0:0 priority 0 hellotime 0 fwddelay 0
		maxage 0 holdcnt 0 proto stp maxaddr 100 timeout 1200
		root id 0:0:0:0:0:0 priority 0 ifcost 0 port 0
		ipfilter disabled flags 0x2
	member: en2 flags=3<LEARNING,DISCOVER>
	        ifmaxaddr 0 port 6 priority 0 path cost 0
	nd6 options=1<PERFORMNUD>
	media: <unknown type>
	status: inactive
bridge100: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
	options=3<RXCSUM,TXCSUM>
	ether 42:6c:8f:40:07:64 
	inet 192.168.3.1 netmask 0xffffff00 broadcast 192.168.3.255
	inet6 fe80::406c:8fff:fe40:764%bridge100 prefixlen 64 scopeid 0xa 
	Configuration:
		id 0:0:0:0:0:0 priority 0 hellotime 0 fwddelay 0
		maxage 0 holdcnt 0 proto stp maxaddr 100 timeout 1200
		root id 0:0:0:0:0:0 priority 0 ifcost 0 port 0
		ipfilter disabled flags 0x2
	member: en0 flags=3<LEARNING,DISCOVER>
	        ifmaxaddr 0 port 4 priority 0 path cost 0
	nd6 options=1<PERFORMNUD>
	media: <unknown type>
	status: inactive
```

#### arp

arp -a

#### pfctl

#### iptables

### HTTP Redirection

When the automatical locating service begin, a HTTP redirection will be activated. All the HTTP request will be redirected to a specific URL.

### 

### Summary

This chapter describes the technology basis to reach the destination.


## [Section 3.1. Research ]
## Research purpose          （研究目标）
* find the network device (AP), which directly connects to a terminal
* HTTP Redirect
* dynamic

在转发启动的时候，所有的HTTP 请求都会被重定向到一个指定的服务器的IP 地址。这个服务器会返回一个网页，带有逃生路径的指示。

为了达到这个目标，需要找到任何一个终端所直连的网络设备。这不是一个特别精确的定位方式，但是比较快速。

## [Section 3.2. Localization Process](localization.md)
## [Section 3.3. Redirection](Chapter3/redirection.md)
 start Redirect               (开启转发)
### PF / PFCTL
### iptables
#### DNS Redirect                (DNS 级别的转发)

### Command-line tool            (命令行工具)

#### SNMP commands               (SNMP 命令)
##### snmptable / snmpwalk
##### ipNetToMedia
##### Command on the switch       (在交换机上使用的命令)

#### ifconfig
#### arp -a / arp
#### ping / traceroute

### Construction of the network topology   (构建网络拓扑结构)
####    为什么无法自动构建
####    本文采用的构建方式

### Web server                             (Web 服务器)
#### Apache
#### Python SimpleHTTPServer

### Programming language                  (编程语言)
#### Python
#### Kivy
##### KvLang
#### Django
#### json
#### shell script

### Flood Algorithm          (洪水算法)
Recursive Query
构建拓扑结构
寻找第一跳
递归查询
