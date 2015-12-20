## Chapter 3 Methodology

This chapter will 

### Console commands

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