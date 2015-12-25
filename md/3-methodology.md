# Chapter 3 Methodology

This chapter will 


## Console commands

To interactive with the network devices, console commands are used in different situations in this master thesis. It's used to activate /deactivate the server and redirection, get the list of media interfaces of the network devices, fetch the information of SNMP, and so on.

This section will list the console commands that used in this articles.


This 

#### (1) snmpwalk
The **snmpwalk** commnd will output all the tables of a SNMP server in key-value pair format. The usage is:

> snampwalk -v 2c -c public <Host IP> [table name]

If the _[table name]_ is specified, only the corresponding table will be outputted.

Because that the _snmpwalk_ will output a lot of informations, and most of them are redudant, so a sample of _snmpwalk_ output is putted in the chapter **attachments**. A typical _snmpwalk_ output, which is useful in this master thsis, is listed below:

```
IF-MIB::ifNumber.0 = INTEGER: 10
IF-MIB::ifIndex.1 = INTEGER: 1
IF-MIB::ifIndex.2 = INTEGER: 2
IF-MIB::ifIndex.3 = INTEGER: 3
IF-MIB::ifIndex.4 = INTEGER: 4
IF-MIB::ifIndex.5 = INTEGER: 5
IF-MIB::ifIndex.6 = INTEGER: 6
IF-MIB::ifIndex.7 = INTEGER: 7
IF-MIB::ifIndex.8 = INTEGER: 8
IF-MIB::ifIndex.9 = INTEGER: 9
IF-MIB::ifIndex.10 = INTEGER: 10
IF-MIB::ifDescr.1 = STRING: lo0
IF-MIB::ifDescr.2 = STRING: gif0
IF-MIB::ifDescr.3 = STRING: stf0
IF-MIB::ifDescr.4 = STRING: en0
IF-MIB::ifDescr.5 = STRING: en1
IF-MIB::ifDescr.6 = STRING: en2
IF-MIB::ifDescr.7 = STRING: fw0
IF-MIB::ifDescr.8 = STRING: p2p0
IF-MIB::ifDescr.9 = STRING: bridge0
IF-MIB::ifDescr.10 = STRING: bridge100
IF-MIB::ifType.1 = INTEGER: softwareLoopback(24)
IF-MIB::ifType.2 = INTEGER: ieee80212(55)
IF-MIB::ifType.3 = INTEGER: hippiInterface(57)
IF-MIB::ifType.4 = INTEGER: ethernetCsmacd(6)
IF-MIB::ifType.5 = INTEGER: ethernetCsmacd(6)
IF-MIB::ifType.6 = INTEGER: ethernetCsmacd(6)
IF-MIB::ifType.7 = INTEGER: ieee1394(144)
IF-MIB::ifType.8 = INTEGER: ethernetCsmacd(6)
IF-MIB::ifType.9 = INTEGER: bridge(209)
IF-MIB::ifType.10 = INTEGER: bridge(209)
IF-MIB::ifMtu.1 = INTEGER: 16384
IF-MIB::ifMtu.2 = INTEGER: 1280
IF-MIB::ifMtu.3 = INTEGER: 1280
IF-MIB::ifMtu.4 = INTEGER: 1500
IF-MIB::ifMtu.5 = INTEGER: 1500
IF-MIB::ifMtu.6 = INTEGER: 1500
IF-MIB::ifMtu.7 = INTEGER: 4078
IF-MIB::ifMtu.8 = INTEGER: 2304
IF-MIB::ifMtu.9 = INTEGER: 1500
IF-MIB::ifMtu.10 = INTEGER: 1500
IF-MIB::ifSpeed.1 = Gauge32: 0
IF-MIB::ifSpeed.2 = Gauge32: 0
IF-MIB::ifSpeed.3 = Gauge32: 0
IF-MIB::ifSpeed.4 = Gauge32: 1000000000
IF-MIB::ifSpeed.5 = Gauge32: 5250000
IF-MIB::ifSpeed.6 = Gauge32: 0
IF-MIB::ifSpeed.7 = Gauge32: 10000000
IF-MIB::ifSpeed.8 = Gauge32: 10000000
IF-MIB::ifSpeed.9 = Gauge32: 0
IF-MIB::ifSpeed.10 = Gauge32: 0
IF-MIB::ifPhysAddress.1 = STRING: 
IF-MIB::ifPhysAddress.2 = STRING: 
IF-MIB::ifPhysAddress.3 = STRING: 
IF-MIB::ifPhysAddress.4 = STRING: 0:6c:8f:4:e6:69
IF-MIB::ifPhysAddress.5 = STRING: 0:40:f3:9f:49:e2
IF-MIB::ifPhysAddress.6 = STRING: 0:0:1d:59:c3:e0
IF-MIB::ifPhysAddress.7 = STRING: 0:7:54:ff:fe:d5:9c:3e
IF-MIB::ifPhysAddress.8 = STRING: 0:40:f3:9f:49:e2
IF-MIB::ifPhysAddress.9 = STRING: 0:6c:8f:40:7:0
IF-MIB::ifPhysAddress.10 = STRING: 0:6c:8f:40:7:64
IF-MIB::ifAdminStatus.1 = INTEGER: up(1)
IF-MIB::ifAdminStatus.2 = INTEGER: down(2)
IF-MIB::ifAdminStatus.3 = INTEGER: down(2)
IF-MIB::ifAdminStatus.4 = INTEGER: up(1)
IF-MIB::ifAdminStatus.5 = INTEGER: up(1)
IF-MIB::ifAdminStatus.6 = INTEGER: up(1)
IF-MIB::ifAdminStatus.7 = INTEGER: up(1)
IF-MIB::ifAdminStatus.8 = INTEGER: down(2)
IF-MIB::ifAdminStatus.9 = INTEGER: up(1)
IF-MIB::ifAdminStatus.10 = INTEGER: up(1)
IF-MIB::ifOperStatus.1 = INTEGER: up(1)
IF-MIB::ifOperStatus.2 = INTEGER: down(2)
IF-MIB::ifOperStatus.3 = INTEGER: down(2)
IF-MIB::ifOperStatus.4 = INTEGER: up(1)
IF-MIB::ifOperStatus.5 = INTEGER: up(1)
IF-MIB::ifOperStatus.6 = INTEGER: up(1)
IF-MIB::ifOperStatus.7 = INTEGER: up(1)
IF-MIB::ifOperStatus.8 = INTEGER: down(2)
IF-MIB::ifOperStatus.9 = INTEGER: up(1)
IF-MIB::ifOperStatus.10 = INTEGER: up(1)
IF-MIB::ifLastChange.1 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.2 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.3 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.4 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.5 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.6 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.7 = Timeticks: (0) 0:00:00.00
IF-MIB::ifLastChange.8 = Timeticks: (309) 0:00:03.09
IF-MIB::ifLastChange.9 = Timeticks: (309) 0:00:03.09
IF-MIB::ifLastChange.10 = Timeticks: (5173577) 14:22:15.77
IF-MIB::ifInOctets.1 = Counter32: 6863903
IF-MIB::ifInOctets.2 = Counter32: 0
IF-MIB::ifInOctets.3 = Counter32: 0
IF-MIB::ifInOctets.4 = Counter32: 2623100
IF-MIB::ifInOctets.5 = Counter32: 1380862186
IF-MIB::ifInOctets.6 = Counter32: 0
IF-MIB::ifInOctets.7 = Counter32: 0
IF-MIB::ifInOctets.8 = Counter32: 0
IF-MIB::ifInOctets.9 = Counter32: 0
IF-MIB::ifInOctets.10 = Counter32: 0
IF-MIB::ifInUcastPkts.1 = Counter32: 121096
IF-MIB::ifInUcastPkts.2 = Counter32: 0
IF-MIB::ifInUcastPkts.3 = Counter32: 0
IF-MIB::ifInUcastPkts.4 = Counter32: 24554
IF-MIB::ifInUcastPkts.5 = Counter32: 2682254
IF-MIB::ifInUcastPkts.6 = Counter32: 0
IF-MIB::ifInUcastPkts.7 = Counter32: 0
IF-MIB::ifInUcastPkts.8 = Counter32: 0
IF-MIB::ifInUcastPkts.9 = Counter32: 0
IF-MIB::ifInUcastPkts.10 = Counter32: 0
IF-MIB::ifInNUcastPkts.1 = Counter32: 0
IF-MIB::ifInNUcastPkts.2 = Counter32: 0
IF-MIB::ifInNUcastPkts.3 = Counter32: 0
IF-MIB::ifInNUcastPkts.4 = Counter32: 0
IF-MIB::ifInNUcastPkts.5 = Counter32: 0
IF-MIB::ifInNUcastPkts.6 = Counter32: 0
IF-MIB::ifInNUcastPkts.7 = Counter32: 0
IF-MIB::ifInNUcastPkts.8 = Counter32: 0
IF-MIB::ifInNUcastPkts.9 = Counter32: 0
IF-MIB::ifInNUcastPkts.10 = Counter32: 0
IF-MIB::ifInDiscards.1 = Counter32: 0
IF-MIB::ifInDiscards.2 = Counter32: 0
IF-MIB::ifInDiscards.3 = Counter32: 0
IF-MIB::ifInDiscards.4 = Counter32: 0
IF-MIB::ifInDiscards.5 = Counter32: 0
IF-MIB::ifInDiscards.6 = Counter32: 0
IF-MIB::ifInDiscards.7 = Counter32: 0
IF-MIB::ifInDiscards.8 = Counter32: 0
IF-MIB::ifInDiscards.9 = Counter32: 0
IF-MIB::ifInDiscards.10 = Counter32: 0
IF-MIB::ifInErrors.1 = Counter32: 0
IF-MIB::ifInErrors.2 = Counter32: 0
IF-MIB::ifInErrors.3 = Counter32: 0
IF-MIB::ifInErrors.4 = Counter32: 0
IF-MIB::ifInErrors.5 = Counter32: 0
IF-MIB::ifInErrors.6 = Counter32: 0
IF-MIB::ifInErrors.7 = Counter32: 0
IF-MIB::ifInErrors.8 = Counter32: 0
IF-MIB::ifInErrors.9 = Counter32: 0
IF-MIB::ifInErrors.10 = Counter32: 0
IF-MIB::ifInUnknownProtos.1 = Counter32: 0
IF-MIB::ifInUnknownProtos.2 = Counter32: 0
IF-MIB::ifInUnknownProtos.3 = Counter32: 0
IF-MIB::ifInUnknownProtos.4 = Counter32: 0
IF-MIB::ifInUnknownProtos.5 = Counter32: 0
IF-MIB::ifInUnknownProtos.6 = Counter32: 0
IF-MIB::ifInUnknownProtos.7 = Counter32: 0
IF-MIB::ifInUnknownProtos.8 = Counter32: 0
IF-MIB::ifInUnknownProtos.9 = Counter32: 0
IF-MIB::ifInUnknownProtos.10 = Counter32: 0
IF-MIB::ifOutOctets.1 = Counter32: 6863903
IF-MIB::ifOutOctets.2 = Counter32: 0
IF-MIB::ifOutOctets.3 = Counter32: 0
IF-MIB::ifOutOctets.4 = Counter32: 1696984
IF-MIB::ifOutOctets.5 = Counter32: 58219438
IF-MIB::ifOutOctets.6 = Counter32: 0
IF-MIB::ifOutOctets.7 = Counter32: 308865
IF-MIB::ifOutOctets.8 = Counter32: 0
IF-MIB::ifOutOctets.9 = Counter32: 303253
IF-MIB::ifOutOctets.10 = Counter32: 20938
IF-MIB::ifOutUcastPkts.1 = Counter32: 60553
IF-MIB::ifOutUcastPkts.2 = Counter32: 0
IF-MIB::ifOutUcastPkts.3 = Counter32: 0
IF-MIB::ifOutUcastPkts.4 = Counter32: 13392
IF-MIB::ifOutUcastPkts.5 = Counter32: 572421
IF-MIB::ifOutUcastPkts.6 = Counter32: 0
IF-MIB::ifOutUcastPkts.7 = Counter32: 0
IF-MIB::ifOutUcastPkts.8 = Counter32: 0
IF-MIB::ifOutUcastPkts.9 = Counter32: 1738
IF-MIB::ifOutUcastPkts.10 = Counter32: 120
IF-MIB::ifOutNUcastPkts.1 = Counter32: 0
IF-MIB::ifOutNUcastPkts.2 = Counter32: 0
IF-MIB::ifOutNUcastPkts.3 = Counter32: 0
IF-MIB::ifOutNUcastPkts.4 = Counter32: 0
IF-MIB::ifOutNUcastPkts.5 = Counter32: 0
IF-MIB::ifOutNUcastPkts.6 = Counter32: 0
IF-MIB::ifOutNUcastPkts.7 = Counter32: 0
IF-MIB::ifOutNUcastPkts.8 = Counter32: 0
IF-MIB::ifOutNUcastPkts.9 = Counter32: 0
IF-MIB::ifOutNUcastPkts.10 = Counter32: 0
IF-MIB::ifOutDiscards.1 = Counter32: 0
IF-MIB::ifOutDiscards.2 = Counter32: 0
IF-MIB::ifOutDiscards.3 = Counter32: 0
IF-MIB::ifOutDiscards.4 = Counter32: 0
IF-MIB::ifOutDiscards.5 = Counter32: 0
IF-MIB::ifOutDiscards.6 = Counter32: 0
IF-MIB::ifOutDiscards.7 = Counter32: 0
IF-MIB::ifOutDiscards.8 = Counter32: 0
IF-MIB::ifOutDiscards.9 = Counter32: 0
IF-MIB::ifOutDiscards.10 = Counter32: 0
IF-MIB::ifOutErrors.1 = Counter32: 0
IF-MIB::ifOutErrors.2 = Counter32: 0
IF-MIB::ifOutErrors.3 = Counter32: 0
IF-MIB::ifOutErrors.4 = Counter32: 0
IF-MIB::ifOutErrors.5 = Counter32: 0
IF-MIB::ifOutErrors.6 = Counter32: 0
IF-MIB::ifOutErrors.7 = Counter32: 0
IF-MIB::ifOutErrors.8 = Counter32: 0
IF-MIB::ifOutErrors.9 = Counter32: 0
IF-MIB::ifOutErrors.10 = Counter32: 0
IF-MIB::ifOutQLen.1 = Gauge32: 0
IF-MIB::ifOutQLen.2 = Gauge32: 0
IF-MIB::ifOutQLen.3 = Gauge32: 0
IF-MIB::ifOutQLen.4 = Gauge32: 0
IF-MIB::ifOutQLen.5 = Gauge32: 0
IF-MIB::ifOutQLen.6 = Gauge32: 0
IF-MIB::ifOutQLen.7 = Gauge32: 0
IF-MIB::ifOutQLen.8 = Gauge32: 0
IF-MIB::ifOutQLen.9 = Gauge32: 0
IF-MIB::ifOutQLen.10 = Gauge32: 0
IF-MIB::ifSpecific.1 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.2 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.3 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.4 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.5 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.6 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.7 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.8 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.9 = OID: SNMPv2-SMI::zeroDotZero
IF-MIB::ifSpecific.10 = OID: SNMPv2-SMI::zeroDotZero
```

The left part is the _"key"_ part, the right part is the _"value"_ part, all the tables of SNMP could be converted in such format. Using

> $ snmptable -v 2c -c public <Host IP> iftable

will output the table content of _"iftable"_ in table format.


Using _"snmptable...iftable"_ could fetch the media interfaces information of a remote computer.


describes the 

#### snmptable
The 

#### ping
The **ping** command

> $ ping 192.168.1.1

```
PING 192.168.1.1 (192.168.1.1): 56 data bytes
64 bytes from 192.168.1.1: icmp_seq=0 ttl=64 time=3.337 ms
64 bytes from 192.168.1.1: icmp_seq=1 ttl=64 time=3.163 ms
```

icmp_seq = ICMP Sequence
ttl = Time to live
ms = Millisecond

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

### arp

arp -a

The _arp_ command uses ICMP to scan the local network. 

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
