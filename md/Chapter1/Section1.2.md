#### MAC Address

**MAC Address** means _Media Access Control or Medium Access Control_. Or it is called the physical address, hardware address, is used to define the location of network device. In the OSI model, the network layer (OSI Layer 3) is responsible for the IP address; the data link layer is responsible for the MAC address. Therefore, a media interface has a MAC address and an IP address in network. The network interface controller (NIC) determines the MAC address, and it is fixed. (Belongs to the device)  

MAC address used hexadecimal digits separated by hyphens (-) or by colons (:) , a total of six bytes (48 bits). Actually MAC address is the adapter address or adapter identifier EUI-48. It is divided into the first three octets and the following three octets:  
*	The first three octets, is called Organizationally Unique Identifier, namely OUI. It is assigned to different manufacturers, which have registered in IEEE, to distinguish the devices of the different manufacturers.  
*	The following three octets, is assigned by the manufacturers themselves, called Extended Identifier. For the same manufacturer, it is also different.  

Speaking of the MAC address, we have to speak about IP address (see the next section).  
To complete the communication，IP addresses working on the network layer, the packet is forwarded from one network to another network; MAC addresses are based on the data link layer, a frame is transmitted from one node to another one in the same link. In a stable network, IP addresses and MAC addresses are a pair. So IP addresses and MAC addresses are corresponding to each other. This mapping between IP addresses and MAC addresses has to be done by the ARP (Address Resolution Protocol).  
The difference between the MAC address and IP address:  
The same with MAC address and IP address is sole (meaning?), but the different characteristics are:  
*	On the same device or a computer, the change and customisation of the IP address is easy (but it must be unique). The MAC address was made by the manufacturer, it generally cannot be changed.  
*	Different length. The length of IP address is 32 bits, MAC address is 48 bits.  
*	Different assignment rules. IP address based on the network topology, MAC address based on the manufacturer.  
*	Different OSI layer for the addressing.  



  

