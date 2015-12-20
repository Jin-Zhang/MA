#### 1.1.1 Overview
The network scale increases, network administrators is difficult to monitor the status of all devices in a timely , to find and repair the fault.

SNMP is called Simple Network Management Protocol, SNMP is defined the application protocol for the management services on network. For the first time in August 1988 defined by the Internet Engineering Task Force (IETF) research team in order to solve the problem on the Internet router administration, and soon reached a formal standard in RFC1157. SNMP is composed of a series of protocols and specifications, which provide a method for collecting network management information from devices on the network. It collects data from managed devices in two ways: one is polling (polling-only) method, and the other is the interrupt based approach. These protocols are supported by many typical network devices such as routers, hubs, bridges, switches, servers, workstations, printers, modem racks and other network components and devices.
 
All SNMP messages received via UDP port 161, only Trap information using UDP port 162.

#### 1.1.2 SNMP Network Architecture(可以加入图分析)
SNMP network architecture consists of three parts: NMS, Agent and MIB.

#####NMS
NMS is the network manager, is a using SNMP for network device management and monitoring system. NMS refer to a dedicated server for network management, also refer to a device executed management functions of an application.  
NMS can send a request to the Agent, select or modify one or more of the specific parameter values. At the same time, NMS can receive Trap information from Agent sends, in order to learn the current status of the managed devices.

#####Agent
Agent is an application module on device in network, used to maintain the managed device information and to respond NMS's  request, to report management data to the NMS, which sends the request.  
After Agent receives a request information from NMS, completes the query or modify operation and sends the operation result to NMS, in order to complete response. Meanwhile, when the device has malfunction or other event, Agent will send initiatively trap information to the NMS and notice the change of current status on device.

#####MIB
Any managed resource can be represented as an object, called the managed object. MIB is a collection of managed objects.It defines a set of properties for managed objects: Object name, object access permissions and object data types, etc.   
Each Agent has its own MIB. MIB also can be seen as an interface between the NMS and the Agent, through this interface, NMS can make 'read' or 'write' operations to each managed object in Agent, so as to achieve the purpose of managing and monitoring devices.  
MIB stores data use a tree structure. The node of the tree represents a managed object, it can use a path starting from the root to uniquely identify, this path is called OID.(可以加图解释)

#### 1.1.3 SNMP Version
##### SNMPv1
SNMPv1 is the initial version of the SNMP，provides minimal network management capabilities. The SNMPv1's SMI and MIB are relatively simple, there are many security vulnerabilities.  
SNMPv1 uses community name for authentication.The role of community name like a password to restrict the access to the Agent of the NMS. If SNMP packets with community names have not been approved in the NMS or Agent, the packet will be discarded.
##### SNMPv2
SNMPv2 uses also community name for authentication.At the same time It is compatible with SNMPv1 and at the same time expanded SNMPv1 functions:   
Provide more operation types (GetBulk operations, etc.)  
Support for more data types (Counter32 etc.)  
Provide richer error codes, more detailed to distinguish error
##### SNMPv3
SNMPv3 has been enhanced primarily in terms of security, it uses USM und VACM technology.  
USM provides authentication and encryption capabilities, USM introduces the concept of user names and groups, set the authentication and encryption features.  
VACM determine the user, whether is allowed access, specific MIB objects and access method, VACM technology defines five elements: the group, security level, contexts, MIB view, access policy, these elements decide access privileges, whether the user is allowed access.
 
#### 1.1.4 SNMP Operations
SNMP support for multiple operating, mainly for the following basic operations:  
* Get: NMS use the operation to obtain one or more parameter values from the Agent.  
* GetNext: NMS get to the next parameter value of one or more parameters from the Agent.  
* Set: NMS set up one or more parameter values in the Agent.  
* Response: Agent returns one or more parameter values. This action is in response to the preceding three operations.  
* Trap: Agent send actively the operation to inform the NMS, What happened.  
When performing the first four operations, the device uses the UDP protocol in port 161 to send packets, when performing Trap operation, the device uses the UDP protocol in port 162 to send packets. Since using a different port number, so a device can be simultaneously as Agent and NMS.

#### 1.1.5 SNMP Technical advantages
SNMP has the following technical advantages:  
* Based on the standard protocol TCP / IP, transport layer generally use UDP(User Datagram Protocol).  
* Automated Network Management. The network administrators can use SNMP on the network to retrieve information, modify information, find fault, complete fault diagnosis, plan capacity and report.  
* Shield the physical differences in different device, to achieve automatic management of products from different vendors.  
* SNMP provides only the most basic feature, makes independence in the management tasks, physical properties of the managed devices and the actual network type, in order to achieve the management of devices for different vendors.  
* SNMP have simple mode of request - response , active notification methods, timeout and retransmission mechanism.  
* Less packet type, simple format of packet is easy to be resolved and to be implemented.  
* SNMPv3 provides the security mechanisms of authentication and encryption, as well as the access control capabilities based on user and view, to enhance security.