#### IP
1.3 IP
IP is the abbreviation for Internet Protocol, meaning "interconnection protocol between networks". In the Internet, it is a set of rules to make all devices, which are connected to the Internet network, compatible with each other for communication. The devices should comply with the rules. Any system manufacturers of a device, as long as it complies the IP, could be interconnected to the Internet. Because of IP, the Internet was able to have rapid development and became the world's largest open communication network.  

IPv4 vs. IPv6
IPv4, Internet Protocol version 4 (IPv4) is the fourth version of the Internet Protocol (IP) ，It is also the first to be used widely, which is the basis of protocol in the current Internet. In 1981, Jon Postel defined the IP in RFC791.  
IPv4 runs on a variety of the bottom network. In local area network, an Ethernet used it most commonly. But its biggest problem is the limited place of network address.  
IPv6, Internet Protocol version 6 is the recent version of the Internet Protocol (IP). IPv6 is the next generation IP protocol, which was designed by IETF (Internet Engineering Task Force), to replace the current Internet Protocol version (IPv4).  
Compared with IPV4, IPV6 has the following advantages:  
*	IPv6 has a larger space for IP address. The length of IPv4 address is 32 bit, that is 2 ^ 32-1 addresses. IPv6 is 128 bit, has 2 ^ 128-1 addresses.  
*	IPv6 uses the smaller routing tables. The assignment of IPv6 address follows Aggregation principle. It makes the Router with a Entry record to represent lots of the subnet, in order to reduce the length of the routing table and improve the speed of packet forwarding in router.  
*	IPv6 enhances the support of Multicast and Flow Control, greatly improving for Quality of Service (QoS).  
*	IPv6 adds the support of the auto-configuration. This is an improvement and expansion of DHCP, to make the network (especially local area network) management more convenient and faster.  
*	IPv6 has a higher level of security. Using IPv6, the users encrypt data at the network layer and check the IP packet.  



#### IP Address  
IP provides a uniform address format, named the Internet Protocol address. It assigns a logical address for each network and each host on the Internet, in order to mask the differences in the physical address. Each device in network needs to have an IP address for normal communication. Then the "IP address" is equivalent to "phone number", and the router acts as "program-controlled switch."  
An IP address is a 32-bit binary number; it is usually divided into four times "8-bit binary number"---four bytes. IP address is usually the dotted decimal notation, the form as (a.b.c.d), in which a, b, c, d is a decimal integer number from 0 to 255.  

IP Address Type
The type of IP address is composed of public address and private address.  
The Internet NIC (Internet Network Information Center) is responsible for the public address. The IP address is assigned to the organizations, which will register or apply to the Inter NIC. It gains access directly to the Internet with it. Private address is a non-registered address, used exclusively for the internal organization.  

IP Address Classification  
IP address according to different network ID is divided into five types, A class to - E class.  
A, B, C class is uniformly distributed Internet NIC in worldwide, D class and E class are the special addresses.  
(See below table) A, B, C (table or text?)
Class D is to be called multicast address.  
Special address  
* Each byte is 0 ("0.0.0.0"), corresponding to the current host  
*	Each byte is 1 ("255.255.255.255"), corresponding to the broadcast address of current subnet  
*	IP addresses cannot be a decimal "127" at the beginning, from 127.0.0.1 to 127.255.255.255 for the Loop Test. Such as: 127.0.0.1 represents the local IP address, using the "http://127.0.0.1" to test the configuration of the Web server in machine.  


IP Address in LAN or WLAN  
In a LAN or WLAN, there are two special IP addresses, a network number and a broadcast address. Network number is the address for addressing, which represents the whole network itself; another is the broadcast address, which represents all of the host network. Network number is the first IP address in the segment, broadcast address is the last IP address in the segment, and these two addresses are not configured on the host. For example, in this segment 192.168.0.0,Subnet Mask is 255.255.255.0, Network number is 192.168.0.0, and the broadcast address is 192.168.0.255. Host IP address can be configured only from 192.168.0.1 to 192.168.0.254.  

