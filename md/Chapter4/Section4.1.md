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