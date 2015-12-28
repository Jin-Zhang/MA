## Showcase

This section will try to implement an experiment. The target is locate a mobile phone on a small network.

### Section 4.1. Case study

This section will implement an experiment. The target is locate a handy on a small network.

#### Experiment environment:
Devices:
ProCurve Switch
Mac Computer
ASUS RT-N16
D-Link
Client: A handy
Devices Topology:
最后画图
Processes of locating:
Pre-configuration
Configure the MAC address of the network devices
The network devices could be Router, Switch or AP(access point). Their addresses must be stored in a „json“ file. A typical section listed below:


#### Section 4.1.2. JSON configuration file sample
```
{
   "interfaces": [
      {
         "mac": "D2:00:1D:59:C3:E0",
         "media_index": 8,
         "name": "en2",
         "status": "active",	
         "link": "00:1C:2E:0E:AA:3F",
      },
   ],
   "name": "Jin-Mac",
   "position": "Unknown",
   "snmp": 2,
   "status": true,
   "type": "router"
}{
   "interfaces": [
      {
         "mac": "BC:EE:7B:97:41:2C",
         "media_index": 5,
         "name": "en0",
         "status": "active"
      }
   ],
   "name": "ASUS",
   "position": "Asus-company",
   "snmp": 0,
   "status": true,
   "type": "ap"
},
{
   "interfaces": [
      {
         "mac": "00:1C:2E:0E:AA:3F",
         "media_index": "1",
         "link": "BC:EE:7B:97:41:2C"
      }
   ],
   "name": "ProCurve",
   "position": "Berlin",
   "snmp": 1,
   "status": true,
   "type": "switch"
}
```

#### (1) Experiment environment:
##### Devices:
+ ProCurve Switch x 1
+ Mac Computer x 1
+ ASUS RT-N16 x 1
+ D-Link x 1
+ Android mobile phone x 1
+ iPhone x 1

##### Devices Topology:
最后画图

#### (2) Processes of locating:
##### A. Pre-configuration
As explained before, the topology map of the network should be stored in the _devices.json_ configuration file. To configure the topology map, the device's name and all the MAC address are needed.

The network devices could be Router, Switch or AP(access point). Their addresses must be stored in a „json“ file. A typical section listed below:

**JSON file sample**:

```
{
   "interfaces": [
      {
         "mac": "D2:00:1D:59:C3:E0",
         "media_index": 8,
         "name": "en2",
         "status": "active",	
         "link": "00:1C:2E:0E:AA:3F",
      },
   ],
   "name": "Jin-Mac",
   "position": "Unknown",
   "snmp": 2,
   "status": true,
   "type": "router"
}{
   "interfaces": [
      {
         "mac": "BC:EE:7B:97:41:2C",
         "media_index": 5,
         "name": "en0",
         "status": "active"
      }
   ],
   "name": "ASUS",
   "position": "Asus-company",
   "snmp": 0,
   "status": true,
   "type": "ap"
},
{
   "interfaces": [
      {
         "mac": "00:1C:2E:0E:AA:3F",
         "media_index": "1",
         "link": "BC:EE:7B:97:41:2C"
      }
   ],
   "name": "ProCurve",
   "position": "Berlin",
   "snmp": 1,
   "status": true,
   "type": "switch"
}
```

This json file contains for now three devices: „Jin-Mac“ as router and the root server, „ProCurve“ as a switch and „ASUS“ as an AP.

The topology structure of the network devices are also have to be configured.
In this experiment, „Jin-Mac“ connects to „ProCurve“, „ProCurve“ connects to „ASUS“.

**config.json** sample:

The _config.json_ file should also be configured, it contains two importand fields: first_hop_ip and host_name.

```
{
    "Host IP": "127.0.0.1",
    "Host name": "Jin-Mac"
}
```

#### 3. Query


On the server web page, only the IP address of the client could be fetchted from the HTTP headers.
	 		
Get the IP address
		
Run command:
		
> $ snmptable -v 2c -c public <Host IP> ipNetToMedia

		
A typical output listed below:

```		
ipNetToMediaIfIndex 		ipNetToMediaPhysAddress ipNetToMediaNetAddress ipNetToMediaType
5 4c:9:d4:4d:d0:d6 192.168.1.1 other
5 ff:ff:ff:ff:ff:ff 192.168.1.255 other
**8 8c:bf:a6:a7:17:63 192.168.2.2 other**
8 10:40:f3:9f:49:e2 192.168.2.5 other
8 0:1c:2e:e:aa:0 192.168.2.7 other
8 ff:ff:ff:ff:ff:ff 192.168.2.255 other
````

The bold row is the mobile phone that we want to find out. In this row, number 8 indicate the media interface, _8c:bf:a6:a7:17:63_ and _192.168.2.2_ is the MAC address and IP address of the mobile phone.

Search the devices.json file, 		media interface 8 connects to the ProCurve switch media interface 		1.
		
And the ProCurve switch media 		interface belongs to ProCurve switch. This device is defined as a 		switch, supports SNMP 1, and is active.

Run command

> snmpwalk -v 2c -c public 192.168.2.7 mib-2.17.7.1.2.2.1.2

It will output the demanded information, an output sample is listed below:

```
SNMPv2-SMI::mib-2.17.7.1.2.2.1.2.1.0.28.46.14.170.0 = INTEGER: 0
SNMPv2-SMI::mib-2.17.7.1.2.2.1.2.1.16.64.243.159.73.226 = INTEGER: 1
SNMPv2-SMI::mib-2.17.7.1.2.2.1.2.1.88.176.53.243.205.40 = INTEGER: 3
SNMPv2-SMI::mib-2.17.7.1.2.2.1.2.1.90.176.53.63.244.100 = INTEGER: 3
SNMPv2-SMI::mib-2.17.7.1.2.2.1.2.1.140.191.166.167.23.99 = INTEGER: 1
SNMPv2-SMI::mib-2.17.7.1.2.2.1.2.2.0.28.46.14.170.1 = INTEGER: 0
````

Care the fifth line, the value 140.191.166.167.23.99 is the decimal format of the MAC address, and it equals to 8c:bf:a6:a7:17:63. After the analyse of this line, it's known that the target mobile phone connects to the media interface 1 of the ProCurve switch.

### Step 5

Again, from the _devices.json_ configurations file, we know that the media interface 1 of the ProCurve switch connects to ASUS. The configuration shows that ASUS is an AP and it doesn't support SNMP, so it shall not have any subdevice. So the ASUS router is returned as the device that directly connects to the mobile phone.

Redirection
redirect the client request to 

SNMP tables
Access SNMP table

SNMP contains a lot of tables.
Used tables in this program are listed below:
ipNetToMediaTable - The IPv4 Address Translation table used for mapping from
IPv4 addresses to physical addresses.

This table has been deprecated, as a new IP version-neutral table has been added. It is loosely replaced by the ipNetToPhysicalTable.
List media interfaces
There are different ways to get the media interfaces of the devices.
Using the ifTable command to list

_snmptable -v 2c -c public localhost ifTable_

SNMP table: IF-MIB::ifTable

```
 ifIndex   ifDescr           ifType ifMtu    ifSpeed          ifPhysAddress ifAdminStatus ifOperStatus  ifLastChange ifInOctets ifInUcastPkts ifInNUcastPkts ifInDiscards ifInErrors ifInUnknownProtos ifOutOctets ifOutUcastPkts ifOutNUcastPkts ifOutDiscards ifOutErrors ifOutQLen              ifSpecific
       1       lo0 softwareLoopback 16384          0                                   up           up  0:0:00:00.00   80614163        912661              0            0          0                 0    80614163         753271               0             0           0         0 SNMPv2-SMI::zeroDotZero
       2      gif0        ieee80212  1280          0                                 down         down  0:0:00:00.00          0             0              0            0          0                 0           0              0               0             0           0         0 SNMPv2-SMI::zeroDotZero
       3      stf0   hippiInterface  1280          0                                 down         down  0:0:00:00.00          0             0              0            0          0                 0           0              0               0             0           0         0 SNMPv2-SMI::zeroDotZero
       4       en0   ethernetCsmacd  1500 1000000000       0:b0:35:f3:cd:28            up           up 5:20:11:09.27 3487803827      22921692              0            0          0                 0  1410249254       13063329               0             0           0         0 SNMPv2-SMI::zeroDotZero
       5       en1   ethernetCsmacd  1500    5250000       0:15:9e:97:55:81            up           up 5:20:11:09.27 1159517553      27396584              0            0          0                 0  1455284450       10840957               0             0           0         0 SNMPv2-SMI::zeroDotZero
       6       fw0         ieee1394  4078   10000000 0:30:62:ff:fe:e9:fb:b8            up           up  0:0:00:00.00          0             0              0            0          0                 0         346              0               0             0           0         0 SNMPv2-SMI::zeroDotZero
       7      p2p0   ethernetCsmacd  2304   10000000       0:15:9e:97:55:81            up           up 5:20:11:09.27          0             0              0            0          0                 0           0              0               0             0           0         0 SNMPv2-SMI::zeroDotZero
       8 bridge100           bridge  1500          0       0:b0:35:3f:f4:64            up           up  7:3:24:05.69          0    4294967256              0            0          0                 0      224699           1412               0             0           0         0 SNMPv2-SMI::zeroDotZero
````

Access the iftable, could 
